---
title: Windows Structures des services de déploiement
description: les structures suivantes sont utilisées avec les Services de déploiement Windows.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760249"
---
# <a name="windows-deployment-services-structures"></a>Windows Structures des services de déploiement

les structures suivantes sont utilisées avec les Services de déploiement Windows.



| Structure                                                                         | Description                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**\_adresse PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Spécifie l’adresse réseau d’un paquet.                                                                        |
| [**\_message PXE DHCP \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | cette structure est utilisée avec l’API du serveur PXE Windows Deployment Services.                                        |
| [**PXE \_ DHCP \_ (option)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | cette structure est utilisée avec l’API du serveur PXE Windows Deployment Services.                                        |
| [**\_fournisseur PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Décrit un fournisseur.                                                                                              |
| [**\_cred CLI de WDS \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contient les informations d’identification utilisées pour autoriser une session cliente.                                                           |
| [**\_requête TRANSPORTCLIENT \_ WDS**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Utilisé par la fonction [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_informations sur la session TRANSPORTCLIENT \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Utilisé par la fonction de rappel [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**\_paramètres d' \_ initialisation de TRANSPORTPROVIDER WDS \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Utilisé par la fonction de rappel [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**\_paramètres de TRANSPORTPROVIDER WDS \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Utilisé par la fonction de rappel [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

les éléments suivants sont disponibles à partir de Windows 8 et Windows Server 2012.

| Structure                                          | Description                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ DHCPv6 \_ (option)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | utilisé avec l’API du serveur PXE Windows Deployment Services. |
| [**\_Message DHCPv6 \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Message DHCPV6.                                         |



 

 

 




