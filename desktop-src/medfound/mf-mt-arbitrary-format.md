---
description: Données de format supplémentaires pour un flux binaire dans un fichier ASF (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Attribut MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529185"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="ba77c-103">\_Attribut de \_ format arbitraire MT \_ MF</span><span class="sxs-lookup"><span data-stu-id="ba77c-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="ba77c-104">Données de format supplémentaires pour un flux binaire dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ba77c-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba77c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ba77c-105">Data type</span></span>

<span data-ttu-id="ba77c-106">**POIDS\[\]**</span><span class="sxs-lookup"><span data-stu-id="ba77c-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="ba77c-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ba77c-107">Get/set</span></span>

<span data-ttu-id="ba77c-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="ba77c-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="ba77c-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="ba77c-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba77c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ba77c-110">Remarks</span></span>

<span data-ttu-id="ba77c-111">Les applications peuvent utiliser des flux binaires pour contenir des types de données personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ba77c-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="ba77c-112">La source de média ASF traite la valeur de cet attribut comme un objet blob opaque.</span><span class="sxs-lookup"><span data-stu-id="ba77c-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="ba77c-113">Le membre **formatType** de la structure d' [**\_ \_ en-tête arbitraire MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) définit la disposition des données de format.</span><span class="sxs-lookup"><span data-stu-id="ba77c-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="ba77c-114">Cette structure correspond au champ de données de format des données spécifiques au type dans l’objet de propriétés de flux, dans les fichiers où le type de flux est un **\_ \_ média binaire ASF**.</span><span class="sxs-lookup"><span data-stu-id="ba77c-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="ba77c-115">Pour plus d’informations, consultez la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="ba77c-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="ba77c-116">Dans le kit de développement logiciel (SDK) Windows Media format, les flux binaires sont appelés des *flux arbitraires* ou des *flux de données arbitraires*.</span><span class="sxs-lookup"><span data-stu-id="ba77c-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="ba77c-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ba77c-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba77c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba77c-118">Requirements</span></span>



| <span data-ttu-id="ba77c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba77c-119">Requirement</span></span> | <span data-ttu-id="ba77c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba77c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba77c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba77c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba77c-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba77c-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ba77c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba77c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba77c-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba77c-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ba77c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba77c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba77c-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba77c-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba77c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba77c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba77c-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba77c-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba77c-129">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="ba77c-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba77c-130">\_ \_ \_ en-tête arbitraire MT</span><span class="sxs-lookup"><span data-stu-id="ba77c-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




