---
description: Apprenez à utiliser l’API WSD (Web Services on Devices) de Microsoft pour implémenter des appareils et des services contrôlés par le client, ainsi que des hôtes d’appareil conformes à DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Développement d’applications WSD sur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d02810f55cc7ae450323543d7a0ee88f055b247fed589057e7d77710f4f86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639349"
---
# <a name="wsd-application-development-on-windows"></a>Développement d’applications WSD sur Windows

L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI peut être utilisé pour le développement des implémentations du client et du serveur (périphérique).

Très souvent, le code WSDAPI pour ces applications est généré à l’aide de [WsdCodeGen](web-services-for-devices-code-generator.md). Certaines fonctions et méthodes WSDAPI sont destinées à être appelées uniquement par le code généré. La documentation de référence sur les API indique quand une fonction ou une méthode doit être utilisée ou implémentée uniquement par le code généré.

le SDK Windows comprend des exemples de fichiers WSDL, des fichiers de configuration WsdCodeGen et du code généré. Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).

Si vous souhaitez énumérer les appareils à l’aide du protocole WSD et interroger les métadonnées de l’appareil WSD, vous pouvez utiliser l’API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) à la place.

si vous souhaitez implémenter un périphérique wsd qui ne s’exécute pas Windows, consultez la page [développement de périphérique wsd](wsd-device-development.md).
