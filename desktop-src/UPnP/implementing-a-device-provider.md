---
title: Implémentation d’un fournisseur d’appareils
description: Pour implémenter un fournisseur d’appareils, créez un objet qui expose l’interface IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462450"
---
# <a name="implementing-a-device-provider"></a>Implémentation d’un fournisseur d’appareils

Pour implémenter un fournisseur d’appareils, créez un objet qui expose l’interface [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) . Cet objet doit être inscrit auprès de l’hôte d’appareil à l’aide de la méthode [**IUPnPRegistrar :: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) . Cette méthode accepte les paramètres suivants :

-   Nom du fournisseur, qui doit être unique sur l’ordinateur.
-   ProgID de la classe qui implémente le fournisseur de l’appareil.
-   Chaîne d’initialisation qui est passée au fournisseur de l’appareil au démarrage.
-   ID de conteneur. Un ID de conteneur est une chaîne qui identifie le groupe auquel appartient l’appareil. Tous les appareils avec le même identificateur de conteneur sont hébergés dans le même processus.

 

 




