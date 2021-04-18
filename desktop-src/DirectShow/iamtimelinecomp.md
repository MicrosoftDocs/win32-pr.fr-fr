---
description: L’interface IAMTimelineComp insère ou récupère des pistes virtuelles sur une composition dans les services d’édition DirectShow (DES). Une composition est une collection de couches qui agit comme une seule piste composite.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interface IAMTimelineComp (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540101"
---
# <a name="iamtimelinecomp-interface"></a>Interface IAMTimelineComp

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’interface **IAMTimelineComp** insère ou récupère des pistes virtuelles sur une composition dans les [services d’édition DirectShow](directshow-editing-services.md) (des).

Une composition est une collection de couches qui agit comme une seule *piste* composite. Par exemple, une composition qui contient deux pistes avec une transition entre elles agit comme une seule piste avec la transition précomposée. Une composition doit contenir un média d’un seul type (audio ou vidéo), mais cette limitation n’est pas appliquée. Une *piste virtuelle* est un objet qui peut résider dans une composition, y compris des pistes et d’autres compositions.

Les nœuds les plus haut dans la chronologie sont des *groupes*. Les groupes implémentent à la fois l' `IAMTimelineComp` interface et l’interface [**IAMTimelineGroup**](iamtimelinegroup.md) .

Pour créer un objet de composition, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la chronologie valeur de \_ \_ type principal \_ composite. Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineComp` interface. Pour plus d’informations, consultez [le modèle de chronologie](the-timeline-model.md) et [construction d’une chronologie](constructing-a-timeline.md).

## <a name="members"></a>Membres

L’interface **IAMTimelineComp** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineComp** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineComp** possède ces méthodes.



| Méthode                                                                       | Description                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Récupère le nombre d’objets d’un type donné contenus dans cette composition et toutes ses pistes virtuelles, de manière récursive.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Récupère la piste virtuelle suivante après une piste virtuelle spécifiée.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, et récupère la *n* ième piste virtuelle à partir de ce classement.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | Non pris en charge.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Récupère la piste virtuelle à la priorité spécifiée.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Récupère le nombre de pistes virtuelles contenues dans la composition.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Insère une piste virtuelle dans la composition à la priorité spécifiée.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Change les niveaux de priorité de deux pistes.<br/>                                                                                                    |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
