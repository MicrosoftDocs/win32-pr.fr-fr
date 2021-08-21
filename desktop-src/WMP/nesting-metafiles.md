---
title: Imbrication de refichiers
description: Imbrication de refichiers
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Fichiers multimédias, imbrication
- Windows Fichiers multimédias, référencement d’autres sous-fichiers
- imbrication de refichiers
- refichiers, imbrication
- les sous-fichiers, qui font référence à d’autres sous-fichiers
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29a45bf545f839e111970b31d5faddd039959b7148a331fa5e347913b67327e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574272"
---
# <a name="nesting-metafiles"></a>Imbrication de refichiers

Un métafichier peut faire référence à un autre métafichier. Pour référencer un autre métafichier, utilisez l’élément **ENTRYREF** . Un élément **ENTRYREF** dans le métafichier principal pointe vers un métafichier externe.

le contrôle Lecteur Windows Media traite les éléments d' **entrée** du métafichier référencé comme s’ils étaient inclus dans le métafichier principal à la position de l’élément **ENTRYREF** . Toutefois, elle ignore tous les éléments d' **entrée** dans le métafichier référencé dont l’attribut **SKIPIFREF** a la valeur Yes.

les Lecteur Windows Media 7,0, 7,1 et Lecteur Windows Media pour les contrôles Windows XP ignorent tous les éléments **ENTRYREF** dans le métafichier référencé. Par conséquent, les fichiers de conversions ne peuvent être imbriqués qu’un niveau profond à l’aide de ces versions. Ces versions ignorent également l’élément **ASX** et ses attributs dans le fichier référencé. Lecteur Windows Media série 9 ou version ultérieure prend en charge l’imbrication de safiles jusqu’à 5 de profondeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> </dl>

 

 




