---
description: L’interface IWiaSegmentationFilter détecte les sous-régions d’un flux d’image et crée des éléments IWiaItem2 distincts pour chacun.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interface IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862674"
---
# <a name="iwiasegmentationfilter-interface"></a>Interface IWiaSegmentationFilter

L’interface **IWiaSegmentationFilter** détecte les sous-régions d’un flux d’image et crée des éléments [**IWiaItem2**](-wia-iwiaitem2.md) distincts pour chacun.

## <a name="members"></a>Membres

L’interface **IWiaSegmentationFilter** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaSegmentationFilter** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaSegmentationFilter** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Détermine les sous-régions d’une image disposées sur le plateau à plat afin que chacune des sous-régions puisse être acquise dans un élément d’image séparé. <br/> |



 

## <a name="remarks"></a>Notes

Une application doit utiliser [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) pour créer une nouvelle instance du filtre de segmentation. Une application appelle généralement cette fonction avant d’afficher sa fenêtre d’aperçu.

Lors de l’implémentation de ce filtre, utilisez [**IWiaItem2 :: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) pour créer les éléments enfants. L’application doit passer **des \_ \_ \_ valeurs de propriétés parentes de copie** au paramètre *ICreationFlags* pour garantir que les propriétés telles que le format et la résolution d’image sont les mêmes dans l’enfant nouvellement créé, comme dans l’élément parent.

Un filtre de segmentation doit prendre en charge tous les formats d’image pris en charge par le pilote qu’il utilise. Le filtre fourni par Microsoft prend en charge les bitmaps (BMP), GIF (Graphics Interchange Format), JPEG, PNG (Portable Network Graphics) et TIFF (Tagged Image File Format).

Le filtre de segmentation doit être utilisé uniquement sur les éléments du scanneur et du film. Pour l’analyse des films, un scanneur est souvent accompagné d’images fixes. dans ce cas, le pilote a créé les éléments enfants et l’application ne doit pas appeler le filtre de segmentation.

L’interface **IWiaSegmentationFilter** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
