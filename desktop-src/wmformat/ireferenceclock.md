---
title: Interface IReferenceClock
description: L’interface IReferenceClock fournit l’accès à une horloge externe. Cette interface est fournie pour permettre la synchronisation de toutes les routines de rendu avec la même horloge. Cette interface peut être obtenue à partir d’un objet lecteur.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Format Windows Media de l’interface IReferenceClock
- Interface IReferenceClock format Windows Media, décrit
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511894"
---
# <a name="ireferenceclock-interface"></a>Interface IReferenceClock

L’interface **IReferenceClock** fournit l’accès à une horloge externe. Cette interface est fournie pour permettre la synchronisation de toutes les routines de rendu avec la même horloge.

Cette interface peut être obtenue à partir d’un objet lecteur.

## <a name="members"></a>Membres

L’interface **IReferenceClock** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReferenceClock** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IReferenceClock** possède ces méthodes.



| Méthode                                                   | Description                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | Non implémenté par ce kit de développement logiciel (SDK).<br/>                                   |
| [**AdviseTime**](ireferenceclock-advisetime.md)         | Demande une notification asynchrone qu’une heure s’est écoulée.<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | Récupère le temps de référence actuel.<br/>                          |
| [**Arrêter**](ireferenceclock-unadvise.md)             | Annule une demande de notification.<br/>                                |



 

## <a name="remarks"></a>Notes

Pour plus d’informations sur les autres interfaces qui peuvent être obtenues à l’aide de la méthode QueryInterface de cette interface, consultez objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> </dl>

 

