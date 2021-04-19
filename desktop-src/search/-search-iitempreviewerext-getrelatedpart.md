---
description: Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'IItemPreviewerExt :: GetRelatedPart, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513984"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="5df56-103">IItemPreviewerExt :: GetRelatedPart, méthode</span><span class="sxs-lookup"><span data-stu-id="5df56-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="5df56-104">Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.</span><span class="sxs-lookup"><span data-stu-id="5df56-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5df56-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5df56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5df56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df56-107">*dwContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5df56-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df56-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5df56-108">Type: **DWORD**</span></span>

<span data-ttu-id="5df56-109">Identificateur de contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5df56-109">The context identifier for the operation.</span></span> <span data-ttu-id="5df56-110">Remplacez la valeur par défaut de **dwContext** pour définir l’identificateur de contexte sur la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="5df56-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="5df56-111">*pwszProp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5df56-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df56-112">Type : **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="5df56-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="5df56-113">Pointeur vers la propriété du contenu lié sous la forme d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="5df56-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="5df56-114">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5df56-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df56-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5df56-115">Type: **DWORD**</span></span>

<span data-ttu-id="5df56-116">Valeur d’entier long non signé qui contient l’index de base zéro de la partie du corps associée.</span><span class="sxs-lookup"><span data-stu-id="5df56-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="5df56-117">*pinfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5df56-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5df56-118">Tapez : \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="5df56-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="5df56-119">Reçoit un pointeur vers la structure [_ *LINKINFO* \*](-search-linkinfo.md) dans laquelle la méthode retourne des informations sur la transaction.</span><span class="sxs-lookup"><span data-stu-id="5df56-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="5df56-120">*pinfo* ne doit pas être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="5df56-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df56-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5df56-121">Return value</span></span>

<span data-ttu-id="5df56-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5df56-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5df56-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5df56-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5df56-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5df56-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df56-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5df56-125">Remarks</span></span>

<span data-ttu-id="5df56-126">L’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5df56-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="5df56-127">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="5df56-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df56-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5df56-128">Requirements</span></span>



| <span data-ttu-id="5df56-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5df56-129">Requirement</span></span> | <span data-ttu-id="5df56-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5df56-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5df56-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5df56-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5df56-132">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5df56-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5df56-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5df56-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5df56-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5df56-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5df56-135">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5df56-135">Redistributable</span></span><br/>          | <span data-ttu-id="5df56-136">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="5df56-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5df56-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5df56-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df56-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="5df56-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




