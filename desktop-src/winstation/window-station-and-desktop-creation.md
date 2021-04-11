---
title: Station Windows et création de bureau
description: Le système crée automatiquement la station Windows Interactive.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315143"
---
# <a name="window-station-and-desktop-creation"></a>Station Windows et création de bureau

Le système crée automatiquement la station Windows Interactive. Lorsqu’un utilisateur interactif se connecte, le système associe la station de fenêtre interactive à la session d’ouverture de session de l’utilisateur. Le système crée également le Bureau d’entrée par défaut pour la station Windows Interactive (Winsta0 \\ par défaut). Les processus démarrés par l’utilisateur connecté sont associés au \\ Bureau par défaut Winsta0.

Un processus peut utiliser la fonction [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) pour créer une nouvelle station Windows, et la fonction **CreateDesktop** ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) pour créer un nouveau bureau. Le nombre de postes de travail qui peuvent être créés est limité par la taille du segment de bureau du système. Pour plus d’informations, consultez [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Lorsqu’un processus non interactif comme une application de service tente de se connecter à une station Windows et qu’il n’existe pas de station Windows pour la session de connexion au processus, le système tente de créer une station Windows et un bureau pour la session. Le nom de la station de fenêtre créée est basé sur l’identificateur de session d’ouverture de session et le bureau est nommé par défaut, comme décrit ici :

-   Si un service s’exécute dans le contexte de sécurité du compte LocalSystem mais n’inclut pas l' \_ attribut processus interactif du service \_ , il utilise la station de Windows et le Bureau suivants : service-0x0-3E7 $ \\ default. Cette station Windows n’étant pas interactive, le service ne peut pas afficher une interface utilisateur. En outre, les processus créés par le service ne peuvent pas afficher une interface utilisateur.
-   Si le service s’exécute dans le contexte de sécurité d’un compte d’utilisateur, le nom de la station Windows est basé sur le SID d’utilisateur service-0x *Z1* - *Z2*$, où *Z1* est la partie haute du SID d’ouverture de session et *Z2* est la partie inférieure du SID d’ouverture de session. Étant donné qu’un SID est unique à la session de connexion, deux services exécutés dans le même contexte de sécurité reçoivent des stations de fenêtre uniques. Ces stations Windows ne sont pas interactives.

La liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) pour la station et le bureau Windows comprend les droits d’accès suivants pour le compte d’utilisateur du service :

Station Windows :

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
\_droits standard \_ requis  
</dl>

Bureau :

<dl> CREATEMENU de bureau \_  
Bureau \_ CREATEWINDOW  
énumération de postes de travail \_  
HOOKCONTROL de bureau \_  
READOBJECTS de bureau \_  
WRITEOBJECTS de bureau \_  
\_droits standard \_ requis  
</dl>

 

 