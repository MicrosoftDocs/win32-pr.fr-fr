---
description: Le fournisseur de services de chiffrement DSS et Diffie-Hellman amélioré Microsoft prend en Diffie-Hellman charge l’échange de clés, le hachage SHA, la signature et la vérification des données DSA (FIPS 186-2) et les algorithmes de chiffrement symétrique RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Fournisseur de services de chiffrement DSS & Diffie-Hellman Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c42b4e504c1e5d4cb8ccfea7405580e37362f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193780"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Fournisseur de services de chiffrement DSS & Diffie-Hellman Microsoft

Le fournisseur de services de chiffrement Microsoft Enhanced DSS et [*Diffie-Hellman*](../secgloss/d-gly.md) prend en charge l’échange de clés *Diffie-Hellman, le* hachage SHA, la signature et la vérification des données DSA (FIPS 186-2) et les algorithmes de chiffrement symétrique RC4.

<dl> Type de fournisseur : **Proven \_ DSS \_**  
Nom du fournisseur : **MS \_ ENH \_ DSS \_ DH \_ Prov** .  
</dl>

Ce fournisseur de services de chiffrement prend en charge les algorithmes suivants.

| ID d’algorithme          | Type d’algorithme  | Taille par défaut (bits) | Description                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Chiffrement des données | 40                  | Algorithme de chiffrement de message CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Chiffrement des données | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Chiffrement des données | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ des**         | Chiffrement des données | 56                  | Data Encryption Standard (DES).                                                                                                                            |
| **CALG \_ 3des \_ 112**   | Chiffrement des données | 112                 | Deux clés triple DES.                                                                                                                                        |
| **CALG \_ 3DES**        | Chiffrement des données | 168                 | Triple clé DES.                                                                                                                                      |
| **CALG \_ SHA1**        | Hachage            | 160                 | Secure Hash Algorithm 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hachage            | 128                 | Message Digest 5 (MD5).                                                                                                                                    |
| **CALG \_ DSS \_**   | Signature       | 1 024                | Algorithme de signature numérique (DSA).                                                                                                                         |
| **CALG \_ DH \_ DF**      | Échange de clés    | 1 024                | Algorithme d’échange de clés de stockage et de redirection [*Diffie-Hellman*](../secgloss/d-gly.md) . |
| **CALG \_ DH \_ EPHEM**   | Échange de clés    | 1 024                | Algorithme éphémère [*Diffie-Hellman*](../secgloss/d-gly.md) .                      |



 

 

 
