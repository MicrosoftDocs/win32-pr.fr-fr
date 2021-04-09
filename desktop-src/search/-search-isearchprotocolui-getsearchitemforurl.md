---
description: Obtient l’élément de recherche pour les données spécifiées. Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'ISearchProtocolUI :: GetSearchItemForUrl, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750397"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="8fa07-104">ISearchProtocolUI :: GetSearchItemForUrl, méthode</span><span class="sxs-lookup"><span data-stu-id="8fa07-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="8fa07-105">Obtient l’élément de recherche pour les données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8fa07-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="8fa07-106">Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8fa07-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fa07-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="8fa07-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fa07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fa07-109">*pcwszURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fa07-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa07-110">Type : **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="8fa07-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="8fa07-111">Pointeur vers une chaîne Unicode terminée par des données NULL contenant l’élément de recherche pour l’URL accédée.</span><span class="sxs-lookup"><span data-stu-id="8fa07-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="8fa07-112">*pPropertyBag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fa07-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa07-113">Tapez : \**IItemPropertyBag \** _</span><span class="sxs-lookup"><span data-stu-id="8fa07-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="8fa07-114">Pointeur vers un objet [_ *IItemPropertyBag* \*](iitempropertybag.md) qui contient des informations sur l’élément de recherche, y compris les propriétés de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8fa07-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="8fa07-115">*ppSearchItem* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8fa07-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa07-116">Type : **[ **ISearchItem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8fa07-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="8fa07-117">Reçoit l’adresse d’un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) créé par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8fa07-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="8fa07-118">Cet objet contient des informations sur l’élément de recherche, telles que le nom de fichier de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8fa07-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fa07-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fa07-119">Return value</span></span>

<span data-ttu-id="8fa07-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8fa07-120">Type: **HRESULT**</span></span>

<span data-ttu-id="8fa07-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8fa07-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8fa07-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fa07-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fa07-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8fa07-123">Remarks</span></span>

<span data-ttu-id="8fa07-124">La méthode **ISearchProtocolUI :: GetSearchItemForUrl** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8fa07-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="8fa07-125">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**ISearchProtocolUI**](-search-isearchprotocolui.md) et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="8fa07-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa07-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fa07-126">Requirements</span></span>



| <span data-ttu-id="8fa07-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fa07-127">Requirement</span></span> | <span data-ttu-id="8fa07-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fa07-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8fa07-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fa07-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa07-130">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fa07-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8fa07-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fa07-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa07-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fa07-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8fa07-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8fa07-133">Redistributable</span></span><br/>          | <span data-ttu-id="8fa07-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="8fa07-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8fa07-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fa07-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa07-136">**ISearchProtocolUI**</span><span class="sxs-lookup"><span data-stu-id="8fa07-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




