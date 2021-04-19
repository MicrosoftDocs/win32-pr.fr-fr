---
title: PxeProviderServiceControl fonction de rappel
description: Appelée lorsqu’un code de contrôle de service est reçu par le service WDS.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Fonction de rappel PxeProviderServiceControl des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510321"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="b787c-104">PxeProviderServiceControl fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="b787c-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="b787c-105">Appelée lorsqu’un code de contrôle de service est reçu par le service WDS.</span><span class="sxs-lookup"><span data-stu-id="b787c-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="b787c-106">Cette fonction de rappel est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini sur le **contrôle du \_ \_ service \_ de rappel PXE**.</span><span class="sxs-lookup"><span data-stu-id="b787c-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b787c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b787c-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="b787c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b787c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b787c-109">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b787c-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b787c-110">Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="b787c-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="b787c-111">*dwControl*</span><span class="sxs-lookup"><span data-stu-id="b787c-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="b787c-112">Code de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b787c-112">Control code.</span></span> <span data-ttu-id="b787c-113">Pour obtenir la liste des valeurs possibles, consultez le paramètre *dwControl* de la fonction [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .</span><span class="sxs-lookup"><span data-stu-id="b787c-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b787c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b787c-114">Return value</span></span>

<span data-ttu-id="b787c-115">Si l’arrêt du fournisseur réussit, le rappel doit retourner la **\_ réussite** de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b787c-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="b787c-116">En cas d’échec, un code d’erreur approprié doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="b787c-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b787c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b787c-117">Requirements</span></span>



| <span data-ttu-id="b787c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b787c-118">Requirement</span></span> | <span data-ttu-id="b787c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b787c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b787c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b787c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b787c-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b787c-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b787c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b787c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b787c-123">Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b787c-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b787c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b787c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b787c-125">Fonctions du serveur des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="b787c-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="b787c-126">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="b787c-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

