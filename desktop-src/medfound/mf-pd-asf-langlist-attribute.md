---
description: Spécifie une liste d’identificateurs de langue qui spécifie les langues contenues dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de langages, défini dans la spécification ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: Attribut MF_PD_ASF_LANGLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521844"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="a8dc0-104">\_ \_ Attribut LANGLIST MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="a8dc0-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="a8dc0-105">Spécifie une liste d’identificateurs de langue qui spécifie les langues contenues dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a8dc0-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a8dc0-106">Cet attribut correspond à l’objet de liste de langages, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8dc0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a8dc0-107">Data type</span></span>

<span data-ttu-id="a8dc0-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="a8dc0-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a8dc0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a8dc0-109">Remarks</span></span>

<span data-ttu-id="a8dc0-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a8dc0-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’en-tête d’objet de liste de langage.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="a8dc0-112">Le tableau suivant indique le format de l’objet BLOB :</span><span class="sxs-lookup"><span data-stu-id="a8dc0-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="a8dc0-113">Champ de l’objet de liste de langues</span><span class="sxs-lookup"><span data-stu-id="a8dc0-113">Language List Object field</span></span> | <span data-ttu-id="a8dc0-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="a8dc0-114">Data type</span></span>    | <span data-ttu-id="a8dc0-115">Taille</span><span class="sxs-lookup"><span data-stu-id="a8dc0-115">Size</span></span>    | <span data-ttu-id="a8dc0-116">Description</span><span class="sxs-lookup"><span data-stu-id="a8dc0-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="a8dc0-117">Nombre d’enregistrements de l’ID de langue</span><span class="sxs-lookup"><span data-stu-id="a8dc0-117">Language ID Records Count</span></span>  | <span data-ttu-id="a8dc0-118">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="a8dc0-118">**DWORD**</span></span>    | <span data-ttu-id="a8dc0-119">4 octets</span><span class="sxs-lookup"><span data-stu-id="a8dc0-119">4 bytes</span></span> | <span data-ttu-id="a8dc0-120">Nombre de langues</span><span class="sxs-lookup"><span data-stu-id="a8dc0-120">Number of languages</span></span>                    |
| <span data-ttu-id="a8dc0-121">Enregistrements d’ID de langue</span><span class="sxs-lookup"><span data-stu-id="a8dc0-121">Language ID Records</span></span>        | <span data-ttu-id="a8dc0-122">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="a8dc0-122">**BYTE**\[\]</span></span> | <span data-ttu-id="a8dc0-123">Variable</span><span class="sxs-lookup"><span data-stu-id="a8dc0-123">Varies</span></span>  | <span data-ttu-id="a8dc0-124">Tableau de chaînes de langage (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="a8dc0-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="a8dc0-125">Le premier **DWORD** est le nombre de langages, suivi d’un tableau de chaînes d’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="a8dc0-126">Chaque chaîne a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="a8dc0-126">Each string has the following format:</span></span>



| <span data-ttu-id="a8dc0-127">Champ de l’objet de liste de langues</span><span class="sxs-lookup"><span data-stu-id="a8dc0-127">Language List Object field</span></span> | <span data-ttu-id="a8dc0-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="a8dc0-128">Data type</span></span>     | <span data-ttu-id="a8dc0-129">Taille</span><span class="sxs-lookup"><span data-stu-id="a8dc0-129">Size</span></span>    | <span data-ttu-id="a8dc0-130">Description</span><span class="sxs-lookup"><span data-stu-id="a8dc0-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dc0-131">Longueur de l’ID de langue</span><span class="sxs-lookup"><span data-stu-id="a8dc0-131">Language ID Length</span></span>         | <span data-ttu-id="a8dc0-132">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="a8dc0-132">**DWORD**</span></span>     | <span data-ttu-id="a8dc0-133">4 octets</span><span class="sxs-lookup"><span data-stu-id="a8dc0-133">4 bytes</span></span> | <span data-ttu-id="a8dc0-134">Longueur de la chaîne en octets, y compris la taille du caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="a8dc0-135">ID de langue</span><span class="sxs-lookup"><span data-stu-id="a8dc0-135">Language ID</span></span>                | <span data-ttu-id="a8dc0-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="a8dc0-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="a8dc0-137">Variable</span><span class="sxs-lookup"><span data-stu-id="a8dc0-137">Varies</span></span>  | <span data-ttu-id="a8dc0-138">Chaîne terminée par le caractère null qui contient le nom du langage RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="a8dc0-139">Chaque chaîne est une balise de langue conforme à la norme RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="a8dc0-140">Pour obtenir la balise de langue d’un flux particulier dans le fichier ASF, interrogez le descripteur de flux pour l’attribut de l' [**\_ index d' \_ \_ \_ \_ ID \_ de langue EXTSTRMPROP MF SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a8dc0-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a8dc0-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8dc0-141">Examples</span></span>

<span data-ttu-id="a8dc0-142">L’exemple suivant montre comment analyser la liste des langues.</span><span class="sxs-lookup"><span data-stu-id="a8dc0-142">The following example shows how to parse the language list.</span></span>


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a><span data-ttu-id="a8dc0-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8dc0-143">Requirements</span></span>



| <span data-ttu-id="a8dc0-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8dc0-144">Requirement</span></span> | <span data-ttu-id="a8dc0-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8dc0-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dc0-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8dc0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dc0-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8dc0-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8dc0-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8dc0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dc0-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8dc0-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8dc0-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8dc0-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8dc0-151"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8dc0-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8dc0-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8dc0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8dc0-153">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8dc0-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8dc0-154">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a8dc0-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a8dc0-155">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a8dc0-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a8dc0-156">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a8dc0-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a8dc0-157">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="a8dc0-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8dc0-158">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="a8dc0-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="a8dc0-159">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="a8dc0-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="a8dc0-160">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="a8dc0-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




