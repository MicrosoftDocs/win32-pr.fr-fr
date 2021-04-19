---
title: Méthode ITSRemoteProgram3 ServerStartApp
description: Spécifie une application à démarrer dans la session à distance.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ServerStartApp
- Méthode ServerStartApp Services Bureau à distance, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, méthode ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106545757"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="8fe7a-106">ITSRemoteProgram3 :: ServerStartApp, méthode</span><span class="sxs-lookup"><span data-stu-id="8fe7a-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="8fe7a-107">Spécifie une application à démarrer dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="8fe7a-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe7a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fe7a-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="8fe7a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fe7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe7a-110">*bstrAppUserModelId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7a-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fe7a-111">*bstrArguments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7a-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8fe7a-112">*vbExpandEnvVarInArgumentsOnServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7a-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="8fe7a-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fe7a-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="8fe7a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fe7a-114">Return value</span></span>

<span data-ttu-id="8fe7a-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8fe7a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8fe7a-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fe7a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe7a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe7a-117">Requirements</span></span>



| <span data-ttu-id="8fe7a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe7a-118">Requirement</span></span> | <span data-ttu-id="8fe7a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe7a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe7a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe7a-121">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe7a-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8fe7a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe7a-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8fe7a-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="8fe7a-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8fe7a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8fe7a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe7a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8fe7a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe7a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe7a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe7a-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe7a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe7a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe7a-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="8fe7a-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





