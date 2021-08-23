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
ms.openlocfilehash: 304b5be43aad8afc1730d2a23c170f11f11d319ffc4ae3eb13781efe09da2d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659699"
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



 

## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
