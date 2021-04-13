---
description: Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés. L’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'IItemPropertyBag :: Read, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318153"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="8ca0f-104">IItemPropertyBag :: Read, méthode</span><span class="sxs-lookup"><span data-stu-id="8ca0f-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="8ca0f-105">Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="8ca0f-106">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ca0f-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="8ca0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ca0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca0f-109">*cProperties* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0f-110">Nombre de propriétés à lire.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-110">The number of properties to read.</span></span> <span data-ttu-id="8ca0f-111">Cet argument spécifie le nombre d’éléments dans les tableaux à *pPropBag*, *pvarValue* et *phrError*.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="8ca0f-112">*pPropBag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0f-113">Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui spécifie les propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="8ca0f-114">*pvarValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0f-115">Reçoit un pointeur qui retourne un tableau de structures **Variant** qui reçoit les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="8ca0f-116">*phrError* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0f-117">Pointeur vers un tableau de valeurs **HRESULT** qui reçoit le résultat de chaque lecture de propriété.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="8ca0f-118">Il doit y avoir au moins éléments *cProperties* dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca0f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ca0f-119">Return value</span></span>

<span data-ttu-id="8ca0f-120">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="8ca0f-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ca0f-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca0f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8ca0f-122">Remarks</span></span>

<span data-ttu-id="8ca0f-123">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8ca0f-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="8ca0f-124">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPropertyBag**](iitempropertybag.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="8ca0f-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca0f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ca0f-125">Requirements</span></span>



| <span data-ttu-id="8ca0f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ca0f-126">Requirement</span></span> | <span data-ttu-id="8ca0f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ca0f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ca0f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ca0f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca0f-129">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8ca0f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ca0f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca0f-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ca0f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8ca0f-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8ca0f-132">Redistributable</span></span><br/>          | <span data-ttu-id="8ca0f-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="8ca0f-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8ca0f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ca0f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca0f-135">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="8ca0f-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




