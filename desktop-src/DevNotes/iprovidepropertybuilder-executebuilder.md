---
description: Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'IProvidePropertyBuilder :: ExecuteBuilder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530410"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="8743d-103">IProvidePropertyBuilder :: ExecuteBuilder, méthode</span><span class="sxs-lookup"><span data-stu-id="8743d-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="8743d-104">Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8743d-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8743d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8743d-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="8743d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8743d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8743d-107">*DISPID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8743d-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-108">DISPID de la propriété pour laquelle le générateur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8743d-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="8743d-109">*bstrGuidBldr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8743d-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-110">**BSTR** du GUID du générateur à appeler.</span><span class="sxs-lookup"><span data-stu-id="8743d-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="8743d-111">Elle est retournée par [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="8743d-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="8743d-112">*pdispApp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8743d-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-113">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8743d-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8743d-114">*hwndBldrOwner* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8743d-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-115">Handle vers la fenêtre du générateur de fenêtres publicitaires parente.</span><span class="sxs-lookup"><span data-stu-id="8743d-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="8743d-116">*pvarValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8743d-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-117">Valeur actuelle de la propriété.</span><span class="sxs-lookup"><span data-stu-id="8743d-117">The current value of the property.</span></span> <span data-ttu-id="8743d-118">Cette valeur peut être modifiée par l’objet et remplacée par la nouvelle valeur si *pbActionCommitted* a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="8743d-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8743d-119">*pbActionCommitted* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8743d-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8743d-120">Valeur qui indique si le générateur A effectué une action sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="8743d-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="8743d-121">Peut être utilisé lorsqu’un utilisateur modifie un événement, puis appuie sur OK dans la boîte de dialogue du générateur de fenêtres publicitaires.</span><span class="sxs-lookup"><span data-stu-id="8743d-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8743d-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8743d-122">Return value</span></span>

<span data-ttu-id="8743d-123">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8743d-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8743d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8743d-124">Requirements</span></span>



| <span data-ttu-id="8743d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8743d-125">Requirement</span></span> | <span data-ttu-id="8743d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8743d-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8743d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8743d-127">DLL</span></span><br/> | <dl> <span data-ttu-id="8743d-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8743d-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8743d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8743d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8743d-130">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="8743d-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




