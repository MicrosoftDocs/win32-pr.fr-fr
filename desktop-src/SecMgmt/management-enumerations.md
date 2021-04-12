---
description: Répertorie les énumérations utilisées par les fonctions de gestion de la stratégie LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Énumérations de la gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203031"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="126dc-103">Énumérations de la gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="126dc-103">Security Management Enumerations</span></span>

<span data-ttu-id="126dc-104">Les énumérations de la gestion de la sécurité sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="126dc-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="126dc-105">Énumérations de la stratégie LSA</span><span class="sxs-lookup"><span data-stu-id="126dc-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="126dc-106">Énumérations plus sûres</span><span class="sxs-lookup"><span data-stu-id="126dc-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="126dc-107">Énumérations de la stratégie LSA</span><span class="sxs-lookup"><span data-stu-id="126dc-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="126dc-108">Les types d’énumération suivants sont utilisés par les fonctions de gestion de la stratégie LSA.</span><span class="sxs-lookup"><span data-stu-id="126dc-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="126dc-109">Énumération</span><span class="sxs-lookup"><span data-stu-id="126dc-109">Enumeration</span></span>                                                                               | <span data-ttu-id="126dc-110">Description</span><span class="sxs-lookup"><span data-stu-id="126dc-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="126dc-111">**\_type d' \_ événement d’audit de stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="126dc-112">Définit les types d’événements que le système peut auditer.</span><span class="sxs-lookup"><span data-stu-id="126dc-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="126dc-113">**\_classe d’informations de stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="126dc-114">Définit les types d’informations qui peuvent être définis ou interrogés pour un objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="126dc-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="126dc-115">**\_rôle de \_ serveur \_ LSA de stratégie**</span><span class="sxs-lookup"><span data-stu-id="126dc-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="126dc-116">Indiquez le rôle d’un serveur LSA.</span><span class="sxs-lookup"><span data-stu-id="126dc-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="126dc-117">**\_classe d' \_ informations de notification de stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="126dc-118">Définit les types d’informations de stratégie et les informations de domaine de stratégie pour lesquelles votre application peut demander une notification des modifications.</span><span class="sxs-lookup"><span data-stu-id="126dc-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="126dc-119">**\_État d' \_ activation du serveur de stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="126dc-120">Représente l’état du serveur LSA, c’est-à-dire s’il est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="126dc-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="126dc-121">**\_classe d’informations de confiance \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="126dc-122">Définit les types d’informations qui peuvent être définis ou interrogés pour un domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="126dc-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="126dc-123">Énumérations plus sûres</span><span class="sxs-lookup"><span data-stu-id="126dc-123">Safer Enumerations</span></span>

<span data-ttu-id="126dc-124">La [sécurité](safer.md) utilise les types énumérés suivants.</span><span class="sxs-lookup"><span data-stu-id="126dc-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="126dc-125">Nom</span><span class="sxs-lookup"><span data-stu-id="126dc-125">Name</span></span>                                                               | <span data-ttu-id="126dc-126">Description</span><span class="sxs-lookup"><span data-stu-id="126dc-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="126dc-127">**TYPES d' \_ identification plus sûrs \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="126dc-128">Type d’énumération qui définit les types possibles de structures de règle d’identification qui peuvent être identifiées par la structure d' [**\_ \_ en-tête d’identification plus sécurisée**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) .</span><span class="sxs-lookup"><span data-stu-id="126dc-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="126dc-129">**classe d' \_ informations d’objet plus sécurisé \_ \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="126dc-130">Type d’énumération qui définit le type d’informations demandé sur un objet plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="126dc-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="126dc-131">**classe d' \_ informations de stratégie plus sécurisée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="126dc-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="126dc-132">Type d’énumération qui définit les façons dont une stratégie peut être interrogée.</span><span class="sxs-lookup"><span data-stu-id="126dc-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



