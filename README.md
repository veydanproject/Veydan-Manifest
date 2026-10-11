# Veydan-Manifest

The signed infrastructure manifest of the Veydan apps: the relays, media, push and call servers and the storage hosts a fresh install starts from.

- `manifest.json`: the current manifest, a Nostr event of kind 30078 with the tag `d` = `net.veydan.messenger.manifest`.
- `manifest-<serial>.json`: every manifest published, by its serial.

The apps take a manifest only when its signature is by the project's key and its `serial` is above the one they hold, so this repository is a mirror that cannot point them anywhere else.

Project key (hex): `9a3df86b487832646de015da85813b568fe3419e5d3d7a6c9a234592a66c6871`

To check a copy by hand: the event's `pubkey` is the key above, its `id` is the SHA-256 of `[0, pubkey, created_at, kind, tags, content]` serialised as NIP-01 says, and `sig` is a BIP-340 Schnorr signature of that id by the key.

Developed by Rookbeam Technologies LLC, USA
