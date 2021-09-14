---
description: à compter de Windows 10, CNG prend en charge les courbes elliptiques nommées suivantes (ANSI x 9.62, x 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Courbes elliptiques nommées CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237732"
---
# <a name="cng-named-elliptic-curves"></a>CNG nommé courbes elliptique

à compter de Windows 10, CNG prend en charge les courbes elliptiques nommées suivantes (ANSI x 9.62, x 9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ Curve \_ 25519**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------|
| Nom              | curve25519                                                  |
| Standard          | [Courbe 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Taille de la clé (bits)   | 255                                                         |
| Compatibilité TLS       |                                                             |
| Identificateur d'objet | None                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP160R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP160r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 160                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP160t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 160                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP192R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP192r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 192                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP192T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP192t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 192                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP224R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP224r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 224                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP224T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP224t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 224                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP256R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP256r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 256                                                                                                               |
| Compatibilité TLS       | Oui                                                                                                               |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP256T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP256t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 256                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP320R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP320r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 320                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP320t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 320                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP384r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 384                                                                                                               |
| Compatibilité TLS       | Oui                                                                                                               |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP384T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP384t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 384                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP512R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP512r1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 512                                                                                                               |
| Compatibilité TLS       | Oui                                                                                                               |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP512T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nom              | brainpoolP512t1                                                                                                   |
| Standard          | [Les courbes et la génération de courbe ECC Brainpool standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Taille de la clé (bits)   | 512                                                                                                               |
| Compatibilité TLS       | Non                                                                                                                |
| Identificateur d'objet | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------|
| Nom              | ec192wapi                                                      |
| Standard          | Chinois national standard pour les réseaux locaux sans fil (Go 15629.11-2003) |
| Taille de la clé (bits)   | 192                                                            |
| Compatibilité TLS       | Non                                                             |
| Identificateur d'objet | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP192**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nom              | nistP192                                                                                                                     |
| Standard          | [Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Taille de la clé (bits)   | 192                                                                                                                          |
| Compatibilité TLS       | Oui                                                                                                                          |
| Identificateur d'objet | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nom              | nistP224                                                                                                                     |
| Standard          | [Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Taille de la clé (bits)   | 224                                                                                                                          |
| Compatibilité TLS       | Oui                                                                                                                          |
| Identificateur d'objet | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP256**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nom              | nistP256                                                                                                                     |
| Standard          | [Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Taille de la clé (bits)   | 256                                                                                                                          |
| Compatibilité TLS       | Oui                                                                                                                          |
| Identificateur d'objet | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nom              | nistP384                                                                                                                     |
| Standard          | [Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Taille de la clé (bits)   | 384                                                                                                                          |
| Compatibilité TLS       | Oui                                                                                                                          |
| Identificateur d'objet | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP521**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nom              | nistP521                                                                                                                     |
| Standard          | [Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Taille de la clé (bits)   | 521                                                                                                                          |
| Compatibilité TLS       | Oui                                                                                                                          |
| Identificateur d'objet | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nom              | numsP256t1                                                                                                                              |
| Standard          | [Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Taille de la clé (bits)   | 256                                                                                                                                     |
| Compatibilité TLS       | Non                                                                                                                                      |
| Identificateur d'objet | None                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nom              | numsP384t1                                                                                                                              |
| Standard          | [Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Taille de la clé (bits)   | 384                                                                                                                                     |
| Compatibilité TLS       | Non                                                                                                                                      |
| Identificateur d'objet | None                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ Curve \_ NUMSP512T1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nom              | numsP512t1                                                                                                                              |
| Standard          | [Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Taille de la clé (bits)   | 512                                                                                                                                     |
| Compatibilité TLS       | Non                                                                                                                                      |
| Identificateur d'objet | None                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP160k1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 160                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP160r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 160                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP160r2                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 160                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP192K1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP192k1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 192                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP192r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 192                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP224K1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP224k1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 224                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP224R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP224r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 224                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP256K1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP256k1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 256                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP256R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP256r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 256                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP384r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 384                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP521R1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| Nom              | secP521r1                                                                       |
| Standard          | [Paramètres de domaine de courbe elliptique recommandés](https://www.secg.org/sec2-v2.pdf) |
| Taille de la clé (bits)   | 521                                                                             |
| Compatibilité TLS       | Oui                                                                             |
| Identificateur d'objet | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ Curve \_ WTLS12**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|--------------|
| Nom              | wtls12       |
| Standard          | WTLS         |
| Taille de la clé (bits)   | 224          |
| Compatibilité TLS       | Non           |
| Identificateur d'objet | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ Curve \_ WTLS7**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|--------------|
| Nom              | wtls7        |
| Standard          | WTLS         |
| Taille de la clé (bits)   | 160          |
| Compatibilité TLS       | Non           |
| Identificateur d'objet | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------|
| Nom              | wtls9         |
| Standard          | WTLS          |
| Taille de la clé (bits)   | 160           |
| Compatibilité TLS       | Non            |
| Identificateur d'objet | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ Curve \_ X962P192V1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P192v1          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 192                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P192v2          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 192                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ Curve \_ X962P192V3**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P192v3          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 192                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P239v1          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 239                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P239v2          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 239                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 de courbe ECC**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P239v3          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 239                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ Curve \_ X962P256V1**</dt> <dd> <dl> <dt> 

| Condition requise | Valeur |
|-------------------|---------------------|
| Nom              | x962P256v1          |
| Standard          | ANSI X 9.62          |
| Taille de la clé (bits)   | 256                 |
| Compatibilité TLS       | Non                  |
| Identificateur d'objet | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour utiliser une courbe nommée, appelez [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) à l’aide de l' **\_ \_ algorithme ECDSA bcrypt** ou de l' **\_ \_ algorithme ECDH bcrypt** comme ID d’algorithme. Ensuite, appelez [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) et définissez la propriété de nom de la **\_ \_ courbe \_ de BCRYPT** à l’aide de l’une des courbes ci-dessus ou de toute courbe nommée inscrite sur l’ordinateur comme indiqué par la `certutil -displayEccCurve` commande.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




