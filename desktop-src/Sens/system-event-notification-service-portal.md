---
description: Surveiller les notifications d’événements système à partir de programmes exécutés sur des ordinateurs portables pour déterminer la bande passante et la latence de la connexion réseau. Écrire des applications optimisées pour l’informatique mobile et les réseaux locaux à latence élevée.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Service de notification d’événements système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013574"
---
# <a name="system-event-notification-service"></a>Service de notification d’événements système

## <a name="purpose"></a>Objectif

Les applications conçues pour être utilisées par les utilisateurs mobiles nécessitent un ensemble unique de fonctions de connectivité et de notifications. Au passé, ces applications individuelles devaient implémenter ces fonctionnalités en interne. Le service de notification d’événements système (SENS) fournit maintenant ces fonctionnalités dans le système d’exploitation, créant une interface de notification et de connectivité uniforme pour les applications. L’utilisation de développeurs SENSe peut déterminer les informations de latence et de bande passante de connexion à partir de leur application et optimiser l’opération de l’application en fonction de ces conditions.

## <a name="where-applicable"></a>Le cas échéant

Les fonctions de connectivité et les notifications de SENS sont utiles pour les applications écrites pour des ordinateurs portables ou des ordinateurs connectés à des réseaux locaux à latence élevée.

## <a name="developer-audience"></a>Développeurs concernés

Ce document est destiné aux développeurs de logiciels qui développent des applications pour l’informatique mobile et des réseaux locaux à latence élevée. Ce document fournit une référence complète de toutes les parties du service de notification d’événements système, y compris l’objet SENS et les méthodes de prise en charge.

## <a name="run-time-requirements"></a>Conditions d’exécution

nécessite Microsoft Windows XP ou version ultérieure. Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une interface ou une fonction particulière, consultez la section Configuration requise de la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                              | Description                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Vue d'ensemble](about-system-event-notification-service.md)<br/> | Informations générales sur le service de notification d’événements système.<br/>               |
| [Référence](sens-reference.md)<br/>                         | Documentation des interfaces et méthodes du service de notification d’événements système.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
