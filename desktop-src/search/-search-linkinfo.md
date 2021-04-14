---
description: Stocke des informations sur les types de liens et est utilisé par l’interface IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: LINKINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201299"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="15976-103">LINKINFO, structure</span><span class="sxs-lookup"><span data-stu-id="15976-103">LINKINFO structure</span></span>

<span data-ttu-id="15976-104">\[**LINKINFO** et [**IItemPreviewerExt**](-search-iitempreviewerext.md) sont pris en charge uniquement sur Windows XP et Windows Server 2003 et ne doivent plus être utilisés.\]</span><span class="sxs-lookup"><span data-stu-id="15976-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="15976-105">Stocke des informations sur les types de liens et est utilisé par l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) .</span><span class="sxs-lookup"><span data-stu-id="15976-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="15976-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15976-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="15976-107">Membres</span><span class="sxs-lookup"><span data-stu-id="15976-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="15976-108">**type**</span><span class="sxs-lookup"><span data-stu-id="15976-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="15976-109">Type : **[ **LinkType**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="15976-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15976-110">Type de lien spécifié lors de l’analyse ou de l’indexation indiqué par une constante [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="15976-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="15976-111">**bstrContentType**</span><span class="sxs-lookup"><span data-stu-id="15976-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="15976-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15976-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15976-113">Valeur **BSTR** qui spécifie le type de contenu.</span><span class="sxs-lookup"><span data-stu-id="15976-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="15976-114">**bstrEncoding**</span><span class="sxs-lookup"><span data-stu-id="15976-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="15976-115">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15976-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15976-116">Attribut EncodingStyle spécifié dans le fichier Web Services Description Language (WSDL).</span><span class="sxs-lookup"><span data-stu-id="15976-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="15976-117">**bstrFileExt**</span><span class="sxs-lookup"><span data-stu-id="15976-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="15976-118">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15976-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15976-119">Valeur **BSTR** qui spécifie l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="15976-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="15976-120">**varData**</span><span class="sxs-lookup"><span data-stu-id="15976-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="15976-121">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="15976-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="15976-122">Variant qui spécifie la valeur de la variable.</span><span class="sxs-lookup"><span data-stu-id="15976-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="15976-123">**dwRelatedParts**</span><span class="sxs-lookup"><span data-stu-id="15976-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="15976-124">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="15976-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="15976-125">**Valeur DWORD** qui spécifie les parties associées.</span><span class="sxs-lookup"><span data-stu-id="15976-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="15976-126">**bstrRelatedCid**</span><span class="sxs-lookup"><span data-stu-id="15976-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="15976-127">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15976-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15976-128">Valeur **BSTR** qui spécifie une propriété CID, une chaîne décimale non complétée et signée.</span><span class="sxs-lookup"><span data-stu-id="15976-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="15976-129">**lCodePage**</span><span class="sxs-lookup"><span data-stu-id="15976-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="15976-130">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="15976-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="15976-131">Page de codes à utiliser pour l’encodage de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="15976-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15976-132">Notes</span><span class="sxs-lookup"><span data-stu-id="15976-132">Remarks</span></span>

<span data-ttu-id="15976-133">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser la structure **LINKINFO** et les API suivantes : les méthodes [**IItemPreviewerExt :: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) et [**IItemPreviewerExt :: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="15976-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="15976-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15976-134">Requirements</span></span>



| <span data-ttu-id="15976-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15976-135">Requirement</span></span> | <span data-ttu-id="15976-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="15976-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15976-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15976-137">Minimum supported client</span></span><br/> | <span data-ttu-id="15976-138">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15976-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="15976-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15976-139">Minimum supported server</span></span><br/> | <span data-ttu-id="15976-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15976-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="15976-141">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="15976-141">Redistributable</span></span><br/>          | <span data-ttu-id="15976-142">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="15976-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




