---
description: L’interface IAMTimelineTrack fournit des méthodes pour manipuler les objets Track dans les services de modification DirectShow (DES). Une piste contient une liste de sources qui sont rendues dans la sortie finale.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interface IAMTimelineTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534901"
---
# <a name="iamtimelinetrack-interface"></a>Interface IAMTimelineTrack

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineTrack` interface fournit des méthodes pour manipuler des objets *Track* dans les [services de modification DirectShow](directshow-editing-services.md) (des).

Une piste contient une liste de sources qui sont rendues dans la sortie finale. Les sources au sein d’une même piste peuvent ne pas se chevaucher. Les pistes vidéo peuvent avoir des effets et des transitions. Le moteur de rendu applique des effets avant d’appliquer des transitions. Les pistes audio peuvent avoir des effets, mais pas des transitions. Pour plus d’informations, consultez [le modèle Timeline](the-timeline-model.md).

Pour créer un objet Track, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la valeur Timeline \_ de \_ type principal \_ Track. Vous pouvez interroger le pointeur **IAMTimelineObj** retourné pour l' `IAMTimelineTrack` interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineTrack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrack** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineTrack** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Détermine si la piste est vide (ne contient aucun objet source).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Recherche la source suivante qui s’affiche à l’heure spécifiée ou une version ultérieure dans le suivi.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Recherche dans la piste la source suivante qui apparaît à l’heure spécifiée ou ultérieurement, avec le donné comme valeur [**REFTIME**](reftime.md) .<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Récupère la source suivante après la source spécifiée.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Récupère le nombre de sources dans la piste.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Récupère l’objet source le plus proche de l’heure spécifiée, sous la forme d’une valeur [**REFTIME**](reftime.md) .<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Fractionne tous les objets qui existent à l’heure spécifiée et insère un espace entre eux.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux, à l’aide des valeurs [**REFTIME**](reftime.md) .<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Non pris en charge.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Non pris en charge.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Ajoute une source à la piste.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Supprime tous les éléments de la piste entre les heures spécifiées.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Supprime tous les éléments de la piste entre les heures spécifiées, en fonction des valeurs [**REFTIME**](reftime.md) .<br/>                                |



 

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



 

 
