---
title: Communication client/serveur
description: Le mécanisme WinEvents permet aux serveurs de communiquer facilement avec les clients Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "106509235"
---
# <a name="clientserver-communication"></a>Communication client/serveur

Le mécanisme [winEvents](winevents-overview.md) permet aux serveurs de communiquer facilement avec les clients Microsoft Active Accessibility. Les clients recueillent souvent des informations en réagissant à WinEvents (par exemple, après le focus), mais ils sont libres de demander des informations à un serveur à tout moment.

Pour demander des informations pour un objet accessible qui génère un WinEvent, un client doit traiter l’événement et établir une connexion avec l’objet accessible approprié. Pour ce faire, le client effectue les six étapes suivantes :

-   Un serveur appelle [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour générer une notification WinEvent pour chaque modification apportée à ses éléments d’interface utilisateur.
-   Le code de gestion WinEvent dans l’utilisateur détermine si des applications clientes ont inscrit une [*fonction de hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent à l’aide de [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) et appelle la fonction de rappel inscrite.
-   Dans sa fonction de rappel, le client demande l’accès à l’objet qui a généré l’événement en appelant [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ou d’autres fonctions de récupération d’objet accessibles. Pour plus d’informations, consultez [récupération d’un objet IAccessible](retrieving-an-iaccessible-object.md).
-   Cette API Microsoft Active Accessibility envoie à l’application serveur [**un \_ message WM**](wm-getobject.md) pour récupérer l’objet accessible.
-   En réponse à la fonction « [**WM \_ GETOBJECT**](wm-getobject.md)», l’application serveur retourne la valeur zéro ou retourne une valeur qui agit comme une référence unique à l’objet qui a généré l’événement.
-   Si le serveur retourne la valeur zéro, Microsoft Active Accessibility crée un objet proxy et lui donne son adresse au client. Dans le cas contraire, Microsoft Active Accessibility utilise cette référence pour récupérer l’adresse d’une interface d’objet telle que [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou [**IDispatch**](idispatch-interface.md)et donne cette adresse au client.

Une fois que le client dispose d’une adresse d’interface, il peut appeler les propriétés et méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet accessible pour récupérer des informations.

## <a name="in-this-section"></a>Dans cette section

-   [WinEvents et Active Accessibility](winevents-overview.md)
-   [Fonctionnement de la fonction GETOBJECT de WM \_](how-wm-getobject-works.md)
-   [Récupération d’un objet IAccessible](retrieving-an-iaccessible-object.md)

 

 




