---
title: Entrée brute
description: Cette section décrit comment le système fournit une entrée brute à votre application et comment une application reçoit et traite cette entrée.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows Interface utilisateur, entrée utilisateur
- Windows Interface utilisateur, entrée brute
- entrée d’utilisateur, entrée brute
- capture de l’entrée utilisateur, entrée brute
- entrée brute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e26d67f2b014ce22c2d01cb4738cca4e041c59e417a216f0d75ffef6e6e4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482755"
---
# <a name="raw-input"></a>Entrée brute

Cette section décrit comment le système fournit une entrée brute à votre application et comment une application reçoit et traite cette entrée. L’entrée brute est parfois appelée entrée générique.

### <a name="in-this-section"></a>Dans cette section



| Nom                                           | Description                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [À propos des entrées brutes](about-raw-input.md)         | Décrit l’entrée utilisateur à partir d’appareils tels que les manettes, les écrans tactiles et les microphones.<br/> |
| [Utilisation des entrées brutes](using-raw-input.md)         | Fournit un exemple de code pour les tâches relatives à l’entrée brute.<br/>                                |
| [Référence d’entrée brute](raw-input-reference.md) | Contient la référence de l’API.<br/>                                                          |



 

### <a name="functions"></a>Fonctions



| Nom                                                                 | Description                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Appelle la procédure d’entrée brute par défaut pour fournir le traitement par défaut des messages d’entrée bruts qu’une application ne traite pas. Cette fonction garantit que chaque message est traité. [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) est appelé avec les mêmes paramètres que ceux reçus par la procédure de fenêtre. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Effectue une lecture en mémoire tampon des données d’entrée brutes.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Obtient l’entrée brute du périphérique spécifié.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Obtient des informations sur l’appareil d’entrée brut.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Énumère les périphériques d’entrée bruts attachés au système. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Obtient les informations sur les périphériques d’entrée bruts pour l’application actuelle.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Inscrit les appareils qui fournissent les données d’entrée brutes.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macros



| Nom                                                            | Description                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ le \_ wParam de code RAWINPUT \_**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Obtient le code d’entrée de *wParam* dans l' [**\_ entrée WM**](wm-input.md).<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Obtient l’emplacement de la structure suivante dans un tableau de structures [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) . <br/> |



 

### <a name="notifications"></a>Notifications



| Nom                                                        | Description                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_entrée WM**](wm-input.md)                               | Envoyé à la fenêtre qui obtient l’entrée brute. <br/>            |
| [**modification de l' \_ appareil d’entrée WM \_ \_**](wm-input-device-change.md) | Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute. <br/> |



 

### <a name="structures"></a>Structures



| Nom                                                            | Description                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Décrit le format de l’entrée brute à partir d’un périphérique d’interface utilisateur (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contient l’entrée brute d’un appareil. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Définit des informations pour les périphériques d’entrée bruts. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contient des informations sur un périphérique d’entrée brut.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contient les informations d’en-tête qui font partie des données d’entrée brutes. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contient des informations sur l’état du clavier. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contient des informations sur l’état de la souris. <br/>                         |
| [**\_informations sur l’appareil RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Définit les données d’entrée brutes provenant de n’importe quel appareil. <br/>                         |
| [**\_ \_ HID informations sur l’appareil RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Définit les données d’entrée brutes provenant du HID spécifié. <br/>                  |
| [**\_ \_ clavier informations sur l’appareil RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Définit les données d’entrée brutes provenant du clavier spécifié. <br/>             |
| [**\_souris d' \_ informations sur l’appareil RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Définit les données d’entrée brutes provenant de la souris spécifiée.<br/>                 |



 

 

