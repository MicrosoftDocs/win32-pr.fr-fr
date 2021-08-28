---
description: Implémentation de IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implémentation de IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378d48ec9047da6068e8d95143f8b10b7016faea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465236"
---
# <a name="implementing-iamerrorlog"></a>Implémentation de IAMErrorLog

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

L’interface [**IAMErrorLog**](iamerrorlog.md) contient une méthode unique, [**LogError**](iamerrorlog-logerror.md). Les paramètres de la méthode contiennent des informations sur l’erreur qui s’est produite.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



le code d’erreur et la chaîne d’erreur sont définis par DirectShow Services d’édition. Pour obtenir la liste des erreurs, consultez [Erreurs de rendu](rendering-errors.md).

Le paramètre *pExtraInfo* contient un pointeur vers un type Variant qui contient des informations supplémentaires sur l’erreur. Le type de données et le contenu de la variante dépendent de l’erreur spécifique qui s’est produite. Par exemple, si l’erreur est due à un nom de fichier incorrect, le VARIANT est une chaîne avec le nom de fichier incorrect. Certaines erreurs n’ont pas d’informations supplémentaires, donc *pExtraInfo* peut avoir la **valeur null**. Le code suivant montre comment tester le membre **VT** du variant, qui indique le type de données et mettre en forme un message en conséquence.


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
> Ne libérez pas la variante vers laquelle pointe
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . En outre, la variante devient non valide après le retour de la méthode, donc ne la référencez pas plus tard.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation des erreurs](logging-errors.md)
</dt> </dl>

 

 



