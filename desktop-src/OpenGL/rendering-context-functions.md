---
title: Rendu des fonctions de contexte
description: Cinq fonctions WGL gèrent les contextes de rendu, comme décrit dans le tableau suivant.
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- WGL, fonctions, contextes de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8d3a8ea0333154d3145711829ab23e262fa485
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941324"
---
# <a name="rendering-context-functions"></a>Rendu des fonctions de contexte

Cinq fonctions WGL gèrent les contextes de rendu, comme décrit dans le tableau suivant.



| WGL fonction)                                         | Description                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | Crée un nouveau contexte de rendu.                                                             |
| [**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | Définit le contexte de rendu actuel d’un thread.                                                   |
| [**WglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | Obtient un handle du contexte de rendu actuel d’un thread.                                    |
| [**WglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | Obtient un handle vers le contexte de périphérique associé au contexte de rendu actuel d’un thread. |
| [**WglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | Supprime un contexte de rendu.                                                                 |



 

La fonction [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) prend un handle de contexte de périphérique en tant que paramètre et retourne un handle de contexte de rendu. Le contexte de rendu créé est adapté au dessin sur l’appareil référencé par le handle de contexte de périphérique. En particulier, son format de pixel est le même que le format de pixel du contexte de périphérique. Après avoir créé un contexte de rendu, vous pouvez libérer ou supprimer le contexte de périphérique. Pour plus d’informations sur la création, l’obtention, le lancement et la suppression d’un contexte de périphérique, consultez [contextes de périphérique](/windows/desktop/gdi/device-contexts) .

> [!Note]  
> Le contexte de périphérique (Device Context) envoyé à [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) doit être un contexte de périphérique d’affichage, un contexte de périphérique de mémoire ou un contexte de périphérique d’imprimante couleur qui utilise quatre bits ou plus par pixel. Le contexte de périphérique ne peut pas être un contexte de périphérique d’imprimante monochrome.

 

La fonction [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) prend un handle de contexte de rendu et un handle de contexte de périphérique en tant que paramètres. Tous les appels OpenGL suivants effectués par le thread sont effectués par le biais de ce contexte de rendu et sont dessinés sur l’appareil référencé par ce contexte de périphérique. Le contexte de périphérique n’a pas besoin d’être le même que celui passé à **wglCreateContext** lorsque le contexte de rendu a été créé, mais il doit se trouver sur le même appareil et avoir le même format de pixel. L’appel à **wglMakeCurrent** crée une association entre le contexte de rendu fourni et le contexte de périphérique. Vous ne pouvez pas libérer ou supprimer le contexte de périphérique associé à un contexte de rendu actuel tant que vous n’avez pas effectué le contexte de rendu en cours.

Une fois qu’un thread a un contexte de rendu actuel, il peut effectuer des appels de graphiques OpenGL. Tous les appels doivent traverser un contexte de rendu. Rien ne se passe si vous effectuez des appels graphiques OpenGL à partir d’un thread qui ne dispose pas d’un contexte de rendu actuel.

La fonction [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) ne prend pas de paramètres et retourne un handle vers le contexte de rendu actuel du thread appelant. Si le thread n’a pas de contexte de rendu actuel, la valeur de retour est **null**.

Quand vous obtenez un handle vers le contexte de périphérique associé au contexte de rendu actuel d’un thread en appelant [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc), l’Association est créée lorsqu’un contexte de rendu devient actif.

Vous pouvez rompre l’association entre un contexte de rendu actuel et un thread en appelant [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) avec l’un des deux Handles suivants :

-   Handle de contexte de rendu **null**
-   Handle autre que celui appelé à l’origine

Après l’appel de [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) avec le paramètre de handle de contexte de rendu ayant la valeur **null**, le thread appelant n’a aucun contexte de rendu actuel. Le contexte de rendu est libéré de sa connexion au thread, et l’Association du contexte de rendu à un contexte de périphérique se termine. OpenGL vide toutes les commandes de dessin et peut libérer des ressources. Aucun dessin OpenGL ne sera effectué avant le prochain appel à **wglMakeCurrent**, car le thread ne peut pas effectuer d’appels de graphiques OpenGL tant qu’il n’a pas récupéré un contexte de rendu actuel.

La deuxième façon de rompre l’association entre un contexte de rendu et un thread consiste à appeler **wglMakeCurrent** avec un contexte de rendu différent. Après un tel appel, le thread appelant a un nouveau contexte de rendu actuel, le précédent contexte de rendu actuel est libéré de sa connexion au thread, et l’ancienne Association du contexte de rendu actuel à un contexte de périphérique se termine.

La fonction [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) accepte un seul paramètre, qui est le handle du contexte de rendu à supprimer. Avant d’appeler **wglDeleteContext**, rendez le contexte de rendu non actuel en appelant [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent), puis supprimez ou libérez le contexte de périphérique associé en appelant [DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) ou [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) , le cas échéant.

Un thread a une erreur pour supprimer un contexte de rendu qui est le contexte de rendu d’un autre thread. Toutefois, si un contexte de rendu est le contexte de rendu actuel du thread appelant, **wglDeleteContext** vide toutes les commandes de dessin OpenGL et rend le contexte de rendu inactif avant de le supprimer. Dans ce cas, si vous utilisez **wglDeleteContext** pour rendre un contexte de rendu non actuel, le programmeur doit supprimer ou libérer le contexte de périphérique associé.

 

 