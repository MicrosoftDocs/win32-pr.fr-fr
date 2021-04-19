---
description: Autorise l’extension à du contenu riche pour une propriété.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'IItemPreviewerExt :: GetLinkedContent, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516841"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="d7387-103">IItemPreviewerExt :: GetLinkedContent, méthode</span><span class="sxs-lookup"><span data-stu-id="d7387-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="d7387-104">Autorise l’extension à du contenu riche pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="d7387-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7387-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7387-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d7387-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7387-107">*dwContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7387-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7387-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d7387-108">Type: **DWORD**</span></span>

<span data-ttu-id="d7387-109">Identificateur de contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d7387-109">The context identifier for the operation.</span></span> <span data-ttu-id="d7387-110">Remplacez la valeur par défaut de *dwContext* pour définir l’identificateur de contexte sur la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d7387-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="d7387-111">*pwszProp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7387-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7387-112">Type : **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="d7387-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="d7387-113">Pointeur vers la propriété du contenu lié sous la forme d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="d7387-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="d7387-114">*pinfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d7387-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d7387-115">Tapez : \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d7387-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="d7387-116">Reçoit un pointeur vers la structure [_ *LINKINFO* \*](-search-linkinfo.md) dans laquelle la méthode retourne des informations sur la transaction.</span><span class="sxs-lookup"><span data-stu-id="d7387-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="d7387-117">*pinfo* ne doit pas être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="d7387-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7387-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7387-118">Return value</span></span>

<span data-ttu-id="d7387-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7387-119">Type: **HRESULT**</span></span>

<span data-ttu-id="d7387-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d7387-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7387-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7387-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7387-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d7387-122">Remarks</span></span>

<span data-ttu-id="d7387-123">L’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d7387-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d7387-124">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d7387-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7387-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7387-125">Requirements</span></span>



| <span data-ttu-id="d7387-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7387-126">Requirement</span></span> | <span data-ttu-id="d7387-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7387-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7387-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7387-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7387-129">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7387-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7387-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7387-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7387-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7387-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7387-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d7387-132">Redistributable</span></span><br/>          | <span data-ttu-id="d7387-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d7387-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d7387-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7387-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7387-135">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="d7387-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




