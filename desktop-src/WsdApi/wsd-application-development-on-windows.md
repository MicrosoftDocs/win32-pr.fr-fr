---
description: L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au profil des appareils pour les services Web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Développement d’applications WSD sur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534288"
---
# <a name="wsd-application-development-on-windows"></a>Développement d’applications WSD sur Windows

L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI peut être utilisé pour le développement des implémentations du client et du serveur (périphérique).

Très souvent, le code WSDAPI pour ces applications est généré à l’aide de [WsdCodeGen](web-services-for-devices-code-generator.md). Certaines fonctions et méthodes WSDAPI sont destinées à être appelées uniquement par le code généré. La documentation de référence sur les API indique quand une fonction ou une méthode doit être utilisée ou implémentée uniquement par le code généré.

Le SDK Windows comprend des exemples de fichiers WSDL, des fichiers de configuration WsdCodeGen et du code généré. Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).

Si vous souhaitez énumérer les appareils à l’aide du protocole WSD et interroger les métadonnées de l’appareil WSD, vous pouvez utiliser l’API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) à la place.

Si vous souhaitez implémenter un périphérique WSD qui n’exécute pas Windows, consultez la page [développement de périphérique WSD](wsd-device-development.md).
