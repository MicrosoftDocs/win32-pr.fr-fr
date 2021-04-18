---
title: À propos de l’API d’accès aux appareils
description: L’API d’accès aux appareils est destinée aux développeurs C++ qui créent une application du Windows Store pour interagir avec des appareils spécialisés dans Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316728"
---
# <a name="about-the-device-access-api"></a>À propos de l’API d’accès aux appareils

L’API d’accès aux appareils est destinée aux développeurs C++ qui créent une application du Windows Store pour interagir avec des appareils spécialisés dans Windows 8. Cette rubrique décrit les scénarios auxquels s’applique l’API d’accès à l’appareil. Elle explique également comment l’API d’accès aux appareils applique des règles de sécurité pour les applications du Windows Store dans Windows 8.

- [Activation des fonctionnalités d’appareil personnalisées dans les applications d’appareils du Windows Store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Activation des fonctionnalités d’appareil personnalisées dans les applications d’appareils du Windows Store

Les développeurs pour les fabricants de matériel indépendants (IHV) et les OEM peuvent créer une application du Windows Store couplée avec leur appareil et acquise automatiquement lors de l’installation de l’appareil. Cette application, appelée application d’appareil du Windows Store, peut fournir une fonctionnalité d’appareil unique.

Les appareils qui n’ont pas de pilotes de classe intégrés ou de Windows Runtime API pour communiquer avec l’appareil dans Windows 8 sont appelés *appareils spécialisés*. Ces appareils peuvent nécessiter un pilote personnalisé. Pour plus d’informations sur les types d’appareils qui requièrent des pilotes personnalisés, consultez le Guide de conception des applications pour appareils Windows Store pour les appareils spécialisés.

L’application d’appareil Windows Store pour un appareil spécialisé qui doit communiquer avec le pilote personnalisé d’un appareil ne peut pas utiliser les API Microsoft Win32 comme [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) et [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) pour envoyer des IOCTL à l’appareil. L’environnement de sécurité restreint dans lequel s’exécutent les applications pour appareils Windows Store nécessite que vous utilisiez l’API d’accès à l’appareil pour communiquer avec votre pilote personnalisé à partir d’une application du Windows Store.

Le développeur d’un appareil personnalisé restreint l’accès aux applications approuvées et privilégiées. Par exemple, le fabricant d’un appareil Media Player peut souhaiter que les utilisateurs lisent uniquement de la musique par le biais de l’application musicale fournie par IHV et limitent l’application de tous les concurrents à la synchronisation des médias de l’appareil. Lorsque vous créez le pilote de périphérique, vous définissez une propriété dans le fichier INF (INF), spécifiez que seules les applications privilégiées peuvent accéder à l’appareil. Les métadonnées sur l’appareil lui-même spécifient les ID de package pour l’ensemble des applications approuvées. Pour plus d’informations sur le processus de définition de ces métadonnées sur votre appareil, consultez [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) .

## <a name="related-topics"></a>Rubriques connexes

[Exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications pour appareils UWP pour appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)