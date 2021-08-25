---
title: Recherche d’appareils
description: L’architecture UPnP est une architecture réseau dynamique qui permet aux appareils de rejoindre et de sortir le réseau à tout moment.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867589"
---
# <a name="finding-devices"></a>Recherche d’appareils

L’architecture UPnP est une architecture réseau dynamique qui permet aux appareils de rejoindre et de sortir le réseau à tout moment. En raison de cette architecture dynamique, les applications ne peuvent pas s’appuyer sur des périphériques UPnP spécifiques pour être disponibles à un moment donné. Pour cette raison, les applications (ou points de contrôle) recherchent le réseau pour trouver les appareils qui correspondent le mieux aux critères spécifiés. Les applications attendent également des messages de publication d’appareil indiquant que de nouveaux appareils ont été ajoutés au réseau.

Les éléments suivants sont des critères de recherche valides pour les périphériques basés sur UPnP :

-   Type d'appareil
-   Type de service
-   Nom d’appareil unique (UDN)
-   Tous les appareils racine

Le type d’appareil et les recherches de type de service sont généralement utilisés pour rechercher une classe d’appareils avec des caractéristiques communes. La recherche UDN est utilisée pour rechercher un appareil spécifique.

Pour rechercher des appareils, une application doit d’abord instancier l’objet Device Finder. Cet objet expose l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; ses méthodes effectuent les recherches décrites précédemment.

Les sections suivantes décrivent le processus de recherche d’appareils :

-   [Création du Finder d’appareils](creating-the-device-finder.md)
-   [Recherche asynchrone](asynchronous-searching.md)
-   [Recherche synchrone](synchronous-searching.md)
-   [Regroupements de périphériques retournés par les recherches synchrones](device-collections-returned-by-synchronous-searches.md)

 

 




