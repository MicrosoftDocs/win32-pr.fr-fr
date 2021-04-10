---
description: Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés. L’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'IItemPropertyBag :: Write, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112391"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="a35a9-104">IItemPropertyBag :: Write, méthode</span><span class="sxs-lookup"><span data-stu-id="a35a9-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="a35a9-105">Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a35a9-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="a35a9-106">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a35a9-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a35a9-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="a35a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a35a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a35a9-109">*cProperties* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35a9-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35a9-110">Nombre de propriétés à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="a35a9-110">The number of properties to save.</span></span> <span data-ttu-id="a35a9-111">Cet argument spécifie le nombre d’éléments dans les tableaux à *pPropBag* et *pvarValue*.</span><span class="sxs-lookup"><span data-stu-id="a35a9-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="a35a9-112">*pPropBag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35a9-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35a9-113">Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui spécifie les propriétés à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="a35a9-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="a35a9-114">*pvarValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a35a9-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35a9-115">Pointeur vers un **Variant** dont le type dépend du type de données des informations de propriété qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="a35a9-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a35a9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a35a9-116">Return value</span></span>

<span data-ttu-id="a35a9-117">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a35a9-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="a35a9-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a35a9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35a9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a35a9-119">Remarks</span></span>

<span data-ttu-id="a35a9-120">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a35a9-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a35a9-121">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPropertyBag**](iitempropertybag.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="a35a9-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35a9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a35a9-122">Requirements</span></span>



| <span data-ttu-id="a35a9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a35a9-123">Requirement</span></span> | <span data-ttu-id="a35a9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a35a9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a35a9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a35a9-126">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a35a9-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a35a9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a35a9-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a35a9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a35a9-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a35a9-129">Redistributable</span></span><br/>          | <span data-ttu-id="a35a9-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a35a9-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a35a9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a35a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35a9-132">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="a35a9-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




