---
title: Considérations relatives à la conception des appareils personnalisés
description: Cette rubrique décrit les considérations de conception qui peuvent vous aider à déterminer si votre appareil a besoin d’un pilote personnalisé.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521812"
---
# <a name="design-considerations-for-custom-devices"></a>Considérations relatives à la conception des appareils personnalisés

Cette rubrique décrit les considérations de conception qui peuvent vous aider à déterminer si votre appareil a besoin d’un pilote personnalisé.

- [Détermination du type de pilote à implémenter](#determining-the-type-of-driver-to-implement)
- [Considérations relatives à la sécurité](#security-considerations)
- [Rubriques connexes](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Détermination du type de pilote à implémenter

ce tableau décrit les cas où vous devez développer un pilote personnalisé pour votre appareil et communiquer avec lui à l’aide de l’API d’accès à l’appareil, et quand vous devez utiliser des piles d’appareils Windows fournies à la place.

| Pour prendre en charge | Implémentation |
|:---|:---|
| Appareils bien connus, notamment : <ul><li>Capteur</li><li>Emplacement</li><li>Webcam</li><li>Proximité</li><li>SMS (Short Message Service)</li><li>Haut débit mobile</li></ul><br/> | pour de nombreux types d’appareils connus, vous n’avez pas besoin d’un pilote personnalisé, car Windows comprend des api et des interfaces de pilote de périphérique (DDIs) d’extension de classe qui gèrent la communication entre le pilote et Windows. les appareils capteur, emplacement et Windows périphérique Portable (WPD) sont des exemples de classes d’appareils qui prennent en charge cette prise en charge. si vous générez un pilote qui utilise l’un de ces DDIs fournis par Windows pour envoyer et recevoir des données et des commandes, il n’est pas nécessaire que votre application Windows Store utilise l’API d’accès de l’appareil pour répartir l’accès ou envoyer des codes de contrôle d’entrée/sortie (e/s) directement au pilote. <br/> quand une application Windows Store demande l’accès à un périphérique bien connu à l’aide de l’API Windows Runtime pour sa classe d’appareils, Windows 8 gère l’accès des appareils en fonction du type d’appareil. Les applications auront toujours accès à certains types d’appareils connus (tels que les accéléromètres) qui ne révèlent pas d’informations d’identification personnelle. D’autres types d’appareils connus doivent être déclarés dans le manifeste de l’application avant qu’une application puisse y accéder. L’utilisateur doit accorder à une application l’autorisation d’accéder aux appareils qui révèlent des informations sensibles, telles que l’emplacement, la webcam et les périphériques du microphone, ou peut coûter l’argent de l’utilisateur, comme les appareils haut débit mobile. <br/> |
| Appareil WPD qui implémente les services MTP.<br/> | Vous pouvez utiliser le pilote de classe MTP, ou vous pouvez générer un pilote à l’aide de l’interface DDI WPD.<br/> Windows 8 prend en charge les services d’appareil MTP. Une application peut utiliser l' [Windows. appareils. portable](/uwp/api/Windows.Devices.Portable) Windows Runtime api, l’api COM (component Object Model) du périphérique portable ou l’Automation WPD pour accéder à l’appareil. Votre application n’a pas besoin d’utiliser l’API d’accès à l’appareil.<br/> |
| un appareil qui n’a pas d’extension de classe ou de pilote de classe fourni par Windows.<br/>  | Dans ce cas, consultez les [applications d’appareil UWP pour](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) les appareils internes pour les appareils spécialisés afin de déterminer si vous devez implémenter un accès personnalisé aux pilotes à l’aide de l’API d’accès à l’appareil.<br/> |

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Les articles suivants fournissent des conseils pour l’écriture de code C++ sécurisé :

- [Meilleures pratiques de sécurité pour C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices Guide de sécurité pour les applications]/Previous-versions/MSP-n-p/ff650760 (v = pandp. 10))

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)
