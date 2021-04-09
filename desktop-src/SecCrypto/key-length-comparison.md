---
description: Le fournisseur de services de chiffrement amélioré de Microsoft fournit une application offrant une sécurité renforcée par rapport au fournisseur de services de chiffrement de base Microsoft. Une longueur de clé supérieure offre aux utilisateurs une meilleure protection des données sensibles.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparaison de la longueur de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869013"
---
# <a name="key-length-comparison"></a>Comparaison de la longueur de clé

Le fournisseur de services de chiffrement amélioré de Microsoft fournit une application offrant une sécurité renforcée par rapport au fournisseur de services de chiffrement de base Microsoft. Une longueur de clé supérieure offre aux utilisateurs une meilleure protection des données sensibles.

Le tableau suivant répertorie les [*longueurs de clé*](../secgloss/k-gly.md) par défaut prises en charge par le fournisseur de base et le fournisseur amélioré pour les algorithmes standard.



| Algorithm                                                                                | Fournisseur de base | Fournisseurs forts et améliorés |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Échange de clés RSA                                                                         | 512 bits       | 1 024 bits                     |
| Signature RSA                                                                            | 512 bits       | 1 024 bits                     |
| RC2                                                                                      | 40 bits        | 128 bits                       |
| RC4                                                                                      | 40 bits        | 128 bits                       |
| DES                                                                                      | Non pris en charge | 56 bits                        |
| [*Triple des*](../secgloss/t-gly.md) (2-clé) | Non pris en charge | 112 bits                       |
| Triple DES (3 touches)                                                                       | Non pris en charge | 168 bits                       |



 

Les algorithmes [*des*](../secgloss/d-gly.md) et [*triple des*](../secgloss/t-gly.md) sont pris en charge dans le fournisseur amélioré.

Le fournisseur amélioré est à compatibilité descendante avec le fournisseur de base distribué avec les versions antérieures de CryptoAPI, avec l’exception suivante. Le fournisseur de base et le fournisseur amélioré peuvent uniquement générer des clés de session de longueur de clé par défaut. La longueur par défaut des clés de session pour le fournisseur de base est de 40 bits. La longueur de clé par défaut pour le fournisseur amélioré est 128 bits. Le fournisseur amélioré ne peut pas créer de clés avec des longueurs de clé compatibles avec le fournisseur de base. Toutefois, le fournisseur amélioré peut importer des longueurs de clé de n’importe quelle taille, jusqu’à 128 bits.

 

 
