---
title: Utilisation d’attributs de métadonnées complexes
description: Utilisation d’attributs de métadonnées complexes
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Media Format SDK, attributs de métadonnées complexes
- ASF (Advanced Systems Format), attributs de métadonnées complexes
- ASF (format de systèmes avancés), attributs de métadonnées complexes
- métadonnées, attributs complexes
- attributs de métadonnées complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314281"
---
# <a name="using-complex-metadata-attributes"></a><span data-ttu-id="cf528-108">Utilisation d’attributs de métadonnées complexes</span><span class="sxs-lookup"><span data-stu-id="cf528-108">Using Complex Metadata Attributes</span></span>

<span data-ttu-id="cf528-109">Le kit de développement logiciel (SDK) Windows Media format prend en charge des attributs de métadonnées complexes, qui sont des attributs qui ont des valeurs représentées par une structure</span><span class="sxs-lookup"><span data-stu-id="cf528-109">The Windows Media Format SDK supports complex metadata attributes, which are attributes that have values represented by a structure.</span></span> <span data-ttu-id="cf528-110">Étant donné que tous les attributs doivent avoir un type de données défini dans l’énumération de type de données de l’attribut [**WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) , tous les attributs de métadonnées complexes sont traités comme un **\_ \_ binaire de type WMT**.</span><span class="sxs-lookup"><span data-stu-id="cf528-110">Because all attributes must have a data type defined in the [**WMT\_ATTR\_DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) enumeration, all complex metadata attributes are treated as **WMT\_TYPE\_BINARY**.</span></span> <span data-ttu-id="cf528-111">Lors de l’écriture d’un attribut complexe, effectuez un cast du pointeur vers la structure comme un pointeur d’octet.</span><span class="sxs-lookup"><span data-stu-id="cf528-111">When writing a complex attribute, cast the pointer to the structure as a byte pointer.</span></span> <span data-ttu-id="cf528-112">Lorsque vous récupérez un attribut complexe, effectuez un cast du tableau d’octets défini par [**IWMHeaderInfo3 :: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) en tant que structure appropriée.</span><span class="sxs-lookup"><span data-stu-id="cf528-112">When you retrieve a complex attribute, cast the array of bytes set by [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) as the appropriate structure.</span></span>

<span data-ttu-id="cf528-113">Les exemples de code suivants montrent comment définir et récupérer un attribut de métadonnées complexe.</span><span class="sxs-lookup"><span data-stu-id="cf528-113">The following code examples show how to set and retrieve a complex metadata attribute.</span></span> <span data-ttu-id="cf528-114">La première fonction ajoute un attribut de texte utilisateur, la deuxième fonction en récupère une.</span><span class="sxs-lookup"><span data-stu-id="cf528-114">The first function adds a user text attribute, the second function retrieves one.</span></span> <span data-ttu-id="cf528-115">Pour plus d’informations sur l’utilisation de ces exemples, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="cf528-115">For more information about how to use these examples, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="cf528-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf528-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf528-117">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="cf528-117">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




