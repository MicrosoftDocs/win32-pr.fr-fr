---
description: Ignore le nombre spécifié d’éléments au cours d’une énumération des objets IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2 :: Skip, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951340"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="e18ab-103">IEnumWiaItem2 :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="e18ab-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="e18ab-104">Ignore le nombre spécifié d’éléments au cours d’une énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="e18ab-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e18ab-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="e18ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e18ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18ab-107">*cElt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e18ab-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e18ab-108">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="e18ab-108">Type: **ULONG**</span></span>

<span data-ttu-id="e18ab-109">Spécifie le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="e18ab-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e18ab-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e18ab-110">Return value</span></span>

<span data-ttu-id="e18ab-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e18ab-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e18ab-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e18ab-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e18ab-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e18ab-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18ab-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e18ab-114">Requirements</span></span>



| <span data-ttu-id="e18ab-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e18ab-115">Requirement</span></span> | <span data-ttu-id="e18ab-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e18ab-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e18ab-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e18ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e18ab-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e18ab-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e18ab-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e18ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e18ab-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e18ab-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e18ab-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e18ab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18ab-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e18ab-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e18ab-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="e18ab-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e18ab-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e18ab-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




