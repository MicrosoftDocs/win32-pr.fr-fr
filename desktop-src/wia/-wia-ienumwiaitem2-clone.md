---
description: Crée une instance supplémentaire de l’interface IEnumWiaItem2 et retourne un pointeur vers celui-ci.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2 :: Clone, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752869"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="9aba4-103">IEnumWiaItem2 :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="9aba4-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="9aba4-104">Crée une instance supplémentaire de l’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) et retourne un pointeur vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="9aba4-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aba4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9aba4-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9aba4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9aba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aba4-107">*ppIEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9aba4-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba4-108">Type : **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9aba4-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="9aba4-109">Reçoit l’adresse de l’instance d’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **IEnumWiaItem2 :: Clone** crée.</span><span class="sxs-lookup"><span data-stu-id="9aba4-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aba4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9aba4-110">Return value</span></span>

<span data-ttu-id="9aba4-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9aba4-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9aba4-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9aba4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aba4-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9aba4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aba4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9aba4-114">Remarks</span></span>

<span data-ttu-id="9aba4-115">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="9aba4-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aba4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9aba4-116">Requirements</span></span>



| <span data-ttu-id="9aba4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9aba4-117">Requirement</span></span> | <span data-ttu-id="9aba4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9aba4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9aba4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9aba4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9aba4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9aba4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9aba4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9aba4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9aba4-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9aba4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9aba4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9aba4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aba4-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aba4-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aba4-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="9aba4-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9aba4-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9aba4-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
