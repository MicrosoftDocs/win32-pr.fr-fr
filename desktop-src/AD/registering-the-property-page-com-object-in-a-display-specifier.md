---
title: Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage
description: cette rubrique montre comment inscrire une DLL d’extension qui contient une feuille de propriétés Active Directory avec le registre Windows et Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage Active Directory
- Active Directory d’objets COM de page de propriétés, inscription dans un spécificateur d’affichage
- spécificateurs d’affichage Active Directory, inscription de l’objet COM page de propriétés dans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6685e406cb1bfdc16f73dd2fddd94a195fe74a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881234"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage

lorsque vous utilisez COM pour créer une DLL d’extension de feuille de propriétés pour Active Directory Domain Services, vous devez également enregistrer l’extension avec le registre Windows et Active Directory Domain Services. l’inscription de l’extension active les composants logiciels enfichables MMC d’administration Active Directory et le shell Windows pour reconnaître l’extension.

## <a name="registering-in-the-windows-registry"></a>inscription dans le registre de Windows

comme tous les serveurs COM, une extension de feuille de propriétés doit être inscrite dans le registre Windows. L’extension est inscrite sous la clé suivante.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; CLSID &gt;* est la représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sous la clé *&lt; &gt; CLSID* , il existe une clé **InprocServer32** qui identifie l’objet en tant que serveur in-proc 32 bits. Sous la clé **InprocServer32** , l’emplacement de la dll est spécifié dans la valeur par défaut et le modèle de thread est spécifié dans la valeur **ThreadingModel** . Toutes les extensions de feuille de propriétés doivent utiliser le modèle de thread « Apartment ».

## <a name="registering-with-active-directory-domain-services"></a>Inscription avec Active Directory Domain Services

L’inscription de l’extension de la feuille de propriétés est spécifique à un paramètre régional. Si l’extension de la feuille de propriétés s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la classe d’objet dans tous les sous-conteneurs de paramètres régionaux dans le conteneur de spécificateurs d’affichage. Si l’extension de la feuille de propriétés est localisée pour un certain nombre de paramètres régionaux, inscrivez-la dans l’objet **displaySpecifier** de ce sous-conteneur de paramètres régionaux. Pour plus d’informations sur le conteneur et les paramètres régionaux des spécificateurs d’affichage, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).

