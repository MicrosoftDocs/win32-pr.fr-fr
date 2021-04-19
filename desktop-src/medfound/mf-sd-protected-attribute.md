---
description: Indique si un flux de données contient du contenu protégé.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Attribut MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536870"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="db8f6-103">\_ \_ Attribut protégé SD MF</span><span class="sxs-lookup"><span data-stu-id="db8f6-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="db8f6-104">Indique si un flux de données contient du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="db8f6-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="db8f6-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="db8f6-105">Data type</span></span>

<span data-ttu-id="db8f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="db8f6-106">**UINT32**</span></span>

<span data-ttu-id="db8f6-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="db8f6-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db8f6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="db8f6-108">Remarks</span></span>

<span data-ttu-id="db8f6-109">Cet attribut s’applique aux descripteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="db8f6-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="db8f6-110">Si la valeur de l’attribut est **true**, le flux de données contient du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="db8f6-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="db8f6-111">Si la valeur est **false** ou si l’attribut n’est pas défini, le flux contient du contenu clair.</span><span class="sxs-lookup"><span data-stu-id="db8f6-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="db8f6-112">Au lieu de vérifier chaque flux pour cet attribut, vous pouvez passer un descripteur de présentation à la fonction [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) .</span><span class="sxs-lookup"><span data-stu-id="db8f6-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="db8f6-113">Cette fonction vérifie si le descripteur de présentation contient des flux protégés.</span><span class="sxs-lookup"><span data-stu-id="db8f6-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="db8f6-114">Une source de média doit définir cet attribut sur le descripteur de flux si le contenu requiert le chemin d’accès de média protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="db8f6-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="db8f6-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="db8f6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="db8f6-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="db8f6-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="db8f6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db8f6-117">Requirements</span></span>



| <span data-ttu-id="db8f6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db8f6-118">Requirement</span></span> | <span data-ttu-id="db8f6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="db8f6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db8f6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db8f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db8f6-121">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="db8f6-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="db8f6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db8f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db8f6-123">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="db8f6-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="db8f6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="db8f6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db8f6-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8f6-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8f6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db8f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8f6-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db8f6-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db8f6-128">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="db8f6-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="db8f6-129">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="db8f6-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="db8f6-130">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="db8f6-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="db8f6-131">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="db8f6-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




