---
description: La classe CMediaControl fournit la gestion de classe de base des méthodes IDispatch de l’IMediaControl à interface double. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869594"
---
# <a name="cmediacontrol-class"></a>CMediaControl, classe

![hiérarchie de la classe cmediacontrol](images/cutil02.png)

La `CMediaControl` classe fournit la gestion de classe de base des méthodes [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) de l' [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)à interface double. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface **IMediaControl** .

En règle générale, le gestionnaire de graphes de filtres est le seul objet qui implémente l’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . (les filtres implémentent l’interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , héritée par [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), pour recevoir des commandes de contrôle du gestionnaire de graphique de filtre.) Par conséquent, cette bibliothèque de classes est un usage limité pour filtrer les développeurs.

Les fonctions membres [**CMediaControl :: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl :: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl :: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)et [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) sont des implémentations standard des méthodes [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) à l’aide de la classe [**CBaseDispatch**](cbasedispatch.md) (et d’une bibliothèque de types) pour analyser les commandes et les passer aux méthodes virtuelles pures de l’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .

Les méthodes [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , définies dans Control. ODL, sont laissées comme des virtuels purs.



| Fonctions de membre                                           | Description                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Construit un objet **CMediaControl** .                                                                                                                                                                                                  |
| Méthodes IDispatch                                          | Description                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Mappe un membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (DISPID), qui peuvent être utilisés lors des appels suivants à la méthode [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) . |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Récupère le nombre d’interfaces d’informations de type fournies par un objet.                                                                                                                                                              |
| [**Appeler**](cmediacontrol-invoke.md)                     | Fournit l'accès aux propriétés et aux méthodes exposées par un objet.                                                                                                                                                                         |



 

 

 
