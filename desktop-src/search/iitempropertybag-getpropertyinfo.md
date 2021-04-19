---
description: Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés. L’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'IItemPropertyBag :: GetPropertyInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516619"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="d5958-104">IItemPropertyBag :: GetPropertyInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d5958-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="d5958-105">Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5958-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="d5958-106">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d5958-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5958-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5958-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="d5958-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5958-109">*nouvel IProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5958-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5958-110">Index de base zéro de la première propriété pour laquelle des informations sont demandées.</span><span class="sxs-lookup"><span data-stu-id="d5958-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="d5958-111">*cProperties* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5958-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5958-112">Nombre de propriétés pour lesquelles obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="d5958-112">The number of properties to get information for.</span></span> <span data-ttu-id="d5958-113">Cet argument spécifie le nombre d’éléments de tableau dans *pPropBag*.</span><span class="sxs-lookup"><span data-stu-id="d5958-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="d5958-114">*pPropBag* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5958-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5958-115">Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui reçoit les informations pour les propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5958-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="d5958-116">*pcProperties* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5958-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5958-117">Reçoit un pointeur vers une variable **ULong** qui reçoit le nombre de propriétés pour lesquelles des informations ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="d5958-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5958-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5958-118">Return value</span></span>

<span data-ttu-id="d5958-119">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5958-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d5958-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5958-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5958-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d5958-121">Remarks</span></span>

<span data-ttu-id="d5958-122">L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d5958-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d5958-123">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPropertyBag**](iitempropertybag.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d5958-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5958-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5958-124">Requirements</span></span>



| <span data-ttu-id="d5958-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5958-125">Requirement</span></span> | <span data-ttu-id="d5958-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5958-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5958-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5958-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5958-128">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5958-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d5958-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5958-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5958-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5958-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d5958-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d5958-131">Redistributable</span></span><br/>          | <span data-ttu-id="d5958-132">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d5958-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d5958-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5958-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5958-134">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="d5958-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




