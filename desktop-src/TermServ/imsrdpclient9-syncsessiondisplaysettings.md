---
title: Méthode IMsRdpClient9 SyncSessionDisplaySettings
description: Synchronise les paramètres d’affichage de la session.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SyncSessionDisplaySettings
- Méthode SyncSessionDisplaySettings Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SyncSessionDisplaySettings
- Méthode SyncSessionDisplaySettings Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941684"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="d1576-108">IMsRdpClient9 :: SyncSessionDisplaySettings, méthode</span><span class="sxs-lookup"><span data-stu-id="d1576-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="d1576-109">Synchronise les paramètres d’affichage de la session.</span><span class="sxs-lookup"><span data-stu-id="d1576-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1576-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1576-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="d1576-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1576-111">Parameters</span></span>

<span data-ttu-id="d1576-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d1576-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1576-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1576-113">Return value</span></span>

<span data-ttu-id="d1576-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d1576-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1576-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1576-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1576-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1576-116">Requirements</span></span>



| <span data-ttu-id="d1576-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1576-117">Requirement</span></span> | <span data-ttu-id="d1576-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1576-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1576-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1576-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d1576-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d1576-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d1576-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1576-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d1576-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d1576-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="d1576-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d1576-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1576-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1576-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="d1576-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1576-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1576-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1576-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="d1576-127">IID</span><span class="sxs-lookup"><span data-stu-id="d1576-127">IID</span></span><br/>                      | <span data-ttu-id="d1576-128">Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="d1576-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="d1576-129">Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="d1576-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="d1576-130">IID \_ IMsRdpClient9 est défini en tant que 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="d1576-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1576-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1576-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1576-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d1576-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d1576-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d1576-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





