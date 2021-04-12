---
title: Méthode IMsTscAxEvents OnRemoteWindowDisplayed
description: Appelé lorsqu’une fenêtre RemoteApp est affichée.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteWindowDisplayed
- Méthode OnRemoteWindowDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384880"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="a74c7-106">IMsTscAxEvents :: OnRemoteWindowDisplayed, méthode</span><span class="sxs-lookup"><span data-stu-id="a74c7-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="a74c7-107">Appelé lorsqu’une fenêtre RemoteApp est affichée.</span><span class="sxs-lookup"><span data-stu-id="a74c7-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74c7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a74c7-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="a74c7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a74c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74c7-110">*vbDisplayed* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a74c7-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74c7-111">Type : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a74c7-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="a74c7-112">Indique si la fenêtre RemoteApp est affichée ou masquée.</span><span class="sxs-lookup"><span data-stu-id="a74c7-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="a74c7-113">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a74c7-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74c7-114">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="a74c7-114">Type: **HWND**</span></span>

<span data-ttu-id="a74c7-115">Handle de la fenêtre affichée.</span><span class="sxs-lookup"><span data-stu-id="a74c7-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a74c7-116">*windowAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a74c7-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74c7-117">Type : **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="a74c7-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="a74c7-118">Valeur de l’énumération [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) qui spécifie plus d’informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="a74c7-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74c7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a74c7-119">Return value</span></span>

<span data-ttu-id="a74c7-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a74c7-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74c7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a74c7-121">Requirements</span></span>



| <span data-ttu-id="a74c7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a74c7-122">Requirement</span></span> | <span data-ttu-id="a74c7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a74c7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a74c7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a74c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a74c7-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a74c7-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a74c7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a74c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a74c7-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a74c7-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a74c7-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a74c7-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a74c7-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74c7-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a74c7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a74c7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74c7-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74c7-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74c7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a74c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74c7-133">**RemoteWindowDisplayedAttribute**</span><span class="sxs-lookup"><span data-stu-id="a74c7-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="a74c7-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="a74c7-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





