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
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="81c20-103">Création de gestionnaires de miniatures</span><span class="sxs-lookup"><span data-stu-id="81c20-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="81c20-104">À compter de Windows Vista, une plus grande utilisation est faite d’images miniatures spécifiques aux fichiers que dans les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="81c20-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="81c20-105">Ils sont utilisés dans tous les affichages, dans les boîtes de dialogue et dans tout type de fichier qui les fournit.</span><span class="sxs-lookup"><span data-stu-id="81c20-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="81c20-106">L’affichage des miniatures a également été modifié.</span><span class="sxs-lookup"><span data-stu-id="81c20-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="81c20-107">Un spectre continu de tailles sélectionnables par l’utilisateur est disponible plutôt que des tailles discrètes, telles que des icônes et des miniatures.</span><span class="sxs-lookup"><span data-stu-id="81c20-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="81c20-108">L’interface [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) permet de fournir une miniature plus simple que l’ancienne [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ou [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span><span class="sxs-lookup"><span data-stu-id="81c20-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="81c20-109">Notez, toutefois, que le code existant qui utilise **IExtractImage** ou **IExtractImage2** est toujours valide et pris en charge.</span><span class="sxs-lookup"><span data-stu-id="81c20-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="81c20-110">Exemple RecipeThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="81c20-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="81c20-111">L’exemple [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) dans cette section est inclus dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="81c20-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="81c20-112">Son emplacement d’installation par défaut est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ exemples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider.</span><span class="sxs-lookup"><span data-stu-id="81c20-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="81c20-113">Toutefois, la majeure partie du code est également incluse ici.</span><span class="sxs-lookup"><span data-stu-id="81c20-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="81c20-114">L’exemple [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) illustre l’implémentation d’un gestionnaire de miniatures pour un nouveau type de fichier inscrit avec une extension. recipe.</span><span class="sxs-lookup"><span data-stu-id="81c20-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="81c20-115">L’exemple illustre l’utilisation des différentes API du gestionnaire de miniatures pour inscrire des serveurs COM (Component Object Model) d’extraction de miniatures pour des types de fichiers personnalisés.</span><span class="sxs-lookup"><span data-stu-id="81c20-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="81c20-116">Cette rubrique vous guide tout au long de l’exemple de code, en mettant en évidence les choix et les recommandations en matière de codage.</span><span class="sxs-lookup"><span data-stu-id="81c20-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="81c20-117">Un gestionnaire de miniatures doit toujours implémenter [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) conjointement avec l’une des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="81c20-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="81c20-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="81c20-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="81c20-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="81c20-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="81c20-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="81c20-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="81c20-121">Dans certains cas, l’initialisation avec des flux n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="81c20-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="81c20-122">Dans les scénarios où votre gestionnaire de miniatures n’implémente pas [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), il doit choisir de ne pas s’exécuter dans le processus isolé où l’indexeur système le place par défaut lorsqu’une modification est apportée au flux.</span><span class="sxs-lookup"><span data-stu-id="81c20-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="81c20-123">Pour désactiver la fonctionnalité d’isolation de processus, définissez la valeur de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="81c20-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="81c20-124">Si vous implémentez [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) et effectuez une initialisation basée sur un flux, votre gestionnaire est plus sécurisé et fiable.</span><span class="sxs-lookup"><span data-stu-id="81c20-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="81c20-125">En règle générale, la désactivation de l’isolation des processus est uniquement destinée aux gestionnaires hérités ; Évitez de désactiver cette fonctionnalité pour tout nouveau code.</span><span class="sxs-lookup"><span data-stu-id="81c20-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="81c20-126">À chaque fois que cela est possible, **IInitializeWithStream** doit être votre premier choix d’interface d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="81c20-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="81c20-127">Étant donné que le fichier image de l’exemple n’est pas incorporé dans le fichier. Recipe et qu’il ne fait pas partie de son flux de fichier, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) est utilisé dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="81c20-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="81c20-128">L’implémentation de la méthode [**IInitializeWithItem :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) passe simplement ses paramètres à des variables de classe privées.</span><span class="sxs-lookup"><span data-stu-id="81c20-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="81c20-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) a une seule méthode,[**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), qui est appelée avec la plus grande taille souhaitée de l’image, en pixels.</span><span class="sxs-lookup"><span data-stu-id="81c20-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="81c20-130">Bien que le paramètre soit nommé *CX*, sa valeur est utilisée comme taille maximale des dimensions x et y de l’image.</span><span class="sxs-lookup"><span data-stu-id="81c20-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="81c20-131">Si la miniature Récupérée n’est pas carrée, l’axe le plus long est limité par *CX* et les proportions de l’image d’origine sont conservées.</span><span class="sxs-lookup"><span data-stu-id="81c20-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="81c20-132">Quand elle retourne, [**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fournit un handle à l’image récupérée.</span><span class="sxs-lookup"><span data-stu-id="81c20-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="81c20-133">Il fournit également une valeur qui indique le format de couleur de l’image et si elle contient des informations alpha valides.</span><span class="sxs-lookup"><span data-stu-id="81c20-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="81c20-134">L’implémentation de miniature dans l’exemple commence par un appel à la méthode privée **\_ GetBase64EncodedImageString** .</span><span class="sxs-lookup"><span data-stu-id="81c20-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="81c20-135">Le type de fichier. Recipe est simplement un fichier XML enregistré sous la forme d’une extension de nom de fichier unique.</span><span class="sxs-lookup"><span data-stu-id="81c20-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="81c20-136">Il inclut un élément appelé **Picture** qui fournit le chemin d’accès relatif et le nom de fichier de l’image à utiliser comme miniature pour ce fichier. Recipe particulier.</span><span class="sxs-lookup"><span data-stu-id="81c20-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="81c20-137">L’élément **Picture** se compose de l’attribut **source** qui spécifie une image encodée de base 64 et d’un attribut de **taille** facultatif.</span><span class="sxs-lookup"><span data-stu-id="81c20-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="81c20-138">La **taille** a deux valeurs, petite et grande.</span><span class="sxs-lookup"><span data-stu-id="81c20-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="81c20-139">Cela vous permet de fournir plusieurs nœuds d' **image** avec des images distinctes.</span><span class="sxs-lookup"><span data-stu-id="81c20-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="81c20-140">L’image récupérée dépend ensuite de la valeur de taille maximale (*CX*) fournie dans l’appel à [**miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span><span class="sxs-lookup"><span data-stu-id="81c20-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="81c20-141">Étant donné que Windows ne dimensionne jamais l’image à une taille supérieure à sa taille maximale, différentes images peuvent être fournies pour différentes résolutions.</span><span class="sxs-lookup"><span data-stu-id="81c20-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="81c20-142">Toutefois, pour plus de simplicité, l’exemple omet l’attribut **Size** et ne fournit qu’une seule image pour toutes les situations.</span><span class="sxs-lookup"><span data-stu-id="81c20-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="81c20-143">La méthode **\_ GetBase64EncodedImageString** , dont l’implémentation est présentée ici, utilise des API XML Document Object Model (DOM) pour récupérer le nœud **image** .</span><span class="sxs-lookup"><span data-stu-id="81c20-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="81c20-144">À partir de ce nœud, il extrait l’image à partir des données d’attribut **source** .</span><span class="sxs-lookup"><span data-stu-id="81c20-144">From that node it extracts the image from the **Source** attribute data.</span></span>


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



<span data-ttu-id="81c20-145">[**Miniature**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) transmet ensuite la chaîne Récupérée à **\_ GetStreamFromString**.</span><span class="sxs-lookup"><span data-stu-id="81c20-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


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



<span data-ttu-id="81c20-146">La méthode **\_ GetStreamFromString** , dont l’implémentation est présentée ici, qui convertit l’image encodée en un flux.</span><span class="sxs-lookup"><span data-stu-id="81c20-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


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



<span data-ttu-id="81c20-147">**Miniature** utilise ensuite les API WIC (Windows Imaging Component) pour extraire une image bitmap du flux et obtenir un handle vers cette bitmap.</span><span class="sxs-lookup"><span data-stu-id="81c20-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="81c20-148">Les informations alpha sont définies, le WIC est correctement quitté et la méthode se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="81c20-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="81c20-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81c20-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c20-150">Gestionnaires de miniatures</span><span class="sxs-lookup"><span data-stu-id="81c20-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="81c20-151">Instructions du gestionnaire de miniatures</span><span class="sxs-lookup"><span data-stu-id="81c20-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="81c20-152">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="81c20-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
