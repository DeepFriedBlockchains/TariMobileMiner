# Tari Mobile Miner - Migration Guide

## Changes from Scala to Tari

This document outlines all changes made to migrate from Scala (DefyX) to Tari (TariRx).

### Core Configuration Changes

1. **Algorithm**: Changed from `panthera` (DefyX) to `tarix` (TariRx)
2. **Miner**: Changed from `xlarig` to `tarixminer`
3. **Coin**: Tari (XTM)

### File Changes

#### Config.java
- Line 27: Updated changelog URL to DeepFriedBlockchains/TariMobileMiner
- Line 28: Updated releases URL to DeepFriedBlockchains/TariMobileMiner
- Line 73: Changed miner from `xlarig` to `tarixminer`
- Line 74: Changed algorithm from `panthera` to `tarix`

#### Utils.java
- Updated wallet addresses (currently empty - please add Tari wallet addresses)
- Updated address regex patterns to match Tari wallet format
- Updated copyright header to include Tari

#### Tools.java
- No functional changes - tool utilities remain the same
- Updated copyright header to include Tari

#### README.md
- Updated project title and description
- Changed algorithm reference from DefyX to TariRx
- Updated wallet and contact information
- Updated links to Tari resources

### Next Steps Required

1. **Replace Miner Binaries**
   - Add TariRx miner binaries to `app/src/main/assets/tarixminer/`
   - Include binaries for: arm64-v8a, armeabi-v7a, x86_64
   - Ensure binaries are named appropriately for the platform

2. **Update Wallet Addresses**
   - Add Tari wallet address to Utils.java (TARI_XTM_ADDRESS)
   - Add BTC and ETH donation addresses if applicable

3. **Update Pool Configuration**
   - Configure default Tari mining pools
   - Update pool API endpoints
   - Test pool connectivity

4. **Test Mining**
   - Verify miner binary execution
   - Test mining with Tari pool
   - Validate hashrate calculations
   - Test temperature monitoring

5. **Update UI Resources**
   - Update strings.xml with Tari branding
   - Update logo and app icon for Tari branding
   - Update help text and documentation

### Miner Binary Requirements

The TariRx miner binaries must be placed in:
- `app/src/main/assets/tarixminer/arm64-v8a/tarixminer` (or similar name)
- `app/src/main/assets/tarixminer/armeabi-v7a/tarixminer`
- `app/src/main/assets/tarixminer/x86_64/tarixminer`

The exact naming convention should match what Config.java specifies (currently `tarixminer`).
