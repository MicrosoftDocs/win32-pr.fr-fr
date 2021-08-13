---
description: L’interface IWiaPreview met en cache les images non filtrées en interne et les transmet via des filtres de traitement d’image.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interface IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442069"
---
# <a name="iwiapreview-interface"></a>Interface IWiaPreview

L’interface **IWiaPreview** met en cache les images non filtrées en interne et les transmet via des filtres de traitement d’image.

## <a name="members"></a>Membres

L’interface **IWiaPreview** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaPreview** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaPreview** possède ces méthodes.



| Méthode                                                  | Description                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Effacer**](-wia-iwiapreview-clear.md)                 | Libère l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Il libère également le filtre de traitement d’image. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) au filtre. <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Met en cache en interne l’image non filtrée retournée par le pilote. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Obtient l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . <br/>                                                            |



 

## <a name="remarks"></a>Remarques

Ce filtre est appelé automatiquement par la méthode [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md) .

L’interface **IWiaPreview** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
