# Keyshuffling Attack for Persistent Early Code Execution in the Nintendo 3DS Secure Bootchain

## [View PDF](https://github.com/Plailect/keyshuffling/blob/master/keyshuffling.pdf)

### Abstract

We demonstrate an attack on the secure bootchain of the Nintendo 3DS in order to gain early code execution. The attack utilizes the block shuffling vulnerability of the ECB cipher mode to rearrange keys in the Nintendo 3DS's encrypted keystore. Because the shuffled keys will deterministically decrypt the encrypted firmware binary to incorrect plaintext data and execute it, and because the device's memory contents are kept between hard reboots, it is possible to reliably reach a branching instruction to a payload in memory. This payload, due to its execution by a privileged processor and its early execution, is able to extract the hash of hardware secrets necessary to decrypt the device's encrypted keystore and set up a persistent exploit of the system.

### Background

This IEEE article was written by me (Devon "Plailect" Maloney) in association with ”stuckpixel”, ”SciresM”, ”Gelex”, ”Normmatt”, and ”Aurora Wright” in order to strengthen my academic resume for the purposes of college and university applications. Information in this article (especially the keyshuffling vulnerability) is original, independent work unless cited otherwise. Note that the keyshuffling vulnerability detailed here is the same one documented publicly by much of this team including "stuckpixel" (also known as "dark_samus") on sites such as [3DBrew](https://www.3dbrew.org). Additionally, note that the persistence vulnerability detailed here is the same one documented publicly as "arm9loaderhax" by "plutoo", "derrek", and "smea" at the [2015 32c3 conference](https://media.ccc.de/v/32c3-7240-console_hacking).

### Authors

+ Devon "Plailect" Maloney *(Contributor)*
+ ”stuckpixel” *(Discoverer)*
+ ”SciresM” *(Implementor)*
+ ”Gelex” *(Contributor)*
+ ”Normmatt” *(Contributor)*
+ ”Aurora Wright” *(Implementor)*