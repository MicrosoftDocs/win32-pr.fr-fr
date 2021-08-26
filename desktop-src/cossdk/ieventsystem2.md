---
description: Utilisé par le service de notification d’événements système (SENS) de Microsoft Internet Explorer pour accéder au magasin de données d’événements. Cette interface étend l’interface IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interface IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070599"
---
# <a name="ieventsystem2-interface"></a>Interface IEventSystem2

Utilisé par le service de notification d’événements système (SENS) de Microsoft Internet Explorer pour accéder au magasin de données d’événements. Cette interface étend l’interface [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .

## <a name="when-to-implement"></a>Quand implémenter

Vous n’avez pas besoin d’implémenter l’interface **IEventSystem2** . Un objet système d’événements fourni par le système (CLSID \_ CEventSystem) implémente **IEventSystem2**.

## <a name="when-to-use"></a>Quand l’utiliser

Si vous utilisez SENS, vous pouvez appeler les méthodes de **IEventSystem2** pour ajouter et supprimer des objets dans le magasin d’événements et pour obtenir des objets à partir du magasin d’événements.

Étant donné que [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) et l’objet du serveur de publication ne sont plus pris en charge, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) n’est pas appelé sur la méthode [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .

## <a name="members"></a>Membres

L’interface **IEventSystem2** hérite de **IEventSystem**. **IEventSystem2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEventSystem2** possède ces méthodes.



| Méthode                                                                         | Description                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Récupère le numéro de version du système d’événements.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Vérifie l’existence de tous les abonnés temporaires dans le magasin de données.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

