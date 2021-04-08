---
title: CleanupCredentialCache fonction)
description: Implémenté par certains fournisseurs de support de sécurité (SSP) pour vider le cache des informations d’identification SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- CleanupCredentialCache fonction WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102928"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="8b6ac-104">CleanupCredentialCache fonction)</span><span class="sxs-lookup"><span data-stu-id="8b6ac-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="8b6ac-105">La fonction **CleanupCredentialCache** est implémentée par certains fournisseurs de support de sécurité (SSP) pour vider le cache des informations d’identification SSP.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b6ac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b6ac-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="8b6ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b6ac-107">Parameters</span></span>

<span data-ttu-id="8b6ac-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b6ac-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b6ac-109">Return value</span></span>

<span data-ttu-id="8b6ac-110">**True** si la fonction est réussie ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b6ac-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b6ac-111">Remarks</span></span>

<span data-ttu-id="8b6ac-112">La fonction **CleanupCredentialCache** est implémentée par les SSP suivants :</span><span class="sxs-lookup"><span data-stu-id="8b6ac-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="8b6ac-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="8b6ac-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="8b6ac-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="8b6ac-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="8b6ac-115">L’implémentation de **CleanupCredentialCache** par ces SSP retourne toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="8b6ac-116">Avant de tenter d’obtenir un handle de module pour exporter **CleanupCredentialCache**, l’application doit vérifier que le fournisseur de services partagés qui a été chargé est l’un des SSP connus qui implémente la fonction **CleanupCredentialCache** .</span><span class="sxs-lookup"><span data-stu-id="8b6ac-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="8b6ac-117">Pour vider le cache des informations d’identification SSP, l’application doit obtenir un handle de module pour le fournisseur de services partagés en appelant la fonction [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="8b6ac-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="8b6ac-118">Une fois le module obtenu, l’application doit exporter la fonction **CleanupCredentialCache** implémentée par le fournisseur de services partagés en appelant la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , en passant le module retourné par **GetModuleHandle** et **CleanupCredentialCache** en tant que paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="8b6ac-119">Comme tous les autres aspects de l’API WinINet, cette fonction ne peut pas être appelée en toute sécurité à partir de DllMain ou des constructeurs et des destructeurs d’objets globaux.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="8b6ac-120">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="8b6ac-121">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="8b6ac-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8b6ac-122">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8b6ac-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b6ac-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b6ac-123">Requirements</span></span>



| <span data-ttu-id="8b6ac-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b6ac-124">Requirement</span></span> | <span data-ttu-id="8b6ac-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b6ac-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b6ac-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b6ac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b6ac-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b6ac-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="8b6ac-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b6ac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b6ac-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b6ac-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="8b6ac-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8b6ac-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b6ac-131"><dt>MSNSSPC.dll ; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b6ac-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

