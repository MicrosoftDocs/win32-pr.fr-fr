---
title: Méthode IMsTscAxEvents OnWarning
description: Appelé lorsque le contrôle client rencontre une condition d’erreur qui n’est pas irrécupérable.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnWarning
- Méthode OnWarning Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742084"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="f2659-106">IMsTscAxEvents :: OnWarning, méthode</span><span class="sxs-lookup"><span data-stu-id="f2659-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="f2659-107">Appelé lorsque le contrôle client rencontre une condition d’erreur qui n’est pas irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="f2659-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2659-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2659-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="f2659-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2659-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2659-110">*WarningCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2659-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2659-111">Code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="f2659-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="f2659-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f2659-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f2659-113">Le cache bitmap est endommagé.</span><span class="sxs-lookup"><span data-stu-id="f2659-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2659-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2659-114">Return value</span></span>

<span data-ttu-id="f2659-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2659-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2659-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f2659-116">Remarks</span></span>

<span data-ttu-id="f2659-117">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f2659-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2659-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2659-118">Requirements</span></span>



| <span data-ttu-id="f2659-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2659-119">Requirement</span></span> | <span data-ttu-id="f2659-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2659-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2659-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2659-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2659-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2659-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f2659-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2659-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2659-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2659-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f2659-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f2659-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2659-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2659-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2659-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f2659-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2659-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2659-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2659-129">IID</span><span class="sxs-lookup"><span data-stu-id="f2659-129">IID</span></span><br/>                      | <span data-ttu-id="f2659-130">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f2659-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f2659-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2659-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2659-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f2659-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





