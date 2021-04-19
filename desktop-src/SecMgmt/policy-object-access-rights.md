---
description: Répertorie et décrit les types d’accès de l’objet de stratégie.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Droits d’accès à l’objet de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529113"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="82892-103">Droits d’accès à l’objet de stratégie</span><span class="sxs-lookup"><span data-stu-id="82892-103">Policy Object Access Rights</span></span>

<span data-ttu-id="82892-104">L’objet de [**stratégie**](policy-object.md) a les types d’accès spécifiques aux objets suivants :</span><span class="sxs-lookup"><span data-stu-id="82892-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="82892-105">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="82892-105">Access type</span></span>                         | <span data-ttu-id="82892-106">Description</span><span class="sxs-lookup"><span data-stu-id="82892-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82892-107">\_ \_ informations locales sur l’affichage \_ de la stratégie</span><span class="sxs-lookup"><span data-stu-id="82892-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="82892-108">Ce type d’accès est nécessaire pour lire les informations de stratégie de sécurité diverses du système cible.</span><span class="sxs-lookup"><span data-stu-id="82892-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="82892-109">Cela comprend le quota par défaut, l’audit, l’état du serveur et les informations de rôle, ainsi que les informations d’approbation.</span><span class="sxs-lookup"><span data-stu-id="82892-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="82892-110">Ce type d’accès est également nécessaire pour énumérer les domaines approuvés, les comptes et les [*privilèges*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="82892-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="82892-111">\_ \_ informations confidentielles \_ sur la stratégie</span><span class="sxs-lookup"><span data-stu-id="82892-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="82892-112">Ce type d’accès est nécessaire pour afficher des informations sensibles, telles que les noms de comptes établis pour les relations de domaine approuvées.</span><span class="sxs-lookup"><span data-stu-id="82892-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="82892-113">\_administrateur d’approbation de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="82892-114">Ce type d’accès est nécessaire pour modifier le domaine du compte ou les informations du domaine principal.</span><span class="sxs-lookup"><span data-stu-id="82892-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="82892-115">\_limites de \_ quota par défaut définies par la stratégie \_ \_</span><span class="sxs-lookup"><span data-stu-id="82892-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="82892-116">Définissez les quotas système par défaut qui sont appliqués aux comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82892-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="82892-117">\_clé de création de la stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="82892-118">Ce type d’accès est nécessaire pour créer un objet de données privées.</span><span class="sxs-lookup"><span data-stu-id="82892-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="82892-119">\_créer un \_ compte de stratégie</span><span class="sxs-lookup"><span data-stu-id="82892-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="82892-120">Ce type d’accès est nécessaire pour créer un nouvel objet de [**compte**](account-object.md) .</span><span class="sxs-lookup"><span data-stu-id="82892-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="82892-121">\_ \_ exigences d’audit définies pour la stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="82892-122">Ce type d’accès est nécessaire pour mettre à jour les exigences d’audit du système.</span><span class="sxs-lookup"><span data-stu-id="82892-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="82892-123">\_administrateur du \_ Journal d’audit de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="82892-124">Ce type d’accès est nécessaire pour modifier les caractéristiques de la piste d’audit, telles que sa taille maximale ou la période de rétention pour les enregistrements d’audit, ou pour effacer le journal.</span><span class="sxs-lookup"><span data-stu-id="82892-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="82892-125">\_ \_ informations d’audit d’affichage de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="82892-126">Ce type d’accès est nécessaire pour afficher les informations sur la piste d’audit ou les exigences d’audit.</span><span class="sxs-lookup"><span data-stu-id="82892-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="82892-127">\_administrateur du serveur de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="82892-128">Ce type d’accès est nécessaire pour modifier les informations sur l’état du serveur ou le rôle (maître/réplica).</span><span class="sxs-lookup"><span data-stu-id="82892-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="82892-129">Il est également nécessaire de modifier la source du réplica et les informations du nom du compte.</span><span class="sxs-lookup"><span data-stu-id="82892-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="82892-130">\_noms de recherche de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="82892-131">Ce type d’accès est nécessaire pour effectuer la conversion entre les noms et les SID.</span><span class="sxs-lookup"><span data-stu-id="82892-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="82892-132">\_privilège de création de stratégie \_</span><span class="sxs-lookup"><span data-stu-id="82892-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="82892-133">Pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="82892-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="82892-134">Masques d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="82892-134">Generic Access Masks</span></span>

<span data-ttu-id="82892-135">L’objet de [**stratégie**](policy-object.md) publie les mappages suivants à partir de types d’accès génériques vers des types d’accès spécifiques :</span><span class="sxs-lookup"><span data-stu-id="82892-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="82892-136">Types d’accès standard</span><span class="sxs-lookup"><span data-stu-id="82892-136">Standard Access Types</span></span>

<span data-ttu-id="82892-137">Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif).</span><span class="sxs-lookup"><span data-stu-id="82892-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="82892-138">Tous les types d’accès requis sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="82892-138">All required access types are supported.</span></span> <span data-ttu-id="82892-139">Le masque de tous les types d’accès pris en charge pour ce type d’objet est :</span><span class="sxs-lookup"><span data-stu-id="82892-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
