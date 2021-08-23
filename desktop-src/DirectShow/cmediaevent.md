---
description: La classe CMediaEvent fournit l’implémentation de la classe de base des méthodes IDispatch du IMediaEvent à interface double. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 505a11b9a8d3c12586e25faa822b127e0b8bb636f6655eb617125a47fb84feaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832482"
---
# <a name="cmediaevent-class"></a>CMediaEvent, classe

![hiérarchie de la classe cmediaevent](images/cutil03.png)

La `CMediaEvent` classe fournit l’implémentation de la classe de base des méthodes **IDispatch** des [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)à deux interfaces. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface **IMediaEvent** .

La `CMediaEvent` classe fournit également l’implémentation de la classe de base de l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) qui dérive de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).

Les fonctions membres [**CMediaEvent :: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent :: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent :: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)et [**CMediaEvent :: Invoke**](cmediaevent-invoke.md) sont des implémentations standard de l’interface **IDispatch** à l’aide de la classe [**CBaseDispatch**](cbasedispatch.md) (et d’une bibliothèque de types) pour analyser les commandes et les passer aux méthodes virtuelles pures de l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .



| Fonctions de membre                                         | Description                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Construit un objet **CMediaEvent** .                                                                                                                                                          |
| Méthodes IDispatch                                        | Description                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Cartes un membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peuvent être utilisés lors des appels suivants à la méthode **IDispatch :: Invoke** . |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Récupère un objet d’informations de type, qui récupère les informations de type pour une interface.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Récupère le nombre d’interfaces d’informations de type fournies par un objet.                                                                                                                    |
| [**Appeler**](cmediaevent-invoke.md)                     | Fournit l'accès aux propriétés et aux méthodes exposées par un objet.                                                                                                                               |



 

 

 



