---
description: Fonction définie par l’application qui libère de la mémoire allouée par la fonction AuthzComputeGroupsCallback. AuthzFreeGroupsCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: AuthzFreeGroupsCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760827"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="19405-104">AuthzFreeGroupsCallback fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="19405-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="19405-105">La fonction **AuthzFreeGroupsCallback** est une fonction définie par l’application qui libère de la mémoire allouée par la fonction [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) .</span><span class="sxs-lookup"><span data-stu-id="19405-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="19405-106">**AuthzFreeGroupsCallback** est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="19405-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="19405-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19405-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="19405-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19405-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19405-109">*pSidAttrArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19405-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19405-110">Pointeur vers la mémoire allouée par [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span><span class="sxs-lookup"><span data-stu-id="19405-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19405-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19405-111">Return value</span></span>

<span data-ttu-id="19405-112">Cette fonction de rappel ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="19405-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19405-113">Notes</span><span class="sxs-lookup"><span data-stu-id="19405-113">Remarks</span></span>

<span data-ttu-id="19405-114">Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.</span><span class="sxs-lookup"><span data-stu-id="19405-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="19405-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19405-115">Requirements</span></span>



| <span data-ttu-id="19405-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19405-116">Requirement</span></span> | <span data-ttu-id="19405-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="19405-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="19405-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19405-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19405-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19405-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="19405-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19405-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19405-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19405-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="19405-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="19405-122">Redistributable</span></span><br/>          | <span data-ttu-id="19405-123">Pack des outils d’administration Windows Server 2003 sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="19405-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19405-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19405-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19405-125">Fonctions de base Access Control</span><span class="sxs-lookup"><span data-stu-id="19405-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="19405-126">**AuthzComputeGroupsCallback**</span><span class="sxs-lookup"><span data-stu-id="19405-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




