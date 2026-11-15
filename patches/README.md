# patches/

Source patches applied to the upstream desktop client before the build, by `scripts/apply-oem.sh` in name
order. Most branding is CMake variables (`OEM.cmake`) and theme files; today there are two patches:
`0001` (enforced server ignores overrides) and `0002` (setup wizard: Virtual files only, other choices greyed
out with a Contact button). `0002` carries the support address, so it is rendered per tenant by
`client-build/gen-oem.py` from `client-build/templates/patches/` and is not stored here.

A patch goes here only when a change to upstream code is unavoidable. Each patch must be a `git
format-patch` file against the exact upstream tag in `oem.json`, numbered (`0001-...patch`), with a
one-line reason at the top. Every patch is part of the corresponding source (GPL) and must be listed in
`README.md`.
