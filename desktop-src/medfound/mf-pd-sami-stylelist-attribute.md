---
description: Contient les noms conviviaux des styles SAMI (Synchronized Accessible Media Interchange) définis dans le fichier SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Attribut MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868546"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="8823f-103">MF \_ PD \_ STYLELIST (attribut same) \_</span><span class="sxs-lookup"><span data-stu-id="8823f-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="8823f-104">Contient les noms conviviaux des styles SAMI (Synchronized Accessible Media Interchange) définis dans le fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="8823f-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="8823f-105">La [source du média sami](sami-media-source.md) définit cet attribut sur le descripteur de présentation qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="8823f-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="8823f-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="8823f-106">Data type</span></span>

<span data-ttu-id="8823f-107">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="8823f-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="8823f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8823f-108">Remarks</span></span>

<span data-ttu-id="8823f-109">L’objet blob d’attribut a la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="8823f-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="8823f-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="8823f-110">Data Type</span></span>

<span data-ttu-id="8823f-111">Description</span><span class="sxs-lookup"><span data-stu-id="8823f-111">Description</span></span>

<span data-ttu-id="8823f-112">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="8823f-112">Size (bytes)</span></span>

<span data-ttu-id="8823f-113">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="8823f-113">**DWORD**</span></span>

<span data-ttu-id="8823f-114">Nombre de chaînes de style.</span><span class="sxs-lookup"><span data-stu-id="8823f-114">Number of style strings.</span></span>

<span data-ttu-id="8823f-115">4</span><span class="sxs-lookup"><span data-stu-id="8823f-115">4</span></span>

<span data-ttu-id="8823f-116">Pour chaque chaîne de style :</span><span class="sxs-lookup"><span data-stu-id="8823f-116">For each style string:</span></span>

<span data-ttu-id="8823f-117">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="8823f-117">**DWORD**</span></span>

<span data-ttu-id="8823f-118">Taille de la chaîne en octets, y compris le caractère **null** .</span><span class="sxs-lookup"><span data-stu-id="8823f-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="8823f-119">4</span><span class="sxs-lookup"><span data-stu-id="8823f-119">4</span></span>

<span data-ttu-id="8823f-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="8823f-120">**LPWSTR**</span></span>

<span data-ttu-id="8823f-121">Chaîne de caractères larges se terminant par un caractère null et contenant le nom du style.</span><span class="sxs-lookup"><span data-stu-id="8823f-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="8823f-122">Variable</span><span class="sxs-lookup"><span data-stu-id="8823f-122">Varies</span></span>



 

<span data-ttu-id="8823f-123">Pour définir le style ou récupérer le style actuel, utilisez l’interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="8823f-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="8823f-124">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8823f-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="8823f-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="8823f-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="8823f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8823f-126">Requirements</span></span>



| <span data-ttu-id="8823f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8823f-127">Requirement</span></span> | <span data-ttu-id="8823f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8823f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8823f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8823f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8823f-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8823f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8823f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8823f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8823f-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8823f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8823f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="8823f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8823f-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8823f-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8823f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8823f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8823f-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8823f-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8823f-137">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="8823f-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="8823f-138">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="8823f-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="8823f-139">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8823f-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="8823f-140">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="8823f-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="8823f-141">Source du média SAMI</span><span class="sxs-lookup"><span data-stu-id="8823f-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




