---
description: Dans l’architecture TAPI, tous les TSPs sont exécutés dans le contexte de TAPISRV, qui est implémenté en tant que processus de service dans SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Architecture MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393335"
---
# <a name="msp-architecture"></a>Architecture MSP

Dans l’architecture TAPI, tous les TSPs sont exécutés dans le contexte de TAPISRV, qui est implémenté en tant que processus de service dans SVCHOST. Les applications TAPI résident dans leur propre processus. Les applications TAPI chargent Tapi3.dll et les MSP nécessaires dans leur propre processus, et la DLL TAPI communique avec TAPISRV via une interface RPC privée. Le diagramme suivant illustre l’interaction de ces composants.

![interactions entre tapisrv, les applications TAPI et les MSP](images/tsp-msp1.png)

Un fournisseur de services de média (MSP) fournit la diffusion multimédia en continu à l’aide des abstractions des terminaux, des flux et des sous-flux.

Un terminal est un récepteur ou une source pour un flux de média. Il peut s’agir d’un objet physique, tel qu’un haut-parleur ou un microphone, ou d’une abstraction d’un appareil, telle qu’une fenêtre vidéo. L' [objet terminal](terminal-object.md) expose l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . La classe de terminal est décrite par le GUID de la [**classe terminal**](terminal-class.md) . Un MSP peut définir ses propres classes de terminaux.

Les flux divisent le média d’un appel en fonction du type de [**média**](tapimediatype--constants.md) ou du type, de la [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)du flux et de l’adresse de destination du média. Par exemple, un flux audio entrant d’un modem est un objet de flux, un flux vidéo sortant vers une adresse IP et un port est un objet de flux, les flux vidéo provenant d’un groupe de multidiffusion IP sont également considérés comme un objet de flux. L’objet de flux est représenté par l’interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) .

Les sous-flux permettent un contrôle plus précis sur le média. Par exemple, dans le cas de la multidiffusion IP, l’objet flux vidéo entrant peut représenter plusieurs personnes. L’application souhaitera probablement que chaque participant ait un convertisseur distinct. Le flux vidéo entrant peut être divisé en plusieurs sous-flux, un pour chaque personne. Un sous-flux correspond à une personne et peut être configuré et contrôlé séparément. L’objet de sous-flux est représenté par l’interface [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) .

Quand une application appelle [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) pour configurer un appel, elle doit spécifier le type de média requis. Sur un appel sortant, il indique simplement à TAPI une fois l’appel créé. Par exemple :

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

Dans ce cas, l’application crée un appel audio-vidéo sortant.

Les types de média transmis indiquent le support qui intéresse l’application pendant la durée de vie de l’appel. Par exemple, l’application peut spécifier l’audio et la vidéo lors de la création de l’appel, mais ne sélectionner que des terminaux audio au début. Le MSP démarre uniquement la diffusion audio en continu, mais ne rejette pas une requête vidéo locale ou distante effectuée plus tard au cours de la durée de vie de l’appel.

Lorsque l’application appelle ensuite [**ITBasicCallControl :: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 appelle [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) dans le TSP. Après l’établissement d’un appel, le MSP et le TSP peuvent communiquer en fonction des besoins.

Lors de la déconnexion d’un appel, il revient au MSP et au TSP de communiquer sur le déchirement de l’appel. Tapi3.dll appellera [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) si l’application appelle [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
