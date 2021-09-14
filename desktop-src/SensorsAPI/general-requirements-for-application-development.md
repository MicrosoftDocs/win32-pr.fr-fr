---
description: Cette rubrique décrit ce que vous devez faire pour commencer à créer des programmes qui utilisent l’API de capteur.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Configuration générale requise pour le développement d’applications (API de capteur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233244"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Configuration générale requise pour le développement d’applications (API de capteur)

Cette rubrique décrit ce que vous devez faire pour commencer à créer des programmes qui utilisent l’API de capteur.

pour créer une application API de capteur, vous devez installer Windows 7 et le kit de développement logiciel (SDK) Windows 7 sur votre ordinateur. Le tableau suivant décrit les fichiers spécifiques dont vous aurez besoin.



| Nom de fichier               | Description                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi. h            | Fichier d’en-tête principal pour l’API de capteur. Ce fichier d’en-tête contient les définitions d’interface.               |
| Capteurs. h               | Fichier d’en-tête qui contient les définitions des constantes définies par la plateforme.                                    |
| Initguid. h              | Fichier d’en-tête qui contient les définitions pour le contrôle de l’initialisation du **GUID** .                          |
| FunctionDiscoveryKeys. h | Fichier d’en-tête qui définit les clés de propriété d’ID d’appareil qui sont requises lorsque vous vous connectez aux capteurs logiques. |
| Sensorsapi. lib          | Bibliothèque statique qui contient des définitions de **GUID** pour l’API de capteur.                                     |
| PortableDeviceGuids. lib | bibliothèque statique qui contient des définitions de **GUID** pour Windows objets périphériques portables.                   |



 

Votre programme peut nécessiter des fichiers supplémentaires.

## <a name="supported-operating-systems"></a>Systèmes d'exploitation pris en charge

les applications API de capteur s’exécutent sur toutes les éditions de Windows 7, à l’exception de l’édition Windows 7 Édition Starter.

## <a name="windows-portable-devices-interfaces"></a>Windows Interfaces des appareils mobiles

l’API de capteur utilise certains objets Windows des appareils mobiles (WPD) pour encapsuler les clés et les valeurs de propriété. Le tableau suivant décrit les interfaces de ces objets.



| Interface                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Cette interface offre un moyen pratique de créer un conteneur de propriétés de paires nom/valeur. Les noms sont représentés par **PROPERTYKEY** s et les valeurs sont représentées par **PROPVARIANT** s. <br/> L’API utilise cette interface pour définir et récupérer à la fois des valeurs uniques et des ensembles de valeurs. Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, en appelant **CoCreateInstance** avec CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Cette interface contient une collection de **PROPERTYKEY** s. Ces clés représentent des noms de propriétés qui peuvent être stockés par **IPortableDeviceValues**. L’API utilise cet objet de collection pour définir et récupérer à la fois des noms de propriété uniques et des ensembles de noms de propriétés.<br/> Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, en appelant **CoCreateInstance** avec CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

