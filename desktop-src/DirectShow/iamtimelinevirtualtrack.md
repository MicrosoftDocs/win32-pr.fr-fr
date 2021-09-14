---
description: l’interface IAMTimelineVirtualTrack fournit des méthodes pour travailler avec des pistes virtuelles dans DirectShow Services d’édition (DES). Les compositions et les suivis prennent en charge cette interface.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interface IAMTimelineVirtualTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012173"
---
# <a name="iamtimelinevirtualtrack-interface"></a>Interface IAMTimelineVirtualTrack

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineVirtualTrack` interface fournit des méthodes pour travailler avec des pistes virtuelles dans [DirectShow Services d’édition](directshow-editing-services.md) (DES). Les compositions et les suivis prennent en charge cette interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineVirtualTrack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineVirtualTrack** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineVirtualTrack** possède ces méthodes.



| Méthode                                                               | Description                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**SetTrackDirty**](iamtimelinevirtualtrack-settrackdirty.md)       | Non pris en charge.<br/>                         |
| [**TrackGetPriority**](iamtimelinevirtualtrack-trackgetpriority.md) | Récupère le niveau de priorité de l’objet.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
