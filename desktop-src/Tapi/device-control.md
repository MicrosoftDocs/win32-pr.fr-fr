---
description: Le contrôle de périphérique au niveau de l’application ou de l’utilisateur final requiert un ensemble relativement restreint d’informations de base.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Contrôle de l’appareil (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17336941a55a529c6b436270f7b225a1cada3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516010"
---
# <a name="device-control-telephony-api"></a>Contrôle de l’appareil (API de téléphonie)

Le contrôle de périphérique au niveau de l’application ou de l’utilisateur final requiert un ensemble relativement restreint d’informations de base. La couche d’abstraction du fournisseur de services effectue un contrôle d’appareil détaillé. Les fournisseurs de services signalent les informations de périphérique requises à une application par le biais de l’interface TAPI.

Les principales catégories d’appareils sont les suivantes :

-   [Réseau](network-ovr.md): couche de transport pour les communications. Du point de vue d’une application, les informations sur le réseau sont généralement incorporées dans le type d’adresse, par exemple LINEADDRESSTYPE \_ PHONENUMBER.
-   [Ligne](line-ovr.md): connexion à un réseau. Ce concept est largement utilisé dans TAPI 2,2 (TAPI/C).
-   [Channel](channel-ovr.md): sous-division d’une ligne. La connaissance des canaux n’est généralement pas nécessaire pour une application, car le fournisseur de services configure la façon dont ils s’affichent en tant qu’adresses.
-   [Adresse](address-ovr.md): un emplacement réseau sur un réseau. Chaque ligne ou canal a une ou plusieurs adresses associées. L’adresse est un concept clé dans TAPI 3,1 (TAPI/COM) et TAPI 2,2 (TAPI/C).
-   [Terminal](terminal-ovr.md): source ou convertisseur pour une adresse et un type de support particuliers.

Les fournisseurs de services signalent les caractéristiques de l’appareil à l’interface TAPI en réponse aux requêtes de l’application. Les fournisseurs de services initient également des rapports sur les modifications de l’état de l’appareil. Ces modifications sont ensuite signalées à une application en fonction des notifications demandées pendant l’initialisation.

Les caractéristiques de base des appareils sont les suivantes :

-   [Classe d’appareil](device-class-ovr.md)
-   [Identificateur de l’appareil](device-identifier-ovr.md)
-   [Type d’adresse](address-type-ovr.md)
-   [Identificateur d’adresse](address-identifier-ovr.md)
-   [Événements de l’appareil](device-events-ovr.md)
-   [Type de média](media-type-ovr.md)
-   [Type de terminal](terminal-type-ovr.md)

En outre, les fournisseurs de services fournissent des informations relatives à la capacité d’une adresse donnée à effectuer différentes opérations de session.

Des caractéristiques supplémentaires peuvent être associées à certains appareils, si les fournisseurs de services les prennent en charge. Une application TAPI 2. x Découvre les fonctionnalités à l’aide des fonctions [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) et [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) . Les applications TAPI 3. x utilisent l’interface [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) à cet effet.

TAPI 2. x fournit un ensemble spécial d’opérations supplémentaires que le fournisseur de services peut implémenter pour une utilisation avec des appareils téléphoniques. Voir [appareils téléphoniques](./opening-and-closing-phone-devices.md).

Les fonctionnalités étendues sont spécifiques au fournisseur et ne sont pas directement couvertes par l’API de téléphonie Microsoft. Consultez [fonctions de ligne étendue](./extended-line-functions.md), [fonctions téléphoniques de téléphonie étendues](./extended-telephony-phone-functions.md)ou [interfaces spécifiques au fournisseur](provider-specific-interfaces.md).

Voici un résumé des opérations TAPI qui interrogent des fournisseurs de services sur les caractéristiques des appareils et fournissent des données sur l’état actuel.



| Fonctions TAPI 2. x                                                  | Description                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Interroge un périphérique de ligne spécifié pour déterminer les fonctions de téléphonie des adresses associées.               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Interroge un périphérique de ligne spécifié pour déterminer les fonctions de téléphonie d’une adresse spécifique.                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Retourne une structure de données « opaque » qui stocke la configuration actuelle d’un appareil.                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Restaure la configuration de l’appareil.                                                                                 |
| [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés à l’appareil.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Récupère un identificateur d’appareil stable qui peut être utilisé dans d’autres appels de fonction TAPI ou avec une API différente. |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Interroge l’appareil en fonction de l’état actuel, par exemple le nombre d’appels actifs.                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Définit l’état de l’appareil, tel que la définition d’un appareil comme non-service.                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Récupère l’icône spécifique au fournisseur pour l’affichage à l’utilisateur.                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Permet à une application de négocier une version d’extension à utiliser avec le périphérique de ligne spécifié.                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Donne accès aux fonctionnalités spécifiques à l’appareil.                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Envoie des fonctionnalités spécifiques à l’appareil au fournisseur de services.                                                        |



 



| Interfaces ou méthodes TAPI 3. x                                   | Description                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Obtient des informations sur les fonctionnalités d’une adresse.                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Définit et obtient DirectShow™ format multimédia.                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Définit et obtient les caractéristiques du terminal audio standard, telles que le volume.                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Obtient des informations sur les fonctionnalités de support multimédia d’une adresse.                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Interface de base pour l’objet terminal. Obtient des informations telles que la classe de terminal et le support pris en charge. |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Obtient des informations sur les terminaux disponibles et crée des terminaux supplémentaires.                               |
| [Interfaces spécifiques au fournisseur](provider-specific-interfaces.md) | Dépend du fournisseur de services.                                                                             |



 

 

 
