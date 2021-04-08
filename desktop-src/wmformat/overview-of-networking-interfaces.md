---
title: Vue d’ensemble des interfaces réseau
description: Vue d’ensemble des interfaces réseau
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK, interfaces réseau
- Windows Media Format SDK, interfaces
- ASF (Advanced Systems Format), interfaces réseau
- ASF (format des systèmes avancés), interfaces réseau
- ASF (Advanced Systems Format), liste d’interfaces pour les fonctionnalités de mise en réseau
- ASF (format de systèmes avancés), liste d’interfaces pour les fonctionnalités de mise en réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724130"
---
# <a name="overview-of-networking-interfaces"></a>Vue d’ensemble des interfaces réseau

Les fonctionnalités de mise en réseau de ce kit de développement logiciel (SDK) sont prises en charge par les méthodes des interfaces suivantes.



| Interface                                                  | Description                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Obtient des informations sur les clients connectés à un récepteur réseau.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Fournit une méthode pour obtenir des informations sur un client attaché à un récepteur réseau d’écriture. Cette interface étend l’interface **IWMClientConnections** . |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Fournit une méthode de rappel pour obtenir les informations d’identification de l’utilisateur lors de l’accès à un site distant.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Fournit des méthodes avancées sur l’objet lecteur.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Étend l’interface **IWMReaderAdvanced2** .                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Étend l’interface **IWMReaderAdvanced3** .                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Configure les paramètres réseau sur l’objet lecteur.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Configure des paramètres réseau supplémentaires sur l’objet lecteur. Cette interface étend l’interface **IWMReaderNetworkConfig** .                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Configure l’objet récepteur réseau, qui est utilisé pour écrire des médias numériques sur un réseau.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Configure l’objet récepteur push, qui est utilisé pour distribuer des médias numériques aux points de publication.                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation des fonctionnalités réseau**](implementing-network-functionality.md)
</dt> </dl>

 

 




