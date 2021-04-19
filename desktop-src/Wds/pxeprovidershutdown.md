---
title: PxeProviderShutdown fonction de rappel
description: Appelé pour arrêter le fournisseur.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Fonction de rappel PxeProviderShutdown des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509103"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="1cc02-104">PxeProviderShutdown fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="1cc02-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="1cc02-105">Appelé pour arrêter le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1cc02-105">Called to shutdown the provider.</span></span> <span data-ttu-id="1cc02-106">Cette fonction est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini **sur \_ \_ arrêt du rappel PXE**.</span><span class="sxs-lookup"><span data-stu-id="1cc02-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="1cc02-107">Une fois cette fonction appelée, le handle *hProvider* passé à la fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="1cc02-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc02-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cc02-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="1cc02-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc02-110">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cc02-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc02-111">Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="1cc02-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc02-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cc02-112">Return value</span></span>

<span data-ttu-id="1cc02-113">Si l’arrêt du fournisseur réussit, le rappel doit retourner la **\_ réussite** de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1cc02-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="1cc02-114">En cas d’échec, un code d’erreur approprié doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="1cc02-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc02-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc02-115">Requirements</span></span>



| <span data-ttu-id="1cc02-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc02-116">Requirement</span></span> | <span data-ttu-id="1cc02-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc02-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc02-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc02-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc02-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc02-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1cc02-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc02-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc02-121">Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cc02-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1cc02-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc02-123">Fonctions du serveur des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="1cc02-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="1cc02-124">*PxeProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="1cc02-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="1cc02-125">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="1cc02-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





