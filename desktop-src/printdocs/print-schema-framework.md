---
description: Ces articles fournissent des informations plus détaillées sur la signification et l’utilisation des types d’éléments de schéma d’impression.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Structure du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407162"
---
# <a name="print-schema-framework"></a>Structure du schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Cette section fournit des informations plus détaillées sur la signification et l’utilisation des types d’éléments de schéma d’impression. L’objectif principal de la version initiale de l’infrastructure du schéma d’impression est de représenter les configurations et les capacités des attributs des appareils. À un niveau élevé, cette infrastructure offre deux styles différents de description d’un attribut d’appareil : en tant que construction fonctionnalité/option, ou en tant que construction de paramètre. Si un attribut d’appareil a un petit nombre de valeurs ou d’États disponibles, l’attribut doit être caractérisé comme une fonctionnalité avec les valeurs ou les États autorisés appelés éléments d’option. À l’inverse, si un attribut d’appareil a un grand nombre de valeurs ou d’États disponibles et que l’ensemble de toutes les valeurs possibles est facilement défini sans avoir recours à une énumération explicite, l’attribut de l’appareil doit être caractérisé comme un paramètre. (Un paramètre est défini au moyen d’un élément ParameterDef, et une instance de paramètre est initialisée au moyen d’un élément ParameterInit.) Les éléments de propriété sont utilisés dans les constructions de fonctionnalités et d’options et de paramètres pour fournir un niveau de différenciation plus fin.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



