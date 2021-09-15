---
title: À propos des entrées brutes
description: Cette rubrique décrit les entrées utilisateur à partir d’appareils tels que les manettes, les écrans tactiles et les microphones.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- entrée d’utilisateur, entrée brute
- capture de l’entrée utilisateur, entrée brute
- entrée brute
- inscription d’une entrée brute
- lecture d’une entrée brute
- entrée brute de manette de jeu
- entrée brute de l’écran tactile
- entrée de microphone RAW
- Périphérique d’interface utilisateur (HID)
- HID (périphérique d’interface utilisateur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3535e5601ec63a254c76060611999a1a2f08aeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520009"
---
# <a name="about-raw-input"></a>À propos des entrées brutes

Il existe de nombreux périphériques d’entrée utilisateur à côté du clavier et de la souris traditionnels. Par exemple, l’entrée d’utilisateur peut provenir d’une manette de jeu, d’un écran tactile, d’un microphone ou d’autres périphériques qui offrent une grande flexibilité en entrée d’utilisateur. Ces appareils sont collectivement appelés périphériques d’interface utilisateur (HIDs). L’API d’entrée brute offre un moyen stable et fiable pour les applications d’accepter une entrée brute à partir de n’importe quel HID, y compris le clavier et la souris.

Cette section couvre les sujets suivants :

-   [Modèle d’entrée brut](#raw-input-model)
-   [Inscription pour une entrée brute](#registration-for-raw-input)
-   [Lecture d’une entrée brute](#reading-raw-input)

## <a name="raw-input-model"></a>Modèle d’entrée brut

Auparavant, le clavier et la souris généraient généralement des données d’entrée. Le système a interprété les données provenant de ces appareils de manière à éliminer les détails spécifiques au périphérique des informations brutes. Par exemple, le clavier génère le code d’analyse spécifique à l’appareil, mais le système fournit une application avec le code de la touche virtuelle. En plus de masquer les détails de l’entrée brute, le gestionnaire de fenêtres ne prenait pas en charge tous les nouveaux HIDs. Pour obtenir une entrée du HIDs non pris en charge, une application doit effectuer de nombreuses opérations : ouvrir l’appareil, gérer le mode partagé, lire régulièrement l’appareil ou configurer le port de terminaison d’e/s, etc. Le modèle d’entrée brut et les API associées ont été développés pour permettre un accès simple aux entrées brutes à partir de tous les périphériques d’entrée, y compris le clavier et la souris.

le modèle d’entrée brut est différent du modèle d’entrée d’origine Windows pour le clavier et la souris. Dans le modèle d’entrée d’origine, une application reçoit une entrée indépendante du périphérique sous la forme de messages envoyés ou publiés dans son Windows, tels que [**WM \_ char**](wm-char.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)et [**WM \_ APPCOMMAND**](wm-appcommand.md). En revanche, pour les entrées brutes, une application doit inscrire les périphériques à partir desquels elle souhaite obtenir des données. En outre, l’application obtient l’entrée brute via le message [**\_ d’entrée WM**](wm-input.md) .

Le modèle d’entrée brut présente plusieurs avantages :

-   Une application n’a pas besoin de détecter ni d’ouvrir le périphérique d’entrée.
-   Une application obtient les données directement à partir de l’appareil et traite les données en ce qui concerne leurs besoins.
-   Une application peut distinguer la source de l’entrée même si elle provient du même type de périphérique. Par exemple, deux souris.
-   Une application gère le trafic de données en spécifiant des données à partir d’une collection de périphériques ou uniquement de types d’appareils spécifiques.
-   Les périphériques HID peuvent être utilisés lorsqu’ils sont disponibles sur la place de marché, sans attendre que de nouveaux types de messages ou un système d’exploitation mis à jour aient de nouvelles commandes dans [**WM \_ APPCOMMAND**](wm-appcommand.md).

Notez que le [**WM \_ APPCOMMAND**](wm-appcommand.md) fournit pour certains périphériques HID. Toutefois, le **WM \_ APPCOMMAND** est un événement d’entrée indépendant du périphérique de niveau supérieur, tandis que l' [**\_ entrée WM**](wm-input.md) envoie des données brutes de niveau faible qui sont spécifiques à un appareil.

## <a name="registration-for-raw-input"></a>Inscription pour une entrée brute

Par défaut, aucune application ne reçoit d’entrée brute. Pour recevoir une entrée brute d’un appareil, une application doit inscrire l’appareil.

Pour inscrire des appareils, une application crée tout d’abord un tableau de structures [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) qui spécifient la [collection de niveau supérieur](/windows-hardware/drivers/hid/top-level-collections) (CCM) pour les périphériques dont elle a besoin. La CCM est définie par une [page d’utilisation](/windows-hardware/drivers/hid/hid-usages#usage-page) (la classe de l’appareil) et un [ID d’utilisation](/windows-hardware/drivers/hid/hid-usages#usage-id) (l’appareil dans la classe). Par exemple, pour obtenir le clavier CCM, définissez UsagePage = 0x01 et UsageID = 0x06. L’application appelle [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) pour inscrire les appareils.

Notez qu’une application peut inscrire un appareil qui n’est pas actuellement attaché au système. lorsque cet appareil est attaché, le gestionnaire de Windows envoie automatiquement l’entrée brute à l’application. Pour récupérer la liste des périphériques d’entrée bruts sur le système, une application appelle [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). À l’aide de *hDevice* à partir de cet appel, une application appelle [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) pour récupérer les informations de l’appareil.

Par le biais du membre **dwFlags** de [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice), une application peut sélectionner les appareils à écouter, ainsi que ceux qu’elle souhaite ignorer. Par exemple, une application peut demander une entrée à partir de tous les appareils de téléphonie, à l’exception des ordinateurs de réponse. Pour obtenir un exemple de code, consultez [inscription pour une entrée brute](using-raw-input.md).

Notez que la souris et le clavier sont également HID, donc les données qu’ils contiennent peuvent être transmises à la fois à l' [**\_ entrée WM**](wm-input.md) du message HID et à celles des messages classiques. Une application peut sélectionner l’une ou l’autre méthode par la sélection appropriée des indicateurs dans [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice).

Pour connaître l’état d’inscription d’une application, appelez [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) à tout moment.

## <a name="reading-raw-input"></a>Lecture d’une entrée brute

Une application reçoit une entrée brute de tout HID dont la [collection de niveau supérieur](/windows-hardware/drivers/hid/top-level-collections) (CCM) correspond à un CCM de l’enregistrement. Lorsqu’une application reçoit une entrée brute, sa file d’attente de messages reçoit un message [**\_ d’entrée WM**](wm-input.md) et l’indicateur d’état de la file d’attente **QS \_ RAWINPUT** est défini (l'**\_ entrée QS** comprend également cet indicateur). Une application peut recevoir des données lorsqu’elle est au premier plan et lorsqu’elle est en arrière-plan.

Il existe deux façons de lire les données brutes : la méthode non mise en mémoire tampon (ou la méthode standard) et la méthode mise en mémoire tampon. La méthode unbufferd obtient les données brutes d’une structure [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) à la fois et convient à de nombreux HIDS. Ici, l’application appelle [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) pour recevoir le [**message \_ d’entrée WM**](wm-input.md) . L’application appelle ensuite [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) à l’aide du handle **RAWINPUT** contenu dans l' **\_ entrée WM**. Pour obtenir un exemple, consultez [réalisation d’une lecture standard d’une entrée brute](using-raw-input.md).

En revanche, la méthode mise en mémoire tampon obtient un tableau de structures [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) à la fois. Elle est fournie pour les appareils qui peuvent générer de grandes quantités d’entrées brutes. Dans cette méthode, l’application appelle [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) pour récupérer un tableau de structures **RAWINPUT** . Notez que la macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) est utilisée pour parcourir un tableau de structures **RAWINPUT** . Pour obtenir un exemple, consultez [réalisation d’une lecture de données brutes en mémoire tampon](using-raw-input.md).

Pour interpréter l’entrée brute, des informations détaillées sur le HID sont requises. Une application obtient les informations de l’appareil en appelant [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) avec le handle de l’appareil. Ce descripteur peut provenir d’une [**\_ entrée WM**](wm-input.md) ou du membre **hDevice** de [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader).