---
description: Obtient le composant WIA (Windows Image Acquisition) 2,0 Preview.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2 :: GetPreviewComponent, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113306"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="95972-103">IWiaItem2 :: GetPreviewComponent, méthode</span><span class="sxs-lookup"><span data-stu-id="95972-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="95972-104">Obtient le composant WIA (Windows Image Acquisition) 2,0 Preview.</span><span class="sxs-lookup"><span data-stu-id="95972-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="95972-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95972-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="95972-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95972-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95972-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95972-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="95972-108">Type: **LONG**</span></span>

<span data-ttu-id="95972-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="95972-109">Not used.</span></span> <span data-ttu-id="95972-110">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="95972-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="95972-111">*ppWiaPreview* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="95972-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95972-112">Type : **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="95972-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="95972-113">Retourne l’adresse d’un pointeur vers l’interface [**IWiaPreview**](-wia-iwiapreview.md) du composant d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="95972-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95972-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95972-114">Return value</span></span>

<span data-ttu-id="95972-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="95972-115">Type: **HRESULT**</span></span>

<span data-ttu-id="95972-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95972-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95972-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95972-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95972-118">Notes</span><span class="sxs-lookup"><span data-stu-id="95972-118">Remarks</span></span>

<span data-ttu-id="95972-119">Utilisez cette fonction pour retourner un pointeur vers l’adresse du composant WIA 2,0 Preview pour tout objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence d’objets d’un périphérique matériel WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="95972-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="95972-120">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppWiaPreview* .</span><span class="sxs-lookup"><span data-stu-id="95972-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="95972-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95972-121">Requirements</span></span>



| <span data-ttu-id="95972-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95972-122">Requirement</span></span> | <span data-ttu-id="95972-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="95972-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95972-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95972-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95972-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95972-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95972-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95972-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95972-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95972-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95972-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="95972-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95972-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="95972-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="95972-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="95972-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95972-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95972-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95972-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95972-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95972-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="95972-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="95972-134">**IWiaPreview**</span><span class="sxs-lookup"><span data-stu-id="95972-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
