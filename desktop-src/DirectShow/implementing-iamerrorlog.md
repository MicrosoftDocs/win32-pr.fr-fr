---
description: Implémentation de IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implémentation de IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514912"
---
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="71507-103">Implémentation de IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="71507-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="71507-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="71507-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="71507-105">L’interface [**IAMErrorLog**](iamerrorlog.md) contient une méthode unique, [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="71507-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="71507-106">Les paramètres de la méthode contiennent des informations sur l’erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="71507-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="71507-107">Le code d’erreur et la chaîne d’erreur sont définis par les services d’édition DirectShow.</span><span class="sxs-lookup"><span data-stu-id="71507-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="71507-108">Pour obtenir la liste des erreurs, consultez [Erreurs de rendu](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="71507-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="71507-109">Le paramètre *pExtraInfo* contient un pointeur vers un type Variant qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="71507-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="71507-110">Le type de données et le contenu de la variante dépendent de l’erreur spécifique qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="71507-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="71507-111">Par exemple, si l’erreur est due à un nom de fichier incorrect, le VARIANT est une chaîne avec le nom de fichier incorrect.</span><span class="sxs-lookup"><span data-stu-id="71507-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="71507-112">Certaines erreurs n’ont pas d’informations supplémentaires, donc *pExtraInfo* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="71507-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="71507-113">Le code suivant montre comment tester le membre **VT** du variant, qui indique le type de données et mettre en forme un message en conséquence.</span><span class="sxs-lookup"><span data-stu-id="71507-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> <span data-ttu-id="71507-114">Ne libérez pas la variante vers laquelle pointe</span><span class="sxs-lookup"><span data-stu-id="71507-114">Do not free the VARIANT pointed to by</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="71507-115">.</span><span class="sxs-lookup"><span data-stu-id="71507-115">.</span></span> <span data-ttu-id="71507-116">En outre, la variante devient non valide après le retour de la méthode, donc ne la référencez pas plus tard.</span><span class="sxs-lookup"><span data-stu-id="71507-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="71507-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71507-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71507-118">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="71507-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



