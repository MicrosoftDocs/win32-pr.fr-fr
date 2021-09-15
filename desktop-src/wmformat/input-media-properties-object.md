---
title: Objet Propriétés du média d’entrée
description: Objet Propriétés du média d’entrée
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, Input Media Properties Objects
- ASF (Advanced Systems Format), objets de propriétés de média d’entrée
- ASF (format de systèmes avancés), objets de propriétés de média d’entrée
- objets, objets de propriétés de média d’entrée
- objets de propriétés de média d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404694"
---
# <a name="input-media-properties-object"></a>Objet Propriétés du média d’entrée

Un objet de propriétés de média d’entrée créé par l’objet Writer prend en charge les interfaces suivantes. Ces interfaces sont accessibles par un appel à **QueryInterface** sur l’une des interfaces de l’objet Writer.



| Interface                                        | Description                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Récupère les propriétés d’un flux d’entrée.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Utilisé comme interface de base pour les autres interfaces de propriété de média (entrée, sortie et vidéo).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gère les propriétés d’un flux vidéo. Il s’agit d’une interface facultative, disponible uniquement pour les flux vidéo. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Auteur, objet**](writer-object.md)
</dt> </dl>

 

 




