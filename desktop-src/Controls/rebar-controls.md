---
title: À propos des contrôles Rebar
description: Un contrôle rebar agit comme un conteneur pour les fenêtres enfants.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031963"
---
# <a name="about-rebar-controls"></a>À propos des contrôles Rebar

Un *contrôle rebar* agit comme un conteneur pour les fenêtres enfants. Elle peut contenir une ou plusieurs *bandes*, et chaque bande peut avoir n’importe quelle combinaison d’une barre de redimensionnement, d’une image bitmap, d’une étiquette de texte et d’une fenêtre enfant. Une application assigne une fenêtre enfant, généralement un autre contrôle, à une bande de contrôle rebar. Lorsque vous repositionnez dynamiquement une bande de contrôle rebar, le contrôle rebar gère la taille et la position de la fenêtre enfant assignée à cette bande. En outre, une application peut spécifier une image bitmap d’arrière-plan pour une bande, et le contrôle rebar affiche la fenêtre enfant de la bande sur l’image bitmap.

La capture d’écran suivante montre un contrôle rebar avec deux bandes. L’un contient une barre d’outils, tandis que l’autre contient une zone de liste déroulante. Les deux bandes ont un pince qui leur permet d’être déplacées et redimensionnées.

![capture d’écran de la boîte de dialogue montrant un contrôle rebar avec une bande contenant une barre d’outils et une bande contenant une zone de liste déroulante](images/rb-rebar.png)

> [!Note]  
> Le contrôle rebar est implémenté dans la version 4,70 et les versions ultérieures de Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Bandes rebar et fenêtres enfants

Une application définit les caractéristiques d’une bande rebar à l’aide des messages [**RB \_ INSERTBAND**](rb-insertband.md) et [**RB \_ SETBANDINFO**](rb-setbandinfo.md) . Ces messages acceptent l’adresse d’une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) comme paramètre *lParam* . Les membres de la structure **REBARBANDINFO** définissent les caractéristiques d’une bande donnée. Pour définir les caractéristiques d’une bande, définissez le membre **cbSize** pour indiquer la taille de la structure en octets. Ensuite, définissez le membre **fmask** pour indiquer les membres de structure que votre application remplit.

Pour assigner une fenêtre enfant à une bande, incluez l' \_ indicateur enfant RBBIM dans le membre **fmask** de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , puis définissez le membre **hwndChild** sur le handle de la fenêtre enfant. Les applications peuvent définir la largeur et la hauteur minimales autorisées d’une fenêtre enfant dans les membres **cxMinChild** et **cyMinChild** .

Lorsqu’un contrôle rebar est détruit, il détruit toutes les fenêtres enfants affectées aux bandes qu’il contient. Pour empêcher le contrôle de détruire les fenêtres enfants affectées à ses bandes, supprimez les bandes en envoyant le message [**RB \_ DELETEBAND**](rb-deleteband.md) , puis utilisez le message [**RB \_ SetParent,**](rb-setparent.md) pour réinitialiser le parent à une autre fenêtre avant de détruire le contrôle rebar.

## <a name="the-rebar-control-user-interface"></a>Interface utilisateur du contrôle rebar

Toutes les bandes de contrôle rebar peuvent être redimensionnées, à l’exception de celles qui utilisent le \_ style RBBS FIXEDSIZE. Pour redimensionner ou modifier l’ordre des bandes dans le contrôle, cliquez et faites glisser la barre de redimensionnement d’une bande. Le contrôle rebar se redimensionne et repositionne automatiquement les fenêtres enfants assignées à ses bandes. En outre, vous pouvez basculer la taille d’une bande en cliquant sur le texte de la bande, le cas échéant.

## <a name="the-rebar-controls-image-list"></a>Liste d’images du contrôle rebar

Si une application utilise une liste d’images avec un contrôle rebar, elle doit envoyer le message [**RB \_ SETBARINFO**](rb-setbarinfo.md) avant d’ajouter des bandes au contrôle. Ce message accepte l’adresse d’une structure [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) comme paramètre *lParam* . Avant d’envoyer le message, préparez la structure **REBARINFO** en définissant le membre **cbSize** sur la taille de la structure en octets. Ensuite, si le contrôle rebar affiche des images sur les bandes, définissez le membre **fmask** sur l' \_ indicateur IMAGELIST RBIM et attribuez un handle de liste d’images au membre **himl** . Si le rebar n’utilise pas d’images de bande, définissez **fmask** sur zéro.

## <a name="rebar-control-message-forwarding"></a>Transfert de messages de contrôle rebar

Un contrôle rebar transfère tous les messages de fenêtre de [**\_ notification WM**](wm-notify.md) à sa fenêtre parente. En outre, un contrôle rebar transfère tous les messages qui lui sont envoyés à partir de fenêtres affectées à ses bandes, comme [**WM \_ CHARTOITEM**](wm-chartoitem.md), la [**\_ commande WM**](/windows/desktop/menurc/wm-command)et d’autres.

 

 