---
title: Vue d’ensemble des gestes tactiles Windows
description: Cette section décrit les différents mouvements pris en charge par Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Tactile Windows, gestes
- mouvements, à propos de
- Tactile Windows, support hérité
- gestes, prise en charge héritée
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031530"
---
# <a name="windows-touch-gestures-overview"></a>Vue d’ensemble des gestes tactiles Windows

Cette section décrit les différents mouvements pris en charge par Windows Touch.

## <a name="gestures-overview"></a>Vue d’ensemble des mouvements

La fonction tactile Windows active plusieurs mouvements qui prennent en charge des contacts uniques et multiples. L’illustration suivante montre les différents mouvements pris en charge dans Windows 7.

![Illustration montrant les gestes pris en charge par Windows Touch dans Windows 7](images/gestures.png)

> [!Note]  
> Certains module de reconnaissance sont plus fiables pour interpréter les gestes avec plusieurs contacts quand les contacts sont plus éloignés l’un de l’autre.

## <a name="legacy-support"></a>Prise en charge héritée

Pour la prise en charge héritée, le gestionnaire de mouvements par défaut mappe certains mouvements aux messages Windows utilisés dans les versions précédentes de Windows. Le tableau suivant décrit la façon dont les gestes sont mappés aux messages hérités.

| Mouvement        | Description  | Message (s) généré (s)              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Panoramique            | Le mouvement de panoramique est mappé à à l’aide de la roulette de défilement.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Appuyer et maintenir enfoncé | Le mouvement appuyer et maintenir est mappé à un clic droit sur la souris.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | Le mouvement de zoom déclenche des messages similaires au maintien de la touche CTRL et en faisant tourner la roulette de la souris. | **WM_MOUSEWHEEL** avec **MK_CONTROL** défini dans *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interprétation des gestes tactiles Windows

Les gestes tactiles Windows peuvent être interprétés par les développeurs d’applications en gérant le message [**WM_GESTURE**](wm-gesture.md) à partir de la fonction WndProc d’une application. Après avoir géré ce message, vous pouvez récupérer une structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) qui décrit le mouvement. La structure **GESTUREINFO** aura des informations assorties qui dépendent du type de mouvement.

La structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) est récupérée en passant le descripteur à la structure d’informations de mouvement à la fonction [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) .

Les indicateurs suivants indiquent les différents États des mouvements et sont stockés dans *dwFlags*. 

| Nom        | Valeur      | Description                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Un mouvement démarre.           |
| GF_INERTIA | 0x00000002 | Un mouvement a déclenché l’inertie. |
| GF_END     | 0x00000004 | Un mouvement est terminé.          |

> [!Note]  
> La plupart des applications doivent ignorer les **GID_BEGIN** et **GID_END** et les transmettre à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Ces messages sont utilisés par le gestionnaire de mouvements par défaut. Le comportement de l’application n’est pas défini lorsque les messages **GID_BEGIN** et **GID_END** sont consommés par une application tierce.

Le tableau suivant indique les différents identificateurs des mouvements. 

| Nom              | Valeur | Description                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Un mouvement démarre.      |
| GID_END          | 2     | Un geste se termine.        |
| GID_ZOOM         | 3     | Mouvement de zoom.           |
| GID_PAN          | 4     | Mouvement de panoramique.            |
| GID_ROTATE       | 5     | Mouvement de rotation.       |
| GID_TWOFINGERTAP | 6     | Mouvement TAP à deux doigts. |
| GID_PRESSANDTAP  | 7     | Mouvement d’appui et de pression.  |

> [!Note]  
> Le mouvement de **GID_PAN** a un inertie intégré. À la fin d’un mouvement de panoramique, des messages de mouvement de panoramique supplémentaires sont créés par le système d’exploitation.

Les membres de la structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** et **ullArguments** spécifient un point (à l’aide de la structure **points** ) et des informations supplémentaires sur les gestes en fonction du mouvement. Le tableau suivant répertorie les valeurs associées à chaque type de mouvement.

| ID de mouvement            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indique la distance entre les deux points.            | Indique le centre du zoom.   |
| **GID_PAN**          | Indique la distance entre les deux points.            | Indique la position actuelle du panoramique.                    |
| **GID_ROTATE**       | Indique l’angle de rotation si l’indicateur de **GF_BEGIN** est défini. Dans le cas contraire, il s’agit de la modification d’angle depuis le début de la rotation. Cela est signé pour indiquer la direction de la rotation. Utilisez les macros [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) et [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) pour récupérer et définir la valeur d’angle. | Cela indique le centre de la rotation qui est le point fixe autour duquel l’objet cible est pivoté. |
| **GID_TWOFINGERTAP** | Indique la distance entre les deux doigts.           | Indique le Centre des deux doigts.                      |
| **GID_PRESSANDTAP**  | Indique le delta entre le premier doigt et le deuxième doigt. Cette valeur est stockée dans une structure de **points** dans les 32 bits inférieurs du membre *ullArguments* .                        | Indique la position de la première partie du doigt.   |

## <a name="related-topics"></a>Rubriques connexes

[Gestes tactiles Windows](guide-multi-touch-gestures.md)