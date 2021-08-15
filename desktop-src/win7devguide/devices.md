---
title: appareils (Guide du développeur Windows 7)
description: les appareils sont un élément fondamental de l’expérience du PC, et Windows 7 offre de nouvelles possibilités aux développeurs d’applications qui interagissent avec les appareils.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086732"
---
# <a name="devices-windows-7-developer-guide"></a>appareils (Guide du développeur Windows 7)

les appareils sont un élément fondamental de l’expérience du PC, et Windows 7 offre de nouvelles possibilités aux développeurs d’applications qui interagissent avec les appareils. La plateforme d’expérience des appareils permet d’associer des applications et des services à un appareil particulier, afin que les utilisateurs puissent tirer le meilleur parti de leurs périphériques immédiatement au moment de la connexion. La plateforme de capteur fournit un ensemble d’API pour la découverte et la communication avec des appareils de capteur qui permettent une nouvelle génération d’applications qui prennent en charge leurs environnements. La plateforme d’emplacement fournit de nouvelles API pour l’utilisation des données d’emplacement à partir d’un récepteur GPS (Global Positioning Systems) ou d’autres services qui activent le comportement de l’application spécifique à l’emplacement pour les utilisateurs mobiles. (Voir [notions de base sur les appareils-vue d’ensemble](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="device-experience-platform"></a>Plateforme de l’expérience des appareils

Windows 7 combine des logiciels et des services pour créer de nouvelles expériences passionnantes pour les téléphones mobiles, les lecteurs multimédias portables, les appareils photo et les imprimantes. Windows 7 facilite l’utilisation de ces appareils directement à partir du bureau Windows. il fournit également aux réviseurs d’appareils un positionnement évident sur le bureau Windows, avec des opportunités de personnalisation et une interface simple pour la présentation des fonctionnalités et des services pris en charge par l’appareil.

grâce à la plateforme d’expérience des appareils, chaque session de Windows devient un portail permettant aux clients d’exploiter davantage la valeur de leurs appareils. La plateforme d’expérience des appareils permet aux utilisateurs de se connecter au fabricant de l’appareil, de découvrir et d’utiliser des services connexes, et d’en savoir plus sur les accessoires. Étant donné que l’expérience de l’appareil est connectée aux services Web de Microsoft, les fabricants d’appareils peuvent mettre à jour l’expérience même après la livraison des appareils aux consommateurs. la plateforme d’expérience des appareils peut générer une expérience de type application pour les appareils Windows *Logo* , tels qu’un téléphone mobile.

la plateforme d’expérience des appareils permet aux applications d’accéder à des appareils tels que des téléphones mobiles et des lecteurs multimédias qui implémentent des services via le *protocole MTP (media Transfer Protocol)* ou le modèle de pilote des [appareils mobiles Windows](https://www.bing.com/search?q=Windows+Portable+Devices) .

Pour permettre la synchronisation des informations personnelles entre un PC et un appareil, la plateforme d’expérience des appareils héberge une nouvelle plateforme de synchronisation pour les appareils connectés et fournit une interface utilisateur pour sélectionner des applications cibles pour la synchronisation des données, telles que les **contacts**, le **calendrier** et les **tâches**. (voir [Windows l’expérience](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)de l’appareil.)

## <a name="windows-biometric-framework"></a>Windows Biometric Framework

le Windows Biometric Framework (WBF) fournit une API qui permet aux applications d’utiliser des périphériques d’empreinte digitale pour inscrire, identifier et vérifier les identités des utilisateurs sans avoir accès directement à des échantillons ou du matériel d’empreintes digitales biométriques. vous pouvez utiliser WBF avec des appareils d’empreintes digitales qui ont des pilotes de Windows server (smart Device Interface). WBF est extensible grâce à des adaptateurs de plug-in qui gèrent les communications de capteur, la correspondance biométrique et le stockage de modèles. Cela permet de s’assurer que WBF peut être utilisé avec un large éventail de capteurs d’empreintes digitales. dans Windows 7, les lecteurs d’empreintes digitales peuvent utiliser WBF pour l’authentification pendant l' *UAC* et Windows ouverture de session. (voir [API Windows Biometric Framework](../secbiomet/biometric-service-api-portal.md).)

 

 
