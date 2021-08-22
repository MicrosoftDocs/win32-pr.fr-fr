---
description: Le bon fonctionnement des composants TAPI requiert la configuration de l’environnement de communication sur un ordinateur.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Initialisation TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f9062f8440cdec6597d21a2141a24b12f69bc9e940e189965d9e73880c54c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659899"
---
# <a name="tapi-initialization"></a>Initialisation TAPI

Le bon fonctionnement des composants TAPI requiert la configuration de l’environnement de communication sur un ordinateur comme suit :

-   L' [installation](installation.md) est effectuée lors de la première ajout de logiciels ou de matériel à l’ordinateur. Les procédures détaillées dépendent du système d’exploitation et du logiciel lui-même.
-   L' [initialisation principale](primary-initialization.md) crée les objets et les chemins de communication.
-   La [négociation de version](version-negotiation.md) garantit que les composants TAPI seront en mesure d’échanger des données.
-   L' [inventaire des ressources](resource-inventory.md) récupère les informations relatives aux appareils disponibles pour une utilisation par une application TAPI.
-   La [notification d’événements](event-notification.md) spécifie comment l’interface TAPI et les fournisseurs de services passent les résultats des opérations asynchrones et les informations de changement d’État à l’application.

## <a name="summary-of-related-reference-pages"></a>Résumé des pages de référence associées



| Fonctions TAPI 2. x                                        | Description                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configure l’environnement de téléphonie, retourne le descripteur d’application et le nombre d’appareils.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Obtient les fonctionnalités de l’appareil, telles que la version TAPI ou les types de média pris en charge.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Obtient des fonctionnalités d’adresse, par exemple si le parc d’appels est pris en charge.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Indique à TAPI que l’application utilisera la ligne et de quelle manière.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Retourne le message TAPI suivant mis en file d’attente pour la remise à une application qui utilise le mécanisme de notification de handle d’événement |



 



| Interfaces ou méthodes TAPI 3. x                                                | Description                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI :: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Configure l’environnement de téléphonie.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Énumère les adresses actuellement disponibles.                                                                                                  |
| [**ITTAPI :: obtient les \_ adresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Crée une collection d’adresses actuellement disponibles. Fourni pour les applications clientes Automation, telles que celles écrites en Visual Basic. |
| [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Détermine la réponse à une notification d’événement asynchrone. Implémentée par l’application, appelée par l’interface TAPI.                                |
| [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Définit le masque de filtre d’événement, qui avertit l’interface TAPI des événements requis par l’application.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Indique à TAPI de transmettre les sessions entrantes de l’application pour une adresse et un ensemble de types de média spécifiés.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Permet à une application de découvrir les fonctionnalités de support multimédia pour une adresse.                                                           |



 

 

 
