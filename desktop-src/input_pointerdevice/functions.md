---
description: Les rubriques de cette section fournissent les spécifications de référence pour les fonctions de pile d’entrée de périphérique pointeur.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Fonctions (pile d’entrée de périphérique pointeur)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106541608"
---
# <a name="pointer-device-input-stack-functions"></a>Fonctions de pile d’entrée de périphérique pointeur

Les rubriques de cette section fournissent les spécifications de référence pour les fonctions de [pile d’entrée de périphérique pointeur](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configure l’appareil d’injection de pointeur pour l’application appelante et initialise le nombre maximal de pointeurs simultanés que l’application peut injecter.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Détruit l’appareil d’injection de pointeur spécifié.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Obtient des informations sur l’appareil du pointeur.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Obtient les ID de curseur mappés aux curseurs associés à un dispositif de pointage.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Obtient les propriétés de l’appareil qui ne sont pas incluses dans la structure des [**\_ \_ informations de périphérique du pointeur**](/previous-versions/windows/desktop/api) . <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Obtient la plage x et y pour l’appareil de pointeur (dans HIMETRIC) et la plage x et y (résolution actuelle) pour l’affichage auquel le périphérique pointeur est mappé. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Obtient des informations sur les périphériques de pointeurs attachés au système.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Obtient les données d’entrée brutes à partir de l’appareil du pointeur. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simule l’entrée de pointeur (stylet ou tactile).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Inscrit une fenêtre pour traiter les notifications d’appareil [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)et de pointer [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) .<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Référence de pile d’entrée de périphérique pointeur](unified-input-stack-reference.md)
