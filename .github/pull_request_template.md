## Pull Request: Switch from DefyX to TariRx Algorithm

### Description
This PR migrates TariMobileMiner from the DefyX algorithm (Scala Network) to the TariRx algorithm (Tari Project) to enable mining of Tari (XTM) coins on Android mobile devices.

### Type of Change
- [x] Algorithm switch (DefyX → TariRx)
- [x] Configuration updates
- [x] Documentation updates
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change

### Changes Made

#### Core Algorithm Changes
- ✅ Updated `Config.java`: Changed algorithm from `panthera` to `tarix` and miner from `xlarig` to `tarixminer`
- ✅ Updated `Utils.java`: Modified wallet address validation for Tari format
- ✅ Updated `Tools.java`: Copyright and compatibility updates

#### Documentation
- ✅ Updated `README.md`: Full documentation rewrite for Tari
- ✅ Created `MIGRATION.md`: Comprehensive migration guide
- ✅ Created `CHANGES.md`: Detailed changelog and next steps
- ✅ Created `config.json`: TariRx configuration template

### Testing Performed
- [x] Code compilation (syntax checked)
- [x] Configuration validation
- [x] Documentation accuracy
- [ ] Android device testing (requires binaries)
- [ ] Mining pool integration (requires binaries)
- [ ] Hashrate calculation (requires binaries)

### Blockers - Must Complete Before Merge

1. **Add TariRx Miner Binaries**
   - Obtain or compile TariRx for Android
   - Add binaries for: arm64-v8a, armeabi-v7a, x86_64
   - Place in: `app/src/main/assets/tarixminer/`
   - Ensure binaries are executable

2. **Update Wallet Addresses**
   - Add primary Tari wallet address to Utils.java
   - Test address validation regex
   - Add donation addresses if applicable

3. **Configure Mining Pools**
   - Add Tari mining pool endpoints
   - Test pool API connectivity
   - Verify pool statistics and payout settings

4. **Device Testing**
   - Build APK and install on test device
   - Verify miner starts correctly
   - Test actual mining with Tari pool
   - Validate temperature monitoring
   - Test all UI features

### Optional Improvements
- [ ] Update Android UI strings (strings.xml)
- [ ] Replace Scala logo with Tari logo
- [ ] Update app icon to Tari branding
- [ ] Add Tari network selection (mainnet/stagenet/testnet)
- [ ] Implement pool selection UI for Tari pools

### Related Issues
- Closes: #[issue-number] (if applicable)
- References: [related issues/discussions]

### Checklist
- [x] My code follows the code style of this project
- [x] I have updated the documentation accordingly
- [x] I have added comments to explain complex changes
- [ ] I have tested this on an actual Android device
- [ ] I have verified the miner binaries work correctly
- [ ] I have updated all relevant strings and resources
- [x] No new warnings are introduced

### Screenshots/Evidence
- Branch: `switch-to-tarix`
- Commits: 2
- Files changed: 6

### Additional Notes

This is a complete algorithm migration from Scala's DefyX to Tari's TariRx. All core configuration and documentation has been updated. The main blocker for testing and merging is obtaining and integrating the TariRx miner binaries for Android.

Please see `MIGRATION.md` for a detailed integration guide.

### Reviewer Guidance

1. **Code Review**: Focus on algorithm configuration changes in `Config.java`
2. **Documentation**: Verify all references to Scala have been updated to Tari
3. **Testing**: Cannot be fully tested without miner binaries
4. **Next Steps**: See CHANGES.md for blockers and required actions

---

**Signed**: DeepFriedBlockchains
**Date**: 2026-09-02
