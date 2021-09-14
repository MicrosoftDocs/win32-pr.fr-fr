---
description: Exigences générales pour le développement d’applications
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Configuration générale requise pour le développement d’applications (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293795"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Configuration générale requise pour le développement d’applications (API WPD)

pour créer une application Windows des appareils mobiles, le kit de [développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads) doit être installé sur votre ordinateur. Les en-têtes et les bibliothèques nécessaires s’affichent dans la liste suivante.

-   PortableDeviceGuids. lib
-   PortableDevice. h
-   PortableDeviceTypes. h
-   PortableDeviceApi. h
-   Toutes les autres bibliothèques et en-têtes nécessaires à votre application pour utiliser ou afficher des fichiers multimédias.

Si votre application prend en charge les nouvelles interfaces de services d’appareils, elle inclura également un ou plusieurs des fichiers d’en-tête suivants.

-   AnchorSyncDeviceService. h
-   BridgeDeviceService. h
-   CalendarDeviceService. h
-   ContactDeviceService. h
-   DeviceServices. h
-   FullEnumSyncDeviceService. h
-   HintsDeviceService. h
-   MessageDeviceService. h
-   MetadataDeviceService. h
-   NotesDeviceService. h
-   RingtoneDeviceService. h
-   StatusDeviceService. h
-   SyncDeviceService. h
-   TaskDeviceService. h

Parmi les fichiers de la liste précédente, BridgeDeviceService. h et DeviceService. h sont requis pour presque toutes les applications qui prennent en charge les services d’appareils. les autres fichiers définissent différents types de services d’appareil et sont inclus comme il convient.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Windows Appareils mobiles**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
