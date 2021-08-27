---
title: API UPnP
description: L’infrastructure UPnP permet la mise en réseau dynamique d’appareils intelligents, de périphériques sans fil et de PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfadd64dbee845f62052e8b140ca1f0b69837ece78cf7b0cc5f24e61563a6e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124799"
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

les api de Point de contrôle et les api d’hôte d’appareil sont utilisées par diverses applications, des scripts incorporés dans les pages HTML aux programmes C++ et Microsoft Visual Basic à part entière.

seule l’API du Point de contrôle prend en charge Visual Basic scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API du Point de contrôle est utilisée sur les ordinateurs exécutant Microsoft Windows Millennium Edition, Windows xp, Windows xp Professional et Windows CE .net.

l’API de l’hôte d’appareil est utilisée sur les ordinateurs exécutant Windows xp, Windows xp Professional et Windows CE .net.

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



 

 

 





