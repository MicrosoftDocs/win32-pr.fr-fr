---
description: Prend en charge les signatures numériques et le chiffrement des données. Il est considéré comme un fournisseur de services de chiffrement à usage général (CSP).
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796ac0b77b91b9cffebc6f04ae3812b1bc25aabd885295e7dd3e1715bb4efc04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901589"
---
# <a name="prov_rsa_aes"></a>\_RSA \_ AES Prov.

Le \_ type de \_ fournisseur RSA AES Prov prend en charge les [signatures numériques](digital-signatures.md) et le chiffrement des données. Il est considéré comme un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) à usage général (CSP). L' [*algorithme de clé publique*](../secgloss/p-gly.md) RSA est utilisé pour toutes les opérations de [*clé publique*](../secgloss/p-gly.md) .

## <a name="algorithms-supported"></a>Algorithmes pris en charge

Pour obtenir une description de chacun de ces algorithmes, consultez le Glossaire.



| Objectif      | Algorithmes pris en charge                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exchange de clé | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Signature    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Chiffrement   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hashing      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 et SHA-512)<br/> |



 

## <a name="related-documentation"></a>Documentations associées

Ce type de fournisseur est défini par Microsoft et RSA Data Security. Il est décrit dans les documents suivants :

-   *Guide du programmeur du fournisseur de services de chiffrement Microsoft*, microsoft, 1996.
-   RSA Laboratories, normes de chiffrement à clé publique, RSA Data Security, novembre 1993.

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et dans certains pays ou régions.

 

 

 
