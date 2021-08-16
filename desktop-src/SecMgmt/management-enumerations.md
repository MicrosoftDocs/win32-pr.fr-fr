---
description: Répertorie les énumérations utilisées par les fonctions de gestion de la stratégie LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Énumérations de la gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf87e6c41cb3e687a8927c294fe3bc1433a294aaf48991310b1c230f4741f299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894455"
---
# <a name="security-management-enumerations"></a>Énumérations de la gestion de la sécurité

Les énumérations de la gestion de la sécurité sont les suivantes :

-   [Énumérations de la stratégie LSA](#lsa-policy-enumerations)
-   [Énumérations plus sûres](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Énumérations de la stratégie LSA

Les types d’énumération suivants sont utilisés par les fonctions de gestion de la stratégie LSA.



| Énumération                                                                               | Description                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type d' \_ événement d’audit de stratégie \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Définit les types d’événements que le système peut auditer.                                                                                     |
| [**\_classe d’informations de stratégie \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Définit les types d’informations qui peuvent être définis ou interrogés pour un objet de [**stratégie**](policy-object.md) .                             |
| [**\_rôle de \_ serveur \_ LSA de stratégie**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indiquez le rôle d’un serveur LSA.                                                                                                   |
| [**\_classe d' \_ informations de notification de stratégie \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Définit les types d’informations de stratégie et les informations de domaine de stratégie pour lesquelles votre application peut demander une notification des modifications. |
| [**\_État d' \_ activation du serveur de stratégie \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Représente l’état du serveur LSA, c’est-à-dire s’il est activé ou désactivé.                                                   |
| [**\_classe d’informations de confiance \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Définit les types d’informations qui peuvent être définis ou interrogés pour un domaine approuvé.                                                     |



 

## <a name="safer-enumerations"></a>Énumérations plus sûres

La [sécurité](safer.md) utilise les types énumérés suivants.



| Nom                                                               | Description                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TYPES d' \_ identification plus sûrs \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Type d’énumération qui définit les types possibles de structures de règle d’identification qui peuvent être identifiées par la structure d' [**\_ \_ en-tête d’identification plus sécurisée**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) . |
| [**classe d' \_ informations d’objet plus sécurisé \_ \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Type d’énumération qui définit le type d’informations demandé sur un objet plus sécurisé.                                                                                                            |
| [**classe d' \_ informations de stratégie plus sécurisée \_ \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Type d’énumération qui définit les façons dont une stratégie peut être interrogée.                                                                                                                         |



 

 

 



