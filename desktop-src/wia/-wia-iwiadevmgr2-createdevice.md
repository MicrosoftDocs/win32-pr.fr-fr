---
description: Crée une arborescence hiérarchique d’objets IWiaItem2 pour un appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2 :: CreateDevice, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865253"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="490ec-103">IWiaDevMgr2 :: CreateDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="490ec-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="490ec-104">Crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour un appareil WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="490ec-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="490ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="490ec-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="490ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="490ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490ec-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="490ec-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="490ec-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="490ec-108">Type: **LONG**</span></span>

<span data-ttu-id="490ec-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="490ec-109">Currently unused.</span></span> <span data-ttu-id="490ec-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="490ec-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="490ec-111">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="490ec-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="490ec-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="490ec-112">Type: **BSTR**</span></span>

<span data-ttu-id="490ec-113">Spécifie l’identificateur unique de l’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="490ec-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="490ec-114">*ppWiaItem2Root* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="490ec-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="490ec-115">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="490ec-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="490ec-116">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine de l’arborescence hiérarchique pour l’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="490ec-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490ec-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="490ec-117">Return value</span></span>

<span data-ttu-id="490ec-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="490ec-118">Type: **HRESULT**</span></span>

<span data-ttu-id="490ec-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="490ec-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="490ec-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="490ec-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="490ec-121">Notes</span><span class="sxs-lookup"><span data-stu-id="490ec-121">Remarks</span></span>

<span data-ttu-id="490ec-122">Les applications utilisent la méthode **IWiaDevMgr2 :: CreateDevice** pour créer un objet appareil pour les appareils WIA 2,0 spécifiés par le paramètre bstrDeviceID.</span><span class="sxs-lookup"><span data-stu-id="490ec-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="490ec-123">Quand elle retourne, la méthode **IWiaDevMgr2 :: CreateDevice** stocke l’adresse d’un pointeur dans le paramètre *ppWiaItem2Root*, qui pointe vers l’élément racine de l’arborescence des objets [**IWiaItem2**](-wia-iwiaitem2.md) créés par **IWiaDevMgr2 :: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="490ec-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="490ec-124">Les applications peuvent utiliser cette arborescence d’objets pour contrôler et récupérer des données à partir de l’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="490ec-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="490ec-125">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs qu’elles reçoivent via le paramètre *ppWiaItem2Root* .</span><span class="sxs-lookup"><span data-stu-id="490ec-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="490ec-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="490ec-126">Requirements</span></span>



| <span data-ttu-id="490ec-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="490ec-127">Requirement</span></span> | <span data-ttu-id="490ec-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="490ec-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="490ec-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="490ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="490ec-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="490ec-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="490ec-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="490ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="490ec-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="490ec-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="490ec-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="490ec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="490ec-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="490ec-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="490ec-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="490ec-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="490ec-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="490ec-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