Il existe trois attributs de spécificateur d’affichage sous lesquels une extension de feuille de propriétés peut être inscrite. Il s’agit des [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)et [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

L’attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifie les pages de propriétés d’administration à afficher dans Active Directory composants logiciels enfichables d’administration. La page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés des objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration de Active Directory.

l’attribut [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifie les pages de propriétés de l’utilisateur final à afficher dans le shell Windows. la page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés des objets de la classe appropriée dans l’explorateur de Windows. à partir des systèmes d’exploitation Windows Server 2003, le shell Windows n’affiche plus d’objets Active Directory Domain Services.

le [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) est disponible uniquement sur les systèmes d’exploitation Windows Server 2003. La page de propriétés s’affiche lorsque l’utilisateur consulte les propriétés de plusieurs objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration de Active Directory.

Tous ces attributs sont à valeurs multiples.

Les valeurs des attributs [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) et [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) requièrent le format suivant.


```C++
<order number>,<clsid>,<optional data>
```



Les valeurs de l’attribut [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) nécessitent le format suivant.


```C++
<order number>,<clsid>
```



« &lt; Order Number &gt; » est un nombre non signé qui représente la position de la page dans la feuille. Lorsqu’une feuille de propriétés est affichée, les valeurs sont triées à l’aide d’une comparaison du « numéro d’ordre » de chaque valeur &lt; &gt; . Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces objets COM de page de propriétés sont chargés dans l’ordre dans lequel ils sont lus à partir du serveur de Active Directory. Si possible, vous devez utiliser un « &lt; numéro d’ordre » non existant &gt; ; autrement dit, il n’est pas utilisé par d’autres valeurs de la propriété. Il n’y a pas de position de départ prescrite, et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».

Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID tel qu’il a été généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

« &lt; Données facultatives &gt; » est une valeur de chaîne qui n’est pas obligatoire. Cette valeur peut être récupérée par l’objet COM page de propriétés à l’aide du pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passé à sa méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . L’objet COM page de propriétés obtient ces données en appelant [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) avec le format de presse-papiers [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) . Cela fournit un **HGLOBAL** qui contient une structure [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) la structure **DSPROPERTYPAGEINFO** contient une chaîne Unicode qui contient les « &lt; données facultatives &gt; ». Les « &lt; données facultatives &gt; » ne sont pas autorisées avec l’attribut [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) . L’exemple de code C/C++ suivant montre comment récupérer les « &lt; données facultatives &gt; ».


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



Une extension de feuille de propriétés peut implémenter plusieurs pages de propriétés ; une utilisation possible des « &lt; données facultatives &gt; » consiste à nommer les pages à afficher. Cela offre la possibilité de choisir d’implémenter plusieurs objets COM, un pour chaque page ou un objet COM unique pour gérer plusieurs pages.

L’exemple de code suivant est une valeur d’exemple qui peut être utilisée pour les attributs [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)ou [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> pour le shell Windows, les données du spécificateur d’affichage sont récupérées à l’ouverture de session de l’utilisateur et mises en cache pour la session utilisateur. Pour les composants logiciels enfichables d’administration, les données du spécificateur d’affichage sont récupérées lorsque le composant logiciel enfichable est chargé et sont mises en cache pour la durée de vie du processus. pour le shell Windows, cela indique que les modifications apportées aux spécificateurs d’affichage prennent effet après qu’un utilisateur se déconnecte, puis se reconnecte. Pour les composants logiciels enfichables d’administration, les modifications prennent effet lors du chargement du composant logiciel enfichable ou de la console.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Ajout d’une valeur aux attributs d’extension de la feuille de propriétés

La procédure suivante décrit comment inscrire une extension de feuille de propriétés sous l’un des attributs d’extension de la feuille de propriétés.

**Inscription d’une extension de feuille de propriétés sous l’un des attributs d’extension de la feuille de propriétés**

1.  Assurez-vous que l’extension n’existe pas déjà dans les valeurs d’attribut.
2.  Ajoutez la nouvelle valeur à la fin de la liste classement des pages de propriétés. Cela permet de définir la &lt; partie « Order Number &gt; » de la valeur de l’attribut sur la valeur suivante après le numéro de commande existant le plus élevé.
3.  La méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) est utilisée pour ajouter la nouvelle valeur à l’attribut. Le paramètre *lnControlCode* doit être défini sur **la \_ propriété \_ Append de publicité** afin que la nouvelle valeur soit ajoutée aux valeurs existantes et ne remplace donc pas les valeurs existantes. La méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) doit être appelée par la suite pour valider la modification dans le répertoire.

Sachez que la même extension de feuille de propriétés peut être inscrite pour plusieurs classes d’objets.

La méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) est utilisée pour ajouter la nouvelle valeur à l’attribut. Le paramètre *lnControlCode* doit être défini sur **la \_ propriété \_ Append de publicités**, afin que la nouvelle valeur soit ajoutée aux valeurs existantes et ne remplace pas les valeurs existantes. La méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) doit être appelée après pour valider la modification dans le répertoire.

L’exemple de code suivant ajoute une extension de feuille de propriétés à la classe de groupe dans les paramètres régionaux par défaut de l’ordinateur. N’oubliez pas que la fonction **AddPropertyPageToDisplaySpecifier** vérifie le CLSID de l’extension de la feuille de propriétés dans les valeurs existantes, obtient le numéro d’ordre le plus élevé et ajoute la valeur de la page de propriétés à l’aide de [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec la **\_ propriété ADS \_ Ajouter** le code de contrôle.


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 
