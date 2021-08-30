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
ms.openlocfilehash: f9eba273793e97c5fb92fdabb365eb2402fc6feb6fbc571f1ec1ef1a0a4b3692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982769"
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



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
