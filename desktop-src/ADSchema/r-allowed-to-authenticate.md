---
title: Autorisé à authentifier à droite étendu
description: Les contrôles de droits d’accès du contrôle qui peuvent s’authentifier auprès d’un ordinateur ou d’un service particulier.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Autorisé à authentifier le schéma AD droit étendu
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a63d63751105500986c27c7a851d60146a72281ee8415bc01c5ec8c5dfa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548829"
---
# <a name="allowed-to-authenticate-extended-right"></a>Autorisé à authentifier à droite étendu

Les contrôles de droits d’accès du contrôle qui peuvent s’authentifier auprès d’un ordinateur ou d’un service particulier. Elle réside en fait sur les objets ordinateur, utilisateur et InetOrgPerson. Il est également applicable sur l’objet de domaine si l’accès est autorisé pour l’ensemble du domaine. Il peut être appliqué aux unités d’organisation pour permettre aux utilisateurs de définir des ACE pouvant être héritées sur les unités d’organisation qui contiennent un ensemble d’objets utilisateur ou ordinateur.



| Entrée | Valeur |
|--------------|--------------------------------------|
| CN           | Autorisé à s’authentifier              |
| Display-Name | Autorisé à s’authentifier              |
| Rights-GUID  | 68b1d179-0d15-4d4f-ab71-46152e79a7bc |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Utilisateur**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localisation-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Utilisateur**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localisation-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Utilisateur**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localisation-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-service-account**](c-msds-managedserviceaccount.md)<br/> [**Utilisateur**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localisation-Display-ID | 65                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-service-account**](c-msds-managedserviceaccount.md)<br/> [**Utilisateur**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localisation-Display-ID | 65                                                                                                                                                                                                               |



 

 





