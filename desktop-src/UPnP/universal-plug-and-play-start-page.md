---
title: API UPnP
description: L’infrastructure UPnP permet la mise en réseau dynamique d’appareils intelligents, de périphériques sans fil et de PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102504"
---
# <a name="upnp-apis"></a>API UPnP

## <a name="purpose"></a>Objectif

L’infrastructure UPnP permet la mise en réseau dynamique d’appareils intelligents, de périphériques sans fil et de PC. Il existe deux API pour l’utilisation d’appareils certifiés UPnP :

-   L’API du point de contrôle, qui se compose d’un ensemble d’interfaces COM utilisées pour rechercher et contrôler des appareils.
-   L’API d’hôte d’appareil, qui se compose d’un ensemble d’interfaces COM utilisées pour implémenter des appareils hébergés par un ordinateur.

## <a name="where-applicable"></a>Le cas échéant

L’API du point de contrôle permet aux développeurs d’écrire des applications qui recherchent et contrôlent les appareils certifiés UPnP. L’API d’hôte d’appareil permet aux développeurs d’implémenter les fonctionnalités des appareils certifiés UPnP et d’utiliser l’hôte d’appareil pour gérer les fonctions de découverte, de description, de contrôle, de présentation et d’événement d’un appareil certifié UPnP.

## <a name="developer-audience"></a>Développeurs concernés

Les développeurs qui utilisent les API de point de contrôle et les API d’hôte d’appareil doivent être familiarisés avec l’architecture de périphérique UPnP. Pour plus d’informations, consultez la [documentation relative](https://openconnectivity.org/resources/upnpresources.zip) à l’implémentation d’UPnP et le [Forum UPnP](https://openconnectivity.org/).

Les développeurs qui utilisent les API d’hôte d’appareil doivent être familiarisés avec les interfaces Active Template Library (ATL) et COM.

Les API de point de contrôle et les API d’hôte d’appareil sont utilisées par diverses applications, des scripts incorporés dans les pages HTML aux programmes C++ et Microsoft Visual Basic à part entière.

Seule l’API du point de contrôle prend en charge les Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Conditions d’exécution

L’API du point de contrôle est utilisée sur les ordinateurs qui exécutent Microsoft Windows Millennium Edition, Windows XP, Windows XP professionnel et Windows CE .NET.

L’API de l’hôte d’appareil est utilisée sur les ordinateurs exécutant Windows XP, Windows XP professionnel et Windows CE .NET.

Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous à « conditions requises » dans la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                          | Description                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Vue d’ensemble de l’architecture UPnP](overview-of-universal-plug-and-play.md)<br/>            | Informations générales et arrière-plan.<br/>                                                     |
| [Vue d’ensemble du point de contrôle](control-point-api.md)<br/>                                     | Informations générales sur l’API du point de contrôle.<br/>                                        |
| [Utilisation de l’API de point de contrôle](using-the-control-point-api-with-upnp-technology.md)<br/> | Exemple de code qui montre comment développer des applications qui contrôlent les appareils certifiés UPnP.<br/> |
| [Informations de référence sur l’API point de contrôle](control-point-api-with-upnp-technology-reference.md)<br/> | Documentation des interfaces, des méthodes et des événements du composant de point de contrôle.<br/>               |
| [Vue d’ensemble de l’API Device Host](device-host-api.md)<br/>                                     | Informations générales sur l’API de l’hôte de l’appareil.<br/>                                          |
| [Utilisation de l’API de l’hôte d’appareil](using-the-device-host-api-with-upnp-technology.md)<br/>     | Exemple de code qui montre comment développer une application pour les appareils certifiés UPnP.<br/>        |
| [Informations de référence sur l’API d’hôte d’appareil](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentation des interfaces, des méthodes et des événements du composant hôte de périphérique.<br/>                 |



 

 

 





