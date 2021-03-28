---
description: À compter de Windows Vista, une plus grande utilisation est faite d’images miniatures spécifiques aux fichiers que dans les versions antérieures de Windows.
title: Création de gestionnaires de miniatures
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972067"
---
# <a name="building-thumbnail-handlers"></a>Création de gestionnaires de miniatures

À compter de Windows Vista, une plus grande utilisation est faite d’images miniatures spécifiques aux fichiers que dans les versions antérieures de Windows. Ils sont utilisés dans tous les affichages, dans les boîtes de dialogue et dans tout type de fichier qui les fournit. L’affichage des miniatures a également été modifié. Un spectre continu de tailles sélectionnables par l’utilisateur est disponible plutôt que des tailles discrètes, telles que des icônes et des miniatures.

L’interface [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) permet de fournir une miniature plus simple que l’ancienne [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ou [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2). Notez, toutefois, que le code existant qui utilise **IExtractImage** ou **IExtractImage2** est toujours valide et pris en charge.

## <a name="the-recipethumbnailprovider-sample"></a>Exemple RecipeThumbnailProvider

L’exemple [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) dans cette section est inclus dans le kit de développement logiciel (SDK) Windows. Son emplacement d’installation par défaut est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ exemples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider. Toutefois, la majeure partie du code est également incluse ici.

L’exemple [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustre l’implémentation d’un gestionnaire de miniatures pour un nouveau type de fichier inscrit avec une extension. recipe. L’exemple illustre l’utilisation des différentes API du gestionnaire de miniatures pour inscrire des serveurs COM (Component Object Model) d’extraction de miniatures pour des types de fichiers personnalisés. Cette rubrique vous guide tout au long de l’exemple de code, en mettant en évidence les choix et les recommandations en matière de codage.

Un gestionnaire de miniatures doit toujours implémenter [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) conjointement avec l’une des interfaces suivantes :

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Dans certains cas, l’initialisation avec des flux n’est pas possible. Dans les scénarios où votre gestionnaire de miniatures n’implémente pas [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), il doit choisir de ne pas s’exécuter dans le processus isolé où l’indexeur système le place par défaut lorsqu’une modification est apportée au flux. Pour désactiver la fonctionnalité d’isolation de processus, définissez la valeur de Registre suivante.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Si vous implémentez [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) et effectuez une initialisation basée sur un flux, votre gestionnaire est plus sécurisé et fiable. En règle générale, la désactivation de l’isolation des processus est uniquement destinée aux gestionnaires hérités ; Évitez de désactiver cette fonctionnalité pour tout nouveau code. À chaque fois que cela est possible, **IInitializeWithStream** doit être votre premier choix d’interface d’initialisation.

Étant donné que le fichier image de l’exemple n’est pas incorporé dans le fichier. Recipe et qu’il ne fait pas partie de son flux de fichier, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) est utilisé dans l’exemple. L’implémentation de la méthode [**IInitializeWithItem :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) passe simplement ses paramètres à des variables de classe privées.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) a une seule méthode,[**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), qui est appelée avec la plus grande taille souhaitée de l’image, en pixels. Bien que le paramètre soit nommé *CX*, sa valeur est utilisée comme taille maximale des dimensions x et y de l’image. Si la miniature Récupérée n’est pas carrée, l’axe le plus long est limité par *CX* et les proportions de l’image d’origine sont conservées.

Quand elle retourne, [**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fournit un handle à l’image récupérée. Il fournit également une valeur qui indique le format de couleur de l’image et si elle contient des informations alpha valides.

L’implémentation de miniature dans l’exemple commence par un appel à la méthode privée **\_ GetBase64EncodedImageString** .


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



Le type de fichier. Recipe est simplement un fichier XML enregistré sous la forme d’une extension de nom de fichier unique. Il inclut un élément appelé **Picture** qui fournit le chemin d’accès relatif et le nom de fichier de l’image à utiliser comme miniature pour ce fichier. Recipe particulier. L’élément **Picture** se compose de l’attribut **source** qui spécifie une image encodée de base 64 et d’un attribut de **taille** facultatif.

La **taille** a deux valeurs, petite et grande. Cela vous permet de fournir plusieurs nœuds d' **image** avec des images distinctes. L’image récupérée dépend ensuite de la valeur de taille maximale (*CX*) fournie dans l’appel à [**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Étant donné que Windows ne dimensionne jamais l’image à une taille supérieure à sa taille maximale, différentes images peuvent être fournies pour différentes résolutions. Toutefois, pour plus de simplicité, l’exemple omet l’attribut **Size** et ne fournit qu’une seule image pour toutes les situations.

La méthode **\_ GetBase64EncodedImageString** , dont l’implémentation est présentée ici, utilise des API XML Document Object Model (DOM) pour récupérer le nœud **image** . À partir de ce nœud, il extrait l’image à partir des données d’attribut **source** .


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



[**Miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) transmet ensuite la chaîne Récupérée à **\_ GetStreamFromString**.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



La méthode **\_ GetStreamFromString** , dont l’implémentation est présentée ici, qui convertit l’image encodée en un flux.


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



**Miniature** utilise ensuite les API WIC (Windows Imaging Component) pour extraire une image bitmap du flux et obtenir un handle vers cette bitmap. Les informations alpha sont définies, le WIC est correctement quitté et la méthode se termine correctement.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires de miniatures](thumbnail-providers.md)
</dt> <dt>

[Instructions du gestionnaire de miniatures](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
