---
title: Protection contre la réentrance dans les fonctions de raccordement
description: Lorsqu’une fonction de raccordement traite un événement, des événements supplémentaires peuvent être déclenchés, ce qui peut entraîner la réentrée de la fonction de raccordement avant la fin du traitement de l’événement d’origine.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519384"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Protection contre la réentrance dans les fonctions de raccordement

Lorsqu’une fonction de raccordement traite un événement, des événements supplémentaires peuvent être déclenchés, ce qui peut entraîner la réentrée de la fonction de raccordement avant la fin du traitement de l’événement d’origine. Le problème de la réentrance dans les fonctions de raccordement est que les événements sont terminés hors séquence, sauf si la fonction de raccordement gère cette situation.

Par exemple, considérez un cas où une fonction de raccordement dans un programme de lecture d’écran traite l’événement [**\_ \_ VALUECHANGE**](event-constants.md) de l’objet d’événement pour un contrôle d’édition. Si, lors du traitement du premier événement de modification de valeur, la fonction de raccordement est réentrée pour traiter un événement de modification de valeur subséquent, le deuxième événement est terminé avant le premier événement. Dans ce cas, le lecteur d’écran transmet des informations inexactes à l’utilisateur.

Étant donné que le traitement des événements est interrompu, des événements supplémentaires peuvent être reçus chaque fois que la fonction de raccordement appelle une fonction qui entraîne la vérification de la file d’attente de messages du thread propriétaire. Cela se produit quand l’un des éléments suivants est appelé dans la fonction de raccordement :

-   fonction Windows [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage), [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea), [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)ou [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   Microsoft Active Accessibility Functions [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou une autre propriété ou méthode com (Component Object Model) qui traverse les limites de processus

Étant donné que les fonctions de raccordement appellent les propriétés et les méthodes [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) et [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , il n’est pas possible d’empêcher la réentrance. La seule solution est que les développeurs de clients ajoutent du code dans la fonction de raccordement qui détecte la réentrance et prennent les mesures appropriées si la fonction de raccordement est réentrée.

 

 