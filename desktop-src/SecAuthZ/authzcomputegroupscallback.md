---
description: Fonction définie par l’application qui crée une liste d’identificateurs de sécurité (SID) qui s’appliquent à un client. AuthzComputeGroupsCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: AuthzComputeGroupsCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760828"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="50cde-104">AuthzComputeGroupsCallback fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="50cde-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="50cde-105">La fonction **AuthzComputeGroupsCallback** est une fonction définie par l’application qui crée une liste d' [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui s’appliquent à un client.</span><span class="sxs-lookup"><span data-stu-id="50cde-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="50cde-106">**AuthzComputeGroupsCallback** est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="50cde-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cde-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50cde-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="50cde-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50cde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cde-109">*hAuthzClientContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50cde-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-110">Handle d’un contexte client.</span><span class="sxs-lookup"><span data-stu-id="50cde-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="50cde-111">*Arguments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50cde-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-112">Données passées dans le paramètre *DynamicGroupArgs* d’un appel à la fonction [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)ou [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .</span><span class="sxs-lookup"><span data-stu-id="50cde-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="50cde-113">*pSidAttrArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50cde-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-114">Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de sid et de structures d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="50cde-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="50cde-115">Ces structures représentent les groupes auxquels le client appartient.</span><span class="sxs-lookup"><span data-stu-id="50cde-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="50cde-116">*pSidCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50cde-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-117">Nombre de structures dans *pSidAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="50cde-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="50cde-118">*pRestrictedSidAttrArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50cde-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-119">Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de sid et de structures d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="50cde-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="50cde-120">Ces structures représentent les groupes dont le client est limité.</span><span class="sxs-lookup"><span data-stu-id="50cde-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="50cde-121">*pRestrictedSidCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50cde-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50cde-122">Nombre de structures dans *pSidRestrictedAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="50cde-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50cde-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50cde-123">Return value</span></span>

<span data-ttu-id="50cde-124">Si la fonction retourne correctement une liste de sid, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="50cde-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="50cde-125">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="50cde-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cde-126">Notes</span><span class="sxs-lookup"><span data-stu-id="50cde-126">Remarks</span></span>

<span data-ttu-id="50cde-127">Les applications peuvent également ajouter des SID au contexte client en appelant [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span><span class="sxs-lookup"><span data-stu-id="50cde-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="50cde-128">Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.</span><span class="sxs-lookup"><span data-stu-id="50cde-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cde-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50cde-129">Requirements</span></span>



| <span data-ttu-id="50cde-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50cde-130">Requirement</span></span> | <span data-ttu-id="50cde-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="50cde-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="50cde-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50cde-132">Minimum supported client</span></span><br/> | <span data-ttu-id="50cde-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50cde-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="50cde-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50cde-134">Minimum supported server</span></span><br/> | <span data-ttu-id="50cde-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50cde-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="50cde-136">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="50cde-136">Redistributable</span></span><br/>          | <span data-ttu-id="50cde-137">Pack des outils d’administration Windows Server 2003 sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="50cde-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50cde-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50cde-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cde-139">Fonctions de base Access Control</span><span class="sxs-lookup"><span data-stu-id="50cde-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="50cde-140">**AuthzAddSidsToContext**</span><span class="sxs-lookup"><span data-stu-id="50cde-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="50cde-141">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="50cde-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="50cde-142">**AuthzInitializeContextFromAuthzContext**</span><span class="sxs-lookup"><span data-stu-id="50cde-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="50cde-143">**AuthzInitializeContextFromSid**</span><span class="sxs-lookup"><span data-stu-id="50cde-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="50cde-144">**AuthzInitializeContextFromToken**</span><span class="sxs-lookup"><span data-stu-id="50cde-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="50cde-145">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="50cde-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="50cde-146">**SID \_ et \_ attributs**</span><span class="sxs-lookup"><span data-stu-id="50cde-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

