---
title: Supprimer des attributs de métadonnées
description: Supprimer des attributs de métadonnées
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, supprimer des attributs de métadonnées
- ASF (Advanced Systems Format), supprimer les attributs de métadonnées
- ASF (format des systèmes avancés), supprimer les attributs de métadonnées
- métadonnées, supprimer des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381687"
---
# <a name="removing-metadata-attributes"></a>Supprimer des attributs de métadonnées

Vous pouvez supprimer un attribut de métadonnées en passant son numéro d’index et de flux à la méthode [**IWMHeaderInfo3 ::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) . L’ordre dans lequel les attributs restants sont indexés après la suppression d’un attribut ne change pas ; les valeurs d’index de tous les attributs restants ayant une valeur d’index supérieure à celle supprimée sont réduites d’une unité. Lors de la suppression de plusieurs attributs, faites-le dans l’ordre décroissant par index pour éviter d’avoir à calculer l’ajustement dans l’indexation.

Pour faciliter la suppression des valeurs, la méthode [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) retourne les valeurs d’index dans l’ordre décroissant.

> [!Note]  
> Les valeurs d’index obtenues à l’aide des méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) ne sont pas compatibles avec les valeurs d’index obtenues à l’aide des méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Si vous utilisez les méthodes d’une interface pour modifier les attributs d’un fichier, vous devez supposer que toutes les valeurs d’index précédemment récupérées à partir de l’autre interface ne sont plus valides et doivent être retirées. Vous devez éviter d’utiliser les méthodes de **IWMHeaderInfo** si possible.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




