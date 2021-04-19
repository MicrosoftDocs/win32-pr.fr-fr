---
title: Présentation de WinEvents
description: Les applications serveur et le système d’exploitation utilisent WinEvents pour notifier les clients lorsqu’une modification se produit dans le système ou dans l’interface utilisateur.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511448"
---
# <a name="what-are-winevents"></a>Qu’est-ce que WinEvents ?

Les applications serveur et le système d’exploitation utilisent WinEvents pour notifier les clients lorsqu’une modification se produit dans le système ou dans l’interface utilisateur.

La prise en charge de WinEvent est une fonctionnalité du système d’exploitation Windows qui fournit les éléments suivants :

-   Méthode simple permettant aux clients de s’inscrire pour recevoir des notifications d’événements.
-   Mécanisme permettant d’injecter du code client dans des serveurs.
-   Routage des événements des serveurs vers les clients intéressés.
-   Génération automatique d’événements pour la plupart des contrôles basés sur **HWND**.

La génération d’événements pour les contrôles basés sur **HWND** est particulièrement importante pour les développeurs de serveurs. Le runtime Microsoft Active Accessibility fournit des proxies [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour tous les éléments d’interface utilisateur standard. De même, le système génère automatiquement le WinEvents approprié à chaque fois qu’il crée, détruit, déplace, redimensionne ou effectue toute autre action sur un contrôle basé sur **HWND**.

Certains WinEvents, y compris les événements **HWND** généraux, sont automatiquement pris en charge par le système. Les autres types de WinEvents, tels que les changements d’État ou les événements de sélection spécifiques à un contrôle particulier, sont pris en charge par les serveurs Microsoft Active Accessibility.

Lorsqu’un événement qui affecte l’interface utilisateur se produit, les serveurs peuvent diffuser une notification d’événements à tous les clients intéressés en appelant la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) . L’appel de fonction comprend des informations qui identifient le type d’événement qui s’est produit et l’élément d’interface utilisateur auquel s’applique l’événement. Les clients peuvent utiliser ces informations pour récupérer un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément d’interface utilisateur et collecter plus d’informations.

Par exemple, pour informer les clients que le nom d’un contrôle a été modifié, un serveur appelle [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) et passe l' [**objet d’événement \_ \_ NameChange,**](event-constants.md) dans le paramètre d’événement. Le système répond en déterminant quels clients sont inscrits pour recevoir cet événement particulier et appelle leur fonction de rappel inscrite. Si aucun client n’est inscrit pour l’événement, l’appel du serveur à **NotifyWinEvent** est comparable à une opération « aucune opération » et l’impact sur les performances est négligeable.

Les serveurs appellent [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour annoncer l’événement au système une fois que l’événement s’est produit. Ils ne doivent jamais notifier le système d’un événement avant que l’événement se produise.

Pour être informé des événements, les clients inscrivent des fonctions de raccordement de rappel à l’aide de [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Les clients définissent une seule fonction de raccordement pour tous les événements possibles ou plusieurs fonctions de raccordement pour des plages discrètes d’événements. Pour plus d’informations, consultez [inscription d’une fonction de raccordement](registering-a-hook-function.md).

Lorsque Microsoft Active Accessibility est averti d’un événement, il appelle toutes les fonctions de raccordement qui ont été inscrites pour cet événement, en transmettant les paramètres à partir de [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




