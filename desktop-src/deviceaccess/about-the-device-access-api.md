---
title: À propos de l’API d’accès aux appareils
description: l’API d’accès aux appareils est destinée aux développeurs C++ qui créent une application Windows Store pour interagir avec des appareils spécialisés dans Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521828"
---
# <a name="about-the-device-access-api"></a>À propos de l’API d’accès aux appareils

l’API d’accès aux appareils est destinée aux développeurs C++ qui créent une application Windows Store pour interagir avec des appareils spécialisés dans Windows 8. Cette rubrique décrit les scénarios auxquels s’applique l’API d’accès à l’appareil. elle explique également comment l’API d’accès aux appareils applique des règles de sécurité pour les applications Windows Store dans Windows 8.

- [activation des fonctionnalités d’appareil personnalisées dans Windows stocker des applications d’appareil](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>activation des fonctionnalités d’appareil personnalisées dans Windows stocker des applications d’appareil

les développeurs pour les fabricants de matériel indépendants (ihv) et les oem peuvent créer une application Windows Store couplée avec leur appareil et acquise automatiquement lors de l’installation de l’appareil. cette application, appelée application de l’appareil de stockage Windows, peut fournir une fonctionnalité d’appareil unique.

les appareils qui n’ont pas de pilotes de classe intégrés ou de Windows Runtime api pour communiquer avec l’appareil dans Windows 8 sont appelés *appareils spécialisés*. Ces appareils peuvent nécessiter un pilote personnalisé. pour plus d’informations sur les types d’appareils qui requièrent des pilotes personnalisés, consultez le guide de conception d’application d’appareil Windows Store pour les appareils spécialisés.

l’application d’appareil Windows Store pour un appareil spécialisé qui doit communiquer avec le pilote personnalisé d’un appareil ne peut pas utiliser les api Microsoft Win32 comme [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) et [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) pour envoyer des ioctl à l’appareil. l’environnement de sécurité restreint dans lequel les applications de l’appareil Windows Store s’exécute nécessitent que vous utilisiez l’API d’accès à l’appareil pour communiquer avec votre pilote personnalisé à partir d’une application Windows Store.

Le développeur d’un appareil personnalisé restreint l’accès aux applications approuvées et privilégiées. Par exemple, le fabricant d’un appareil Media Player peut souhaiter que les utilisateurs lisent uniquement de la musique par le biais de l’application musicale fournie par IHV et limitent l’application de tous les concurrents à la synchronisation des médias de l’appareil. Lorsque vous créez le pilote de périphérique, vous définissez une propriété dans le fichier INF (INF), spécifiez que seules les applications privilégiées peuvent accéder à l’appareil. Les métadonnées sur l’appareil lui-même spécifient les ID de package pour l’ensemble des applications approuvées. Pour plus d’informations sur le processus de définition de ces métadonnées sur votre appareil, consultez [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) .

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)