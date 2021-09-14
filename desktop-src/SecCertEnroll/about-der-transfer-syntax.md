---
description: L’application d’une règle de codage aux structures de données décrites par une syntaxe abstraite fournit une syntaxe de transfert qui régit la façon dont les octets d’un flux sont organisés lorsqu’ils sont envoyés entre les ordinateurs.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Syntaxe de transfert DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095926"
---
# <a name="der-transfer-syntax"></a>Syntaxe de transfert DER

L’application d’une règle de codage aux structures de données décrites par une syntaxe abstraite fournit une syntaxe de transfert qui régit la façon dont les octets d’un flux sont organisés lorsqu’ils sont envoyés entre les ordinateurs. la syntaxe de transfert utilisée par Distinguished Encoding Rules suit toujours un format de *balise, de longueur et de valeur* . Le format est généralement désigné sous le terme de triplet TLV dans lequel chaque champ (T, L ou V) contient un ou plusieurs octets.

![type der, longueur et valeur (TLV) triplet](images/der-tlv-basic.png)

Le champ de *balise* spécifie le type de la structure de données à envoyer, le champ de *longueur* spécifie le nombre d’octets de contenu à transférer et le champ de *valeur* contient le contenu. Notez que le champ *valeur* peut être un triplet s’il contient un type de données construit comme indiqué dans l’illustration suivante.

![récursivité des triplets de der TLV](images/der-tlv-recursive.png)

Consultez les rubriques suivantes pour obtenir des informations détaillées sur les composants d’un tripleon.

-   [Octets de balise encodés](about-encoded-tag-bytes.md)
-   [Octets de longueur et de valeur encodés](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types construits](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



