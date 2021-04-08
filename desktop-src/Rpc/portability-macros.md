---
title: Macros de portabilité (RPC. h)
description: Les outils RPC permettent d’obtenir l’indépendance de modèle, d’appel et de convention d’affectation de noms en associant les types de données et les types de retour de fonction dans les fichiers stub générés et les fichiers d’en-tête avec des définitions spécifiques à chaque plateforme.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Macros de portabilité RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "103953331"
---
# <a name="portability-macros"></a><span data-ttu-id="dce22-104">Macros de portabilité</span><span class="sxs-lookup"><span data-stu-id="dce22-104">Portability Macros</span></span>

<span data-ttu-id="dce22-105">Les outils RPC permettent d’obtenir l’indépendance de modèle, d’appel et de convention d’affectation de noms en associant les types de données et les types de retour de fonction dans les fichiers stub générés et les fichiers d’en-tête avec des définitions spécifiques à chaque plateforme.</span><span class="sxs-lookup"><span data-stu-id="dce22-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="dce22-106">Ces définitions de macros garantissent que tous les types de données et fonctions qui requièrent la désignation de **\_ \_ Far** sont spécifiés en tant qu’objets Far.</span><span class="sxs-lookup"><span data-stu-id="dce22-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="dce22-107">L’illustration suivante montre les définitions de macros que le compilateur MIDL applique aux appels de fonction entre les composants RPC :</span><span class="sxs-lookup"><span data-stu-id="dce22-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![Diagramme montrant les définitions de macros MIDL s’applique aux appels de fonction.](images/prog-a29.png)

<span data-ttu-id="dce22-109">Les macros RPC sont définies comme suit.</span><span class="sxs-lookup"><span data-stu-id="dce22-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="dce22-110">Définition</span><span class="sxs-lookup"><span data-stu-id="dce22-110">Definition</span></span>    | <span data-ttu-id="dce22-111">Description</span><span class="sxs-lookup"><span data-stu-id="dce22-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce22-112">\_\_\_API RPC</span><span class="sxs-lookup"><span data-stu-id="dce22-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="dce22-113">Appliqué aux appels effectués par le stub à l’application utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dce22-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="dce22-114">Les deux fonctions se trouvent dans le même programme exécutable.</span><span class="sxs-lookup"><span data-stu-id="dce22-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="dce22-115">\_\_RPC \_ Far</span><span class="sxs-lookup"><span data-stu-id="dce22-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="dce22-116">Appliqué à la définition de macro standard pour les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="dce22-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="dce22-117">Cette définition de macro doit apparaître dans la signature de toutes les fonctions fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dce22-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="dce22-118">\_\_\_stub RPC</span><span class="sxs-lookup"><span data-stu-id="dce22-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="dce22-119">Appliqué aux appels effectués à partir de la bibliothèque Runtime vers le stub.</span><span class="sxs-lookup"><span data-stu-id="dce22-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="dce22-120">Ces appels peuvent être considérés comme privés.</span><span class="sxs-lookup"><span data-stu-id="dce22-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="dce22-121">\_\_\_utilisateur RPC</span><span class="sxs-lookup"><span data-stu-id="dce22-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="dce22-122">Appliqué aux appels effectués par la bibliothèque Runtime à l’application utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dce22-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="dce22-123">Ils traversent la limite entre une DLL et une application.</span><span class="sxs-lookup"><span data-stu-id="dce22-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="dce22-124">\_entrée RPC</span><span class="sxs-lookup"><span data-stu-id="dce22-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="dce22-125">Appliqué aux appels effectués par l’application ou le stub à la bibliothèque Runtime.</span><span class="sxs-lookup"><span data-stu-id="dce22-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="dce22-126">Cette définition de macro est appliquée à toutes les fonctions runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="dce22-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="dce22-127">Pour établir une liaison correcte avec les bibliothèques Runtime Microsoft RPC, les stubs et les routines de prise en charge, certaines fonctions fournies par l’utilisateur doivent également inclure ces macros dans la définition de fonction.</span><span class="sxs-lookup"><span data-stu-id="dce22-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="dce22-128">Utilisez l' **\_ \_ \_ API RPC** de macro lorsque vous définissez les fonctions associées à la gestion de la mémoire, aux handles de liaison définis par l’utilisateur et à l’attribut **transmit \_ As** , et utilisez l' **\_ \_ \_ utilisateur RPC** de la macro quand vous définissez la routine d’exécution de contexte associée au handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="dce22-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="dce22-129">Spécifiez les fonctions comme suit :</span><span class="sxs-lookup"><span data-stu-id="dce22-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="dce22-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_Utilisateur \_ RPC *MIDL \_* \_ allouer (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Utilisateur \_ RPC *utilisateur \_* \_ gratuit (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Liaison *comme HandleType* de l’utilisateur RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_ *Comme HANDLETYPE* utilisateur RPC \_ annuler la liaison (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Type* d’utilisateur RPC \_ sur \_ local</span><span class="sxs-lookup"><span data-stu-id="dce22-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Type* \_ d’utilisateur RPC \_ local</span><span class="sxs-lookup"><span data-stu-id="dce22-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Type d’utilisateur RPC \_ à transmission \_ (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Type* d’utilisateur RPC de la transmission \_ de transmission \_ (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Type* d’utilisateur RPC \_ gratuit \_ local</span><span class="sxs-lookup"><span data-stu-id="dce22-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Type* d’utilisateur RPC \_ gratuit \_ inst (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_Transmission \_ libre du *type* d’utilisateur RPC \_ \_ (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dce22-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_Arrêt du contexte de l’utilisateur RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="dce22-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="dce22-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dce22-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="dce22-143">Tous les paramètres de pointeur dans ces fonctions doivent être spécifiés à l’aide de la macro **\_ \_ RPC \_ bien**.</span><span class="sxs-lookup"><span data-stu-id="dce22-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dce22-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dce22-144">Requirements</span></span>



| <span data-ttu-id="dce22-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dce22-145">Requirement</span></span> | <span data-ttu-id="dce22-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="dce22-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dce22-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dce22-147">Minimum supported client</span></span><br/> | <span data-ttu-id="dce22-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dce22-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dce22-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dce22-149">Minimum supported server</span></span><br/> | <span data-ttu-id="dce22-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dce22-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dce22-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="dce22-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce22-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce22-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





