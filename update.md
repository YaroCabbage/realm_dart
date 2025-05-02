# Realm Dart Repository Update Process

**Original repository:** https://github.com/realm/realm-dart

When the original repository is updated, we need to update our fork as follows:

1. Merge changes from the original repository, selecting all changes from the original repository

2. Check if dependencies were updated in the original repo:
   - If dependencies were updated (analyzer → v7, source_gen → v2, dart_style → v3):
     - Reapply only the last commit from [our fork](https://gitlab.com/hero-chums/browser/hero-mobile-deps/realm_dart/-/tree/for-hero?ref_type=heads)
   - Otherwise:
     - Reapply the last two commits from our fork

3. Don't forget to check if this instruction still persists after updates

**Note:** The last commit from our fork allows us to separate the builder package from the main package. We're doing this to make sure that changes from the generator do not get into the app itself.