---
description: La classe CBaseMediaFilter implémente l’interface IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: CBaseMediaFilter, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239243"
---
# <a name="cbasemediafilter-class"></a>CBaseMediaFilter, classe

![cbasemediafilter](images/filter05.png)

La `CBaseMediaFilter` classe implémente l’interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) . Utilisez cette classe pour les serveurs de distribution de plug-in ou d’autres objets qui doivent prendre en charge **IMediaFilter** sans prendre en charge l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . N’utilisez pas cette classe pour les filtres. Utilisez plutôt la classe [**CBaseFilter**](cbasefilter.md) , ou une classe de base dérivée de **CBaseFilter**.



| Variables membres protégées                                       | Description                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_État m**](cbasemediafilter-m-state.md)                     | État actuel de l’objet.                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | Pointeur vers l’horloge de référence de l’objet.                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | Temps de référence qui correspond au temps de flux 0.            |
| [**m \_ CLSID**](cbasemediafilter-m-clsid.md)                     | Identificateur de classe (CLSID) de l’objet.                      |
| [**m \_ pLock**](cbasemediafilter-m-plock.md)                     | Pointeur vers une section critique.                               |
| M&#233;thodes publiques                                                   | Description                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Méthode de constructeur.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Méthode de destructeur. Virtuels.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Récupère le temps de flux actuel. Virtuels.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Détermine si l’objet est actif (en cours d’exécution ou en pause). |
| IPersist, méthodes                                                 | Description                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Récupère l’identificateur de classe.                              |
| Méthodes IMediaFilter                                             | Description                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Définit une horloge de référence pour l’objet.                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Récupère l’horloge de référence utilisée par l’objet.      |
| [**Arrêter**](cbasemediafilter-stop.md)                            | Arrête l’objet.                                            |
| [**Suspendre**](cbasemediafilter-pause.md)                          | Suspend l’objet.                                           |
| [**Exécuter**](cbasemediafilter-run.md)                              | Exécute l’objet.                                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




