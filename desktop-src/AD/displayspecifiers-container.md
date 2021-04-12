---
title: Conteneur DisplaySpecifiers
description: Les spécificateurs d’affichage sont stockés, par paramètres régionaux, dans le conteneur DisplaySpecifiers du conteneur de configuration. Étant donné que le conteneur de configuration est répliqué dans toute la forêt, les spécificateurs d’affichage sont propagés dans tous les domaines d’une forêt.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- Conteneur DisplaySpecifiers
- Conteneur, spécificateurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462879"
---
# <a name="displayspecifiers-container"></a><span data-ttu-id="33b5d-106">Conteneur DisplaySpecifiers</span><span class="sxs-lookup"><span data-stu-id="33b5d-106">DisplaySpecifiers Container</span></span>

<span data-ttu-id="33b5d-107">Les spécificateurs d’affichage sont stockés, par paramètres régionaux, dans le conteneur DisplaySpecifiers du conteneur de configuration.</span><span class="sxs-lookup"><span data-stu-id="33b5d-107">Display specifiers are stored, by locale, in the DisplaySpecifiers container of the Configuration container.</span></span> <span data-ttu-id="33b5d-108">Étant donné que le conteneur de configuration est répliqué dans toute la forêt, les spécificateurs d’affichage sont propagés dans tous les domaines d’une forêt.</span><span class="sxs-lookup"><span data-stu-id="33b5d-108">Because the Configuration container is replicated across the entire forest, display specifiers are propagated across all domains in a forest.</span></span>

<span data-ttu-id="33b5d-109">Le conteneur de configuration stocke le conteneur DisplaySpecifiers, qui stocke ensuite les conteneurs correspondant à chaque paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="33b5d-109">The Configuration container stores the DisplaySpecifiers container, which then stores containers that correspond to each locale.</span></span> <span data-ttu-id="33b5d-110">Ces conteneurs de paramètres régionaux sont nommés à l’aide de la représentation hexadécimale de l’identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="33b5d-110">These locale containers are named using the hexadecimal representation of the locale identifier.</span></span> <span data-ttu-id="33b5d-111">Par exemple, le conteneur de paramètres régionaux US/anglais est nommé 409, le conteneur de paramètres régionaux allemands est nommé 407, et le conteneur de paramètres régionaux japonais s’intitule 411.</span><span class="sxs-lookup"><span data-stu-id="33b5d-111">For example, the US/English locale container is named 409, the German locale's container is named 407, and the Japanese locale's container is named 411.</span></span> <span data-ttu-id="33b5d-112">Pour plus d’informations et pour obtenir la liste des identificateurs de langage possibles, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="33b5d-112">For more information, and a list of possible language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

<span data-ttu-id="33b5d-113">Chaque conteneur de paramètres régionaux stocke les objets de la classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .</span><span class="sxs-lookup"><span data-stu-id="33b5d-113">Each locale container stores objects of the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) class.</span></span>

<span data-ttu-id="33b5d-114">Pour répertorier tous les spécificateurs d’affichage pour des paramètres régionaux, énumérez tous les objets [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) dans le conteneur de paramètres régionaux spécifié dans le conteneur DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="33b5d-114">To list all display specifiers for a locale, enumerate all the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) objects in the specified locale container within the DisplaySpecifiers container.</span></span>

<span data-ttu-id="33b5d-115">L’exemple de code suivant contient une fonction qui crée une liaison avec le conteneur spécificateur d’affichage pour les paramètres régionaux spécifiés :</span><span class="sxs-lookup"><span data-stu-id="33b5d-115">The following code example contains a function that binds to the display specifier container for the specified locale:</span></span>


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 