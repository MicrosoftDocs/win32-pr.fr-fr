---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Utilisations du PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953501"
---
# <a name="uses-of-the-printcapabilities"></a>Utilisations du PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le PrintCapabilities est destiné à représenter des attributs d’appareil configurables comme des constructions de fonctionnalité/option ou des constructions de paramètres. Ces informations définissent l’espace de configuration de l’appareil et peuvent être utilisées par un client de l’interface utilisateur pour construire une interface utilisateur. Les mots clés du schéma d’impression définissent un ensemble d’instances de fonctionnalités standard, d’instances d’option pour les instances de fonctionnalités standard et d’instances ParameterDef.

Les constructions de fonctionnalité et d’option ou de paramètres dans PrintCapabilities sont destinées à contenir des instances de propriété ou de ScoredProperty qui décrivent un appareil et qui sont prises en charge par le sous-système de spouleur. Ces instances de propriété et ScoredProperty présentent un intérêt général pour les clients de l’appareil, et contiennent les informations fournies par les fonctions Win32 DevCaps. Les mots clés du schéma d’impression définissent un ensemble de propriétés standard et d’instances ScoredProperty.

Il convient de souligner que le document PrintCapabilities est destiné à représenter uniquement des données à valeur unique : les données qui ne dépendent pas d’une configuration particulière de l’appareil. Le document PrintCapabilities fournit uniquement une capture instantanée de données dépendantes de la configuration.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



