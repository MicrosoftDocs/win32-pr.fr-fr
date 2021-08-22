---
description: Une application obtient un DC d’affichage en appelant la fonction BeginPaint, GetDC ou GetDCEx et en identifiant la fenêtre dans laquelle la sortie correspondante s’affiche.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Afficher les contextes de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761324"
---
# <a name="display-device-contexts"></a>Afficher les contextes de périphérique

Une application obtient un DC d’affichage en appelant la fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) et en identifiant la fenêtre dans laquelle la sortie correspondante s’affiche. En règle générale, une application obtient un contrôleur de domaine d’affichage uniquement lorsqu’il doit le dessiner dans la zone cliente. Toutefois, il est possible d’obtenir un [contexte de périphérique Windows](#window-device-contexts) en appelant la fonction [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) . Une fois l’application terminée, elle doit libérer le DC en appelant la fonction [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) ou [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Il existe cinq types de contrôleurs de contrôleur pour les affichages vidéo :

-   Classe
-   Courant
-   Privé
-   Fenêtre
-   Parent

## <a name="class-device-contexts"></a>Contextes de périphérique de classe

Les *contextes de périphérique de classe* sont pris en charge uniquement pour la compatibilité avec les versions 16 bits de Windows. Quand vous écrivez votre application, évitez d’utiliser le contexte de périphérique de la classe ; Utilisez un contexte de périphérique privé à la place.

## <a name="common-device-contexts"></a>Contextes de périphérique courants

Les *contextes de périphérique courants* affichent les contrôleurs de réseau qui sont conservés dans un cache spécial par le système. Les contextes de périphérique courants sont utilisés dans les applications qui effectuent des opérations de dessin peu fréquentes. Avant que le système retourne le handle de contrôleur de réseau, il initialise le contexte de périphérique courant avec les objets, les attributs et les modes par défaut. Toutes les opérations de dessin effectuées par l’application utilisent ces valeurs par défaut, sauf si l’une des fonctions GDI est appelée pour sélectionner un nouvel objet, modifier les attributs d’un objet existant ou sélectionner un nouveau mode.

Étant donné qu’il n’existe qu’un nombre limité de contextes d’appareil communs, une application doit les libérer une fois le dessin terminé. Lorsque l’application libère un contexte de périphérique courant, toute modification apportée aux données par défaut est perdue.

## <a name="private-device-contexts"></a>Contextes de périphérique privé

Les *contextes d’appareil privé* sont des contrôleurs de contrôle d’affichage qui, contrairement aux contextes de périphérique courants, conservent les modifications apportées aux données par défaut même après leur publication par une application. Les contextes d’appareil privé sont utilisés dans les applications qui effectuent de nombreuses opérations de dessin, telles que les applications de conception assistée par ordinateur (CAO), les applications de publication de bureau, les applications de dessin et de peinture, etc. Les contextes de périphérique privé ne font pas partie de la mémoire cache du système et ne doivent donc pas être libérés après utilisation. Le système supprime automatiquement un contexte de périphérique privé une fois que la dernière fenêtre de cette classe a été détruite.

Une application crée un contexte de périphérique privé en spécifiant tout d’abord le \_ style de classe de fenêtre CS OWNDC lorsqu’il initialise le membre **style** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) et appelle la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . (Pour plus d’informations sur les classes de fenêtre, consultez [classes de fenêtre](../winmsg/window-classes.md).)

Après la création d’une fenêtre avec le \_ style cs OWNDC, une application peut appeler la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) une fois pour obtenir un handle identifiant un contexte de périphérique privé. L’application peut continuer à utiliser ce handle (et le contrôleur de service associé) jusqu’à ce qu’il supprime la fenêtre créée avec cette classe. Toute modification apportée aux objets graphiques et à leurs attributs, ou aux modes graphiques, est conservée par le système jusqu’à ce que la fenêtre soit supprimée.

## <a name="window-device-contexts"></a>Contextes de périphérique Windows

Un *contexte de périphérique de fenêtre* permet à une application de dessiner n’importe où dans une fenêtre, y compris la zone non cliente. Les contextes de périphérique Windows sont généralement utilisés par les applications qui traitent les messages [**WM \_ NCPAINT**](wm-ncpaint.md) et [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) pour Windows avec des zones non clientes personnalisées. L’utilisation d’un contexte de périphérique Windows n’est pas recommandée à d’autres fins. Pour plus d’informations, consultez [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contextes de périphérique parent

Un *contexte de périphérique parent* permet à une application de réduire le temps nécessaire pour configurer la zone de découpage pour une fenêtre. Une application utilise généralement des contextes d’appareil parent pour accélérer le dessin des fenêtres de contrôle sans nécessiter un contexte de périphérique ou de classe privé. Par exemple, le système utilise des contextes de périphérique parent pour le bouton de commande et les contrôles d’édition. Les contextes de périphérique parent sont destinés à être utilisés uniquement avec les fenêtres enfants, jamais avec des fenêtres contextuelles ou de niveau supérieur. Pour plus d’informations, consultez [contextes de périphérique d’affichage parent](parent-display-device-contexts.md).

 

 
