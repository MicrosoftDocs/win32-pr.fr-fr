---
description: Le fournisseur de services de chiffrement RSA et AES amélioré de Microsoft prend en charge les mêmes fonctionnalités que le fournisseur de chiffrement de base Microsoft, appelé fournisseur de base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Fournisseur de services de chiffrement AES Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581867"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Fournisseur de services de chiffrement AES Microsoft

Le fournisseur de services de chiffrement RSA et AES amélioré de Microsoft prend en charge les mêmes fonctionnalités que le fournisseur de chiffrement de base Microsoft, appelé fournisseur de base. Le fournisseur AES prend en charge une sécurité renforcée via des clés plus longues et des algorithmes supplémentaires. Il peut être utilisé avec toutes les versions de CryptoAPI.

**Windows XP :** Le fournisseur de services de chiffrement AES Microsoft s’appelait Microsoft Enhanced RSA et AES Cryptographic Provider (prototype).

Pour assurer la compatibilité descendante avec les versions antérieures du fournisseur, le nom du fournisseur, tel que défini dans le fichier d’en-tête Wincrypt. h, conserve la désignation de la version 1,0 même si des versions plus récentes de ce fournisseur ont été expédiées. Pour déterminer la version du fournisseur en cours d’utilisation, appelez [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec le paramètre *DWPARAM* défini sur pp \_ version. La version 2,0 est utilisée si 0x0200 est retourné.

|                   | Valeur                    |
|-------------------|--------------------------|
| **Type de fournisseur** | \_RSA \_ AES Prov.           |
| **Nom du fournisseur** | \_ \_ RSA \_ AES Prov ENH \_  |



 

Le tableau suivant met en évidence les différences entre le fournisseur de base, le fournisseur fort et le fournisseur AES. Les [*longueurs de clé*](../secgloss/k-gly.md) affichées sont les longueurs de clé par défaut.



| Algorithm                                                                                | Longueur de la clé du fournisseur de base | Longueur de clé du fournisseur fort | Longueur de la clé du fournisseur AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algorithme de signature de clé publique RSA                                                       | 512 bits                 | 1 024 bits                 | 1 024 bits                                  |
| Algorithme d’échange de clés publiques RSA                                                        | 512 bits                 | 1 024 bits                 | 1 024 bits                                  |
| Algorithme de chiffrement par bloc RC2                                                           | 40 bits                  | 128 bits                   | la longueur du Salt 128 bits peut être définie.<br/> |
| Algorithme de chiffrement de flux RC4                                                          | 40 bits                  | 128 bits                   | la longueur du Salt 128 bits peut être définie.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 clés) | Non pris en charge            | 112 bits                   | 112 bits                                    |
| Triple DES (clé 3)                                                                       | Non pris en charge            | 168 bits                   | 168 bits                                    |



 

Pour obtenir la liste complète des algorithmes pris en charge, consultez [algorithmes de fournisseur AES](aes-provider-algorithms.md).

Le fournisseur fort, le fournisseur amélioré et le fournisseur AES sont à compatibilité descendante avec le fournisseur de base, sauf que les fournisseurs peuvent générer uniquement des clés RC2 ou RC4 de longueur de clé par défaut. La longueur par défaut pour le fournisseur de base est de 40 bits. La longueur par défaut du fournisseur AES est 128 bits. Par conséquent, le fournisseur AES ne peut pas créer de clés avec des longueurs de clé compatibles avec le fournisseur de base. Toutefois, le fournisseur AES peut importer des clés RC2 et RC4 allant jusqu’à 128 bits. Par conséquent, le fournisseur AES peut importer et utiliser des clés 40 bits générées à l’aide du fournisseur de base.

 

 
