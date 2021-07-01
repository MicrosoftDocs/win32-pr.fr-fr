---
title: Document en tant qu’instantané des propriétés
description: Examinez le document PrintCapabilities comme un instantané des propriétés. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118644"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Document PrintCapabilities comme un instantané des propriétés

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’appareil décrit par le PrintCapabilities peut avoir des propriétés qui dépendent de l’État ou de la configuration de l’appareil. Alors que PrintCapabilities représente l’espace de configuration complet d’un appareil, le fournisseur PrintCapabilities produit une instance dépendante de la configuration du PrintCapabilities, appelée document PrintCapabilities. Ce document PrintCapabilities dépendant de la configuration évite la charge du schéma PrintCapabilities avec la complexité de la représentation des données à valeurs multiples. Plus important encore, pour soulager un consommateur du document PrintCapabilities du point de vue de l’extraction de la valeur appropriée d’une représentation de données à valeurs multiples, toutes les instances Property et ScoredProperty d’un document PrintCapabilities doivent être à valeur unique. En d’autres termes, chaque propriété et instance ScoredProperty dans un document PrintCapabilities doit avoir une valeur fixe, relative à la configuration d’entrée. Chaque document PrintCapabilities peut être considéré comme un instantané des propriétés de l’appareil lorsque ce dernier est dans un état particulier. Par conséquent, avant de pouvoir construire un document PrintCapabilities, vous devez fournir la configuration à utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



