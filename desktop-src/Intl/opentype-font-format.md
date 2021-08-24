---
description: Le format de police OpenType Unicode étend le format de fichier de police TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Format des polices OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18324f3a9c84553da81c9f9723a2ecd67c03539b4dd39c7a80afc4be5cdcda66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147092"
---
# <a name="opentype-font-format"></a>Format des polices OpenType

Le format de police OpenType Unicode étend le format de fichier de police TrueType. Les polices OpenType autorisent le mappage entre les caractères et les [glyphes](uniscribe-glossary.md), en activant la prise en charge des ligatures, des formes positionnelles, des alternatives et d’autres substitutions. les polices OpenType peuvent également inclure des informations qui prennent en charge le positionnement de glyphes à deux dimensions et une pièce jointe de glyphe, et peuvent contenir des contours TrueType ou PostScript.

Les fonctionnalités de disposition dans les polices OpenType sont organisées par scripts et langages, ce qui permet à une police unique de prendre en charge plusieurs systèmes d’écriture, même au sein du même script. Pour garantir la cohérence des opérations de disposition du texte et éviter une surcharge inutile dans les fichiers de polices ou les applications, un grand nombre des algorithmes de mise en page du texte et des algorithmes sémantiques de langage sont inclus dans Uniscribe. Cela évite au développeur de polices d’avoir à définir des règles de script généralisées dans une police.

Les applications peuvent introduire des connaissances ou des préférences spécifiques concernant la disposition des scripts. Les polices de disposition OpenType peuvent même contenir des règles de disposition qui dupliquent ou remplacent celles appliquées par les services du système d’exploitation. La structure en couches des services de système d’exploitation prenant en charge la disposition du texte permet à une application de choisir les informations de mise en page à utiliser, et de choisir comment l’appliquer. Pour plus d’informations, consultez la [vue d’ensemble des spécifications de typographie Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) ou la [spécification OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



