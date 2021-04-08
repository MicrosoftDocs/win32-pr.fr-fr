---
title: Réception d’erreurs pour les pointeurs d’interface IAccessible
description: Cette rubrique décrit les situations dans lesquelles vous pouvez recevoir une erreur pour un pointeur d’interface IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840430"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Réception d’erreurs pour les pointeurs d’interface IAccessible

Cette rubrique décrit les situations dans lesquelles vous pouvez recevoir une erreur pour un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Les fonctions **IAccessible** peuvent retourner des erreurs pour les pointeurs d’interface **IAccessible** lorsqu’un utilisateur ferme une application à laquelle l’objet appartient, ou si un utilisateur ignore un contrôle par le biais de l’interface utilisateur.

## <a name="user-closes-an-application"></a>L’utilisateur ferme une application

Si un utilisateur ferme l’application qui contient un objet sur lequel le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pointe, tous les appels futurs à cet objet retournent un code d’erreur. L’erreur, telle que **co \_ E \_ OBJNOTCONNECTED**, indique que l’objet n’existe plus. Cela s’applique à tous les pointeurs d’interface **IAccessible** .

## <a name="user-dismisses-a-control"></a>L’utilisateur ignore un contrôle

Si un utilisateur ignore un contrôle (par exemple, en appuyant sur un bouton de commande), les clients peuvent toujours appeler des méthodes et des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur cet objet, car l’objet n’a pas été libéré. Toutefois, les appels futurs recevront des messages d’erreur.

Cette situation s’applique aux fonctions et méthodes suivantes :

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible :: \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible :: \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




