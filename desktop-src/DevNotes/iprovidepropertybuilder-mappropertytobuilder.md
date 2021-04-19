---
description: Vérifie si un générateur doit être associé à une propriété particulière.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'IProvidePropertyBuilder :: MapPropertyToBuilder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532753"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="cc47c-103">IProvidePropertyBuilder :: MapPropertyToBuilder, méthode</span><span class="sxs-lookup"><span data-stu-id="cc47c-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="cc47c-104">Vérifie si un générateur doit être associé à une propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="cc47c-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc47c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc47c-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="cc47c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc47c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc47c-107">*DISPID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc47c-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc47c-108">DISPID de la propriété en question.</span><span class="sxs-lookup"><span data-stu-id="cc47c-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="cc47c-109">*pdwCtlBldType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc47c-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc47c-110">Générateur à mapper.</span><span class="sxs-lookup"><span data-stu-id="cc47c-110">The builder to be mapped.</span></span> <span data-ttu-id="cc47c-111">Ce paramètre peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc47c-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="cc47c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc47c-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="cc47c-113">Signification</span><span class="sxs-lookup"><span data-stu-id="cc47c-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="cc47c-114"><dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cc47c-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="cc47c-115">Appeler un générateur de système standard (non pris en charge dans Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="cc47c-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="cc47c-116"><dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cc47c-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="cc47c-117">Appelle un générateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="cc47c-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="cc47c-118"><dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cc47c-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="cc47c-119">Le concepteur modifie l'objet.</span><span class="sxs-lookup"><span data-stu-id="cc47c-119">Builder modifies the object.</span></span> <span data-ttu-id="cc47c-120">Il s'agit d'un comportement commun.</span><span class="sxs-lookup"><span data-stu-id="cc47c-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="cc47c-121">*pbstrGuidBldr* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc47c-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc47c-122">GUID qui identifie le générateur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="cc47c-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="cc47c-123">*builderAvailable* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cc47c-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cc47c-124">Ce paramètre a la **valeur true** si cette propriété prend actuellement en charge un générateur.</span><span class="sxs-lookup"><span data-stu-id="cc47c-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc47c-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc47c-125">Return value</span></span>

<span data-ttu-id="cc47c-126">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc47c-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc47c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc47c-127">Requirements</span></span>



| <span data-ttu-id="cc47c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc47c-128">Requirement</span></span> | <span data-ttu-id="cc47c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc47c-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc47c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cc47c-130">DLL</span></span><br/> | <dl> <span data-ttu-id="cc47c-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc47c-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc47c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc47c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc47c-133">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="cc47c-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




