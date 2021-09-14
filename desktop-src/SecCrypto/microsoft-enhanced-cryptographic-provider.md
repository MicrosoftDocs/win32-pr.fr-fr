---
description: Le fournisseur de services de chiffrement amélioré Microsoft prend en charge les mêmes fonctionnalités que le fournisseur de chiffrement de base Microsoft, mais il prend en charge une sécurité renforcée grâce à des clés plus longues et des algorithmes supplémentaires.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Fournisseur de services de chiffrement amélioré Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf3b3b421e3151811da033e7536f334e3883487
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193783"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Fournisseur de services de chiffrement amélioré Microsoft

Le fournisseur de services de chiffrement amélioré Microsoft, appelé fournisseur amélioré, prend en charge les mêmes fonctionnalités que le fournisseur de chiffrement de base Microsoft, appelé fournisseur de base. Le fournisseur amélioré prend en charge une sécurité renforcée grâce à des clés plus longues et des algorithmes supplémentaires. Il peut être utilisé avec toutes les versions de CryptoAPI.

Pour assurer la compatibilité descendante avec les versions antérieures du fournisseur, le nom du fournisseur, tel que défini dans le fichier d’en-tête Wincrypt. h, conserve la désignation de la version 1,0. Toutefois, la version 2,0 de ce fournisseur est actuellement commercialisée. Pour déterminer la version du fournisseur en cours d’utilisation, appelez [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec l’argument *DwParam* défini sur **pp \_ version**. La version 2,0 est utilisée si 0x0200 est retourné.

|                   | Valeur               |
|-------------------|---------------------|
| **Type de fournisseur** | PROUVER \_ RSA \_ Full     |
| **Nom du fournisseur** | \_ \_ Proven avancé ms  |



 

Le tableau suivant met en évidence les différences entre le fournisseur de base, le fournisseur fort et le fournisseur amélioré. Les longueurs de clé affichées sont les longueurs de clé par défaut.



| Algorithm                                                                                | Longueur de la clé du fournisseur de base | Longueur de clé du fournisseur fort | Longueur de la clé du fournisseur amélioré                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algorithme de signature de clé publique RSA                                                       | 512 bits                 | 1 024 bits                 | 1 024 bits                                  |
| Algorithme d’échange de clés publiques RSA                                                        | 512 bits                 | 1 024 bits                 | 1 024 bits                                  |
| Algorithme de chiffrement par bloc RC2                                                           | 40 bits                  | 128 bits                   | la longueur du Salt 128 bits peut être définie.<br/> |
| Algorithme de chiffrement de flux RC4                                                          | 40 bits                  | 128 bits                   | la longueur du Salt 128 bits peut être définie.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 clés) | Non pris en charge            | 112 bits                   | 112 bits                                    |
| Triple DES (clé 3)                                                                       | Non pris en charge            | 168 bits                   | 168 bits                                    |



 

Le fournisseur fort et le fournisseur amélioré sont à compatibilité descendante avec le fournisseur de base, sauf que les fournisseurs peuvent uniquement générer des clés RC2 ou RC4 de [*longueur de clé*](../secgloss/k-gly.md)par défaut. La longueur par défaut pour le fournisseur de base est de 40 bits. La longueur par défaut du fournisseur amélioré est de 128 bits. Le fournisseur amélioré ne peut donc pas créer de clés avec des longueurs de clé compatibles avec le fournisseur de base. Toutefois, le fournisseur amélioré peut importer des clés RC2 et RC4 allant jusqu’à 128 bits. Par conséquent, le fournisseur amélioré peut importer et utiliser les clés de bits 40 générées à l’aide du fournisseur de base.

 

 
