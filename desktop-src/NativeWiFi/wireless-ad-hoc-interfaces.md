---
description: L’interface de programmation ad hoc sans fil est composée des interfaces suivantes.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517599"
---
# <a name="wireless-ad-hoc-interfaces"></a>Interfaces ad hoc sans fil

L’interface de programmation ad hoc sans fil est composée des interfaces suivantes.



| Nom de l'interface                                                                       | Description                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Représente une carte d’interface réseau (NIC) sans fil.                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Définit les notifications prises en charge par [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Crée et gère des réseaux ad hoc 802,11.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Définit les notifications prises en charge par l’interface [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) . |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Représente une destination de réseau ad hoc disponible dans la plage de connexions.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Définit les notifications prises en charge par l’interface [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) . |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Spécifie les paramètres de sécurité pour un réseau ad hoc sans fil.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Représente la collection des interfaces réseau ad hoc 802,11 actuellement visibles.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Représente la collection de réseaux ad hoc 802,11 actuellement visibles.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Représente la collection de paramètres de sécurité associée à chaque réseau ad hoc sans fil visible.   |



 

> [!Note]  
> Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows. À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez plutôt [le Wi-Fi direct](about-the-wi-fi-direct-api.md) .

 

 

 



