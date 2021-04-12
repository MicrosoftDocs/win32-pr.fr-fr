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
# <a name="displayspecifiers-container"></a>Conteneur DisplaySpecifiers

Les spécificateurs d’affichage sont stockés, par paramètres régionaux, dans le conteneur DisplaySpecifiers du conteneur de configuration. Étant donné que le conteneur de configuration est répliqué dans toute la forêt, les spécificateurs d’affichage sont propagés dans tous les domaines d’une forêt.

Le conteneur de configuration stocke le conteneur DisplaySpecifiers, qui stocke ensuite les conteneurs correspondant à chaque paramètre régional. Ces conteneurs de paramètres régionaux sont nommés à l’aide de la représentation hexadécimale de l’identificateur de paramètres régionaux. Par exemple, le conteneur de paramètres régionaux US/anglais est nommé 409, le conteneur de paramètres régionaux allemands est nommé 407, et le conteneur de paramètres régionaux japonais s’intitule 411. Pour plus d’informations et pour obtenir la liste des identificateurs de langage possibles, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langue.

Chaque conteneur de paramètres régionaux stocke les objets de la classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .

Pour répertorier tous les spécificateurs d’affichage pour des paramètres régionaux, énumérez tous les objets [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) dans le conteneur de paramètres régionaux spécifié dans le conteneur DisplaySpecifiers.

L’exemple de code suivant contient une fonction qui crée une liaison avec le conteneur spécificateur d’affichage pour les paramètres régionaux spécifiés :


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



 

 