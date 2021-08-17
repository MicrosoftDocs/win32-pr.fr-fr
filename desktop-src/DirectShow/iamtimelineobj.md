---
description: l’interface IAMTimelineObj fournit des méthodes permettant de manipuler des objets timeline dans des Services d’édition DirectShow.
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interface IAMTimelineObj (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428159"
---
# <a name="iamtimelineobj-interface"></a>Interface IAMTimelineObj

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineObj` interface fournit des méthodes permettant de manipuler des objets de chronologie dans des [Services d’édition DirectShow](directshow-editing-services.md) . Tous les objets Timeline implémentent cette méthode, y compris les objets source, Effect, transition, Track, Group et composition. Créez un objet Timeline en appelant la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .

## <a name="members"></a>Membres

L’interface **IAMTimelineObj** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineObj** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineObj** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Non pris en charge.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Arrondit les heures de début et de fin spécifiées aux limites de frame les plus proches.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Arrondit les heures de début et de fin spécifiées sous forme de valeurs [**REFTIME**](reftime.md) aux limites de frame les plus proches.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Non pris en charge.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Non pris en charge.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Non pris en charge.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Récupère l’identificateur généré de l’objet.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Non pris en charge.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Récupère l’état d’édition de l’objet (verrouillé ou déverrouillé).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Récupère l’État muet de l’objet.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Récupère la méthode setter de propriété de l’objet.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Récupère les heures de début et de fin de l’objet en tant que valeurs [**REFTIME**](reftime.md) .<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Récupère le sous-objet associé à cet objet.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Récupère le GUID du sous-objet associé à cet objet Timeline.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Récupère le GUID du sous-objet sous la forme d’une valeur **BSTR** .<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Détermine si le pointeur de sous-objet de l’objet a été défini.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Non pris en charge.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Récupère le type de l’objet.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Récupère les données persistantes définies par l’application.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Récupère l’identificateur défini par l’application de l’objet.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Récupère le nom défini par l’application de l’objet.<br/>                                                                            |
| [**Installez**](iamtimelineobj-remove.md)                         | Supprime cet objet de la chronologie, pour la réinsertion ailleurs.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Supprime définitivement cet objet de la chronologie, y compris les sous-objets et les enfants.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Non implémenté.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Non implémenté.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Définit l’état de modification de l’objet sur verrouillé ou déverrouillé.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Définit l’État muet de l’objet.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Définit la méthode setter de propriété de l’objet.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Définit les heures de début et de fin de l’objet par rapport à la chronologie.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Définit les heures de début et de fin de l’objet en tant que valeurs **REFTIME** .<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Non pris en charge.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Spécifie l’identificateur global unique (GUID) du sous-objet associé à cet objet.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Spécifie le GUID du sous-objet sous la forme d’une valeur **BSTR** .<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | Non pris en charge.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Définit les données persistantes définies par l’application.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Définit un identificateur défini par l’application pour l’objet.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Définit un nom défini par l’application pour l’objet.<br/>                                                                            |



 

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



 

 
