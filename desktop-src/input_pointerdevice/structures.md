---
description: Les rubriques de cette section fournissent les spécifications de référence pour les structures de pile d’entrée de périphérique pointeur.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Structures (point d’entrée de périphérique pointeur)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 042e1582d9c01cc6779ad672fb4935d288d29d8f442011d88e2b967b6adcf50a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830269"
---
# <a name="pointer-device-input-stack-structures"></a>Structures de pile d’entrée de périphérique pointeur

Les rubriques de cette section fournissent les spécifications de référence pour les structures de [pile d’entrée de périphérique pointeur](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [**POINTER_DEVICE_CURSOR_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | Contient les mappages d’ID de curseur pour les périphériques de pointeurs.<br/> |
| [**POINTER_DEVICE_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | Contient des informations sur un dispositif de pointage. Un tableau de ces structures est retourné à partir de la fonction [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) . Une structure unique est retournée à partir d’un appel à la fonction [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) . <br/> |
| [**POINTER_DEVICE_PROPERTY**](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | Contient les propriétés de l’appareil (HID) éléments globaux qui correspondent aux utilisations HID.<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Référence de pile d’entrée de périphérique pointeur](unified-input-stack-reference.md)
