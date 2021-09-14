---
title: Objet de propriétés du média de sortie
description: Objet de propriétés du média de sortie
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK, sortie objets propriétés du média
- ASF (Advanced Systems Format), sortie objets propriétés du média
- ASF (format des systèmes avancés), objets de propriétés de média de sortie
- objets, propriétés du média de sortie objets
- objets de propriétés de média de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234551"
---
# <a name="output-media-properties-object"></a>Objet de propriétés du média de sortie

Un objet de propriétés de média de sortie est utilisé pour récupérer et définir une propriété de sortie. Les objets de propriétés de média de sortie sont créés pour les formats de sortie de flux pris en charge dans un fichier qui est chargé dans un objet lecteur. Pour les flux compressés, les propriétés de sortie sont déterminées par les sorties possibles du codec de décompression.

Un objet de propriétés de média de sortie est créé par [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) cette méthode crée un objet de propriétés de média de sortie qui contient les propriétés du format de sortie par défaut. D’autres formats peuvent être pris en charge pour une sortie. Pour obtenir des formats de sortie supplémentaires, vous pouvez appeler [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) pour obtenir le nombre de formats de sortie pris en charge, puis les parcourir à l’aide d’appels à [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat** crée un objet de propriétés de média de sortie rempli avec les données pour le format de sortie sélectionné.

Les objets de propriétés de média de sortie peuvent également être créés avec le lecteur synchrone. Tous les noms de méthode sont identiques à ceux du lecteur et sont tous exposés par l’interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

**GetOutputProps** et **GetOutputFormat** définissent tous deux un pointeur vers une interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) . Les autres interfaces de l’objet de propriétés de média de sortie peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par chaque objet de propriétés de média de sortie.



| Interface                                          | Description                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Utilisé comme interface de base pour les autres interfaces de propriété de média (entrée, sortie et vidéo).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Récupère les propriétés d’une sortie.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Gère les propriétés d’un flux vidéo. Il s’agit d’une interface facultative, disponible uniquement pour les flux vidéo. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Lecteur, objet**](reader-object.md)
</dt> </dl>

 

 




