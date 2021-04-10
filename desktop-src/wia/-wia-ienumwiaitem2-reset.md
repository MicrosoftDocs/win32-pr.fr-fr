---
description: Réinitialise la référence d’énumération au premier objet IWiaItem2.
ms.assetid: 392e3471-f7fc-456f-a1cc-ab4eb6d3fe18
title: 'IEnumWiaItem2 :: Reset, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Reset
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ab4d5a9effbcb003265da53ddc753f63630df51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201672"
---
# <a name="ienumwiaitem2reset-method"></a><span data-ttu-id="cd8c7-103">IEnumWiaItem2 :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="cd8c7-103">IEnumWiaItem2::Reset method</span></span>

<span data-ttu-id="cd8c7-104">Réinitialise la référence d’énumération au premier objet [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="cd8c7-104">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd8c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd8c7-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="cd8c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd8c7-106">Parameters</span></span>

<span data-ttu-id="cd8c7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cd8c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd8c7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd8c7-108">Return value</span></span>

<span data-ttu-id="cd8c7-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd8c7-109">Type: **HRESULT**</span></span>

<span data-ttu-id="cd8c7-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8c7-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd8c7-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd8c7-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd8c7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd8c7-112">Requirements</span></span>



| <span data-ttu-id="cd8c7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd8c7-113">Requirement</span></span> | <span data-ttu-id="cd8c7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd8c7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd8c7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd8c7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cd8c7-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd8c7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cd8c7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd8c7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cd8c7-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd8c7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cd8c7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd8c7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd8c7-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c7-120"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd8c7-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="cd8c7-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd8c7-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c7-122"><dt>Wia.idl</dt></span></span> </dl> |



 

 




