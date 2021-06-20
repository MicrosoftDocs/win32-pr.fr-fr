---
description: Cet article explique comment initialiser des gestionnaires de propriétés pour fonctionner avec le système de propriétés Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisation des gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7626f92b3d81a6764e635c10302747f82a383
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406992"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="acec2-103">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-103">Initializing Property Handlers</span></span>

<span data-ttu-id="acec2-104">Cette rubrique explique comment créer et inscrire des gestionnaires de propriétés pour utiliser le système de propriétés Windows.</span><span class="sxs-lookup"><span data-stu-id="acec2-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="acec2-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="acec2-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="acec2-106">Gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="acec2-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="acec2-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="acec2-108">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="acec2-109">Banque de propriétés en mémoire</span><span class="sxs-lookup"><span data-stu-id="acec2-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="acec2-110">Gestion des valeurs de PROPVARIANT-Based</span><span class="sxs-lookup"><span data-stu-id="acec2-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="acec2-111">Prise en charge des métadonnées ouvertes</span><span class="sxs-lookup"><span data-stu-id="acec2-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="acec2-112">Contenu de texte intégral</span><span class="sxs-lookup"><span data-stu-id="acec2-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="acec2-113">Fournir des valeurs pour les propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="acec2-114">Écriture des valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="acec2-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="acec2-115">Implémentation de IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="acec2-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="acec2-116">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="acec2-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acec2-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="acec2-118">Gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-118">Property Handlers</span></span>

<span data-ttu-id="acec2-119">Les gestionnaires de propriétés constituent une partie essentielle du système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="acec2-120">Elles sont appelées in-process par l’indexeur pour lire et indexer les valeurs de propriété, et elles sont également appelées par l’Explorateur Windows en mode in-process pour lire et écrire des valeurs de propriété directement dans les fichiers.</span><span class="sxs-lookup"><span data-stu-id="acec2-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="acec2-121">Ces gestionnaires doivent être écrits et testés avec soin pour éviter la dégradation des performances ou la perte de données dans les fichiers affectés.</span><span class="sxs-lookup"><span data-stu-id="acec2-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="acec2-122">Pour plus d’informations sur les considérations spécifiques à l’indexeur qui affectent l’implémentation du gestionnaire de propriétés, consultez [développement de gestionnaires de propriétés pour Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="acec2-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="acec2-123">Cette rubrique présente un exemple de format de fichier basé sur XML qui décrit une recette avec une extension de nom de fichier. recipe.</span><span class="sxs-lookup"><span data-stu-id="acec2-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="acec2-124">L’extension de nom de fichier. Recipe est inscrite en tant que format de fichier distinct plutôt que de s’appuyer sur le format de fichier .xml plus générique, dont le gestionnaire utilise un flux secondaire pour stocker les propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="acec2-125">Nous vous recommandons d’inscrire des extensions de nom de fichier uniques pour vos types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="acec2-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="acec2-126">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="acec2-126">Before You Begin</span></span>

<span data-ttu-id="acec2-127">Les gestionnaires de propriétés sont des objets COM qui créent l’abstraction [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour un format de fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="acec2-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="acec2-128">Ils lisent (analysent) et écrivent ce format de fichier d’une manière conforme à sa spécification.</span><span class="sxs-lookup"><span data-stu-id="acec2-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="acec2-129">Certains gestionnaires de propriétés effectuent leur travail en fonction d’API qui extraient l’accès à un format de fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="acec2-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="acec2-130">Avant de développer un gestionnaire de propriétés pour votre format de fichier, vous devez comprendre comment votre format de fichier stocke les propriétés et comment ces propriétés (noms et valeurs) sont mappées à l’abstraction de la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="acec2-131">Quand vous planifiez votre implémentation, n’oubliez pas que les gestionnaires de propriétés sont des composants de bas niveau qui sont chargés dans le contexte de processus tels que l’Explorateur Windows, l’indexeur de recherche Windows et des applications tierces qui utilisent le modèle de programmation d’élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="acec2-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="acec2-132">Par conséquent, les gestionnaires de propriétés ne peuvent pas être implémentés en code managé et doivent être implémentés en C++.</span><span class="sxs-lookup"><span data-stu-id="acec2-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="acec2-133">Si votre gestionnaire utilise des API ou des services pour effectuer son travail, vous devez vous assurer que ces services peuvent fonctionner correctement dans le ou les environnements dans lesquels votre gestionnaire de propriétés est chargé.</span><span class="sxs-lookup"><span data-stu-id="acec2-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="acec2-134">Les gestionnaires de propriétés sont toujours associés à des types de fichiers spécifiques ; ainsi, si votre format de fichier contient des propriétés qui nécessitent un gestionnaire de propriétés personnalisées, vous devez toujours inscrire une extension de nom de fichier unique pour chaque format de fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="acec2-135">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-135">Initializing Property Handlers</span></span>

<span data-ttu-id="acec2-136">Avant qu’une propriété ne soit utilisée par le système, elle est initialisée en appelant une implémentation d' [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span><span class="sxs-lookup"><span data-stu-id="acec2-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="acec2-137">Le gestionnaire de propriétés doit être initialisé en faisant en sorte que le système lui affecte un flux au lieu de quitter cette assignation à l’implémentation du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="acec2-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="acec2-138">Cette méthode d’initialisation garantit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="acec2-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="acec2-139">Le gestionnaire de propriétés peut s’exécuter dans un processus restreint (une fonctionnalité de sécurité importante) sans disposer de droits d’accès pour lire ou écrire directement des fichiers, plutôt que d’accéder à leur contenu via le flux.</span><span class="sxs-lookup"><span data-stu-id="acec2-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="acec2-140">Le système peut être approuvé pour gérer correctement les oplocks de fichiers, ce qui constitue une mesure de fiabilité importante.</span><span class="sxs-lookup"><span data-stu-id="acec2-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="acec2-141">Le système de propriétés fournit un service d’enregistrement sécurisé automatique sans aucune fonctionnalité supplémentaire requise à partir de l’implémentation du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="acec2-142">Pour plus d’informations sur les flux, consultez la section [écriture des valeurs de retour](#writing-back-values) .</span><span class="sxs-lookup"><span data-stu-id="acec2-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="acec2-143">L’utilisation de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) fait abstraction de votre implémentation des détails du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="acec2-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="acec2-144">Cela permet au gestionnaire de prendre en charge l’initialisation par le biais de stockages alternatifs tels qu’un dossier protocole FTP (FTP) ou un fichier compressé avec une extension de nom de fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="acec2-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="acec2-145">Dans certains cas, l’initialisation avec des flux n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="acec2-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="acec2-146">Dans ce cas, il existe deux autres interfaces que les gestionnaires de propriétés peuvent implémenter : [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) et [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="acec2-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="acec2-147">Si un gestionnaire de propriétés n’implémente pas l' [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), il doit choisir de ne pas s’exécuter dans le processus isolé dans lequel l’indexeur système le placerait par défaut en cas de modification du flux.</span><span class="sxs-lookup"><span data-stu-id="acec2-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="acec2-148">Pour désactiver cette fonctionnalité, définissez la valeur de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="acec2-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="acec2-149">Toutefois, il est nettement préférable d’implémenter [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) et d’effectuer une initialisation basée sur un flux.</span><span class="sxs-lookup"><span data-stu-id="acec2-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="acec2-150">Votre gestionnaire de propriétés sera plus sûr et plus fiable en conséquence.</span><span class="sxs-lookup"><span data-stu-id="acec2-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="acec2-151">La désactivation de l’isolation de processus est généralement prévue uniquement pour les gestionnaires de propriétés hérités et doit être évitée de manière ardue par tout nouveau code.</span><span class="sxs-lookup"><span data-stu-id="acec2-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="acec2-152">Pour examiner en détail l’implémentation d’un gestionnaire de propriétés, examinez l’exemple de code suivant, qui est une implémentation de [**IInitializeWithStream :: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="acec2-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="acec2-153">Le gestionnaire est initialisé en chargeant un document de recette XML à l’aide d’un pointeur vers l’instance [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associée à ce document.</span><span class="sxs-lookup"><span data-stu-id="acec2-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="acec2-154">La variable **\_ spDocEle** utilisée près de la fin de l’exemple de code est définie plus tôt dans l’exemple en tant que msxml2 :: IXMLDOMElementPtr.</span><span class="sxs-lookup"><span data-stu-id="acec2-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="acec2-155">Les exemples de code suivants et suivants sont extraits de l’exemple de gestionnaire de recette inclus dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="acec2-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="acec2-156">.</span><span class="sxs-lookup"><span data-stu-id="acec2-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="acec2-157">Â</span><span class="sxs-lookup"><span data-stu-id="acec2-157">Â</span></span> 

<span data-ttu-id="acec2-158">Une fois le document lui-même chargé, les propriétés à afficher dans l’Explorateur Windows sont chargées en appelant la méthode protégée **\_ LoadProperties** , comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="acec2-159">Ce processus est examiné en détail dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="acec2-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="acec2-160">Si le flux est en lecture seule mais que le paramètre *grfMode* contient l' \_ indicateur STGM ReadWrite, l’initialisation doit échouer et retourner STG \_ E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="acec2-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="acec2-161">Sans cette vérification, l’Explorateur Windows affiche les valeurs de propriété comme étant accessibles en écriture, même si ce n’est pas le cas, ce qui complique l’expérience de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="acec2-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="acec2-162">Le gestionnaire de propriétés n’est initialisé qu’une seule fois pendant sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="acec2-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="acec2-163">Si une deuxième initialisation est demandée, le gestionnaire doit retourner `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="acec2-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="acec2-164">Banque de propriétés de In-Memory</span><span class="sxs-lookup"><span data-stu-id="acec2-164">In-Memory Property Store</span></span>

<span data-ttu-id="acec2-165">Avant d’examiner l’implémentation de **\_ LoadProperties**, vous devez comprendre le tableau **PropertyMap** utilisé dans l’exemple pour mapper les propriétés du document XML aux propriétés existantes dans le système de propriétés par le biais de leurs valeurs de groupe de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="acec2-166">Vous ne devez pas exposer tous les éléments et attributs du fichier XML en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="acec2-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="acec2-167">Au lieu de cela, sélectionnez uniquement celles que vous jugerez utiles pour les utilisateurs finaux de l’organisation de leurs documents (dans ce cas, recettes).</span><span class="sxs-lookup"><span data-stu-id="acec2-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="acec2-168">Il s’agit d’un concept important à prendre en compte lors du développement de vos gestionnaires de propriétés : la différence entre les informations réellement utiles pour les scénarios organisationnels et les informations qui appartiennent aux détails de votre fichier et qui peuvent être consultées en ouvrant le fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="acec2-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="acec2-169">Les propriétés ne sont pas destinées à être une duplication complète d’un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="acec2-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="acec2-170">Voici l’implémentation complète de la méthode **\_ LoadProperties** appelée par [**IInitializeWithStream :: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="acec2-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="acec2-171">La méthode **\_ LoadProperties** appelle la fonction d’assistance de Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés en mémoire (cache) pour les propriétés gérées.</span><span class="sxs-lookup"><span data-stu-id="acec2-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="acec2-172">À l’aide d’un cache, les modifications sont suivies pour vous.</span><span class="sxs-lookup"><span data-stu-id="acec2-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="acec2-173">Cela vous évite de suivre si une valeur de propriété a été modifiée dans le cache, mais pas encore enregistrée dans un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="acec2-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="acec2-174">Elle vous évite également d’avoir à conserver inutilement des valeurs de propriété qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="acec2-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="acec2-175">La méthode **\_ LoadProperties** appelle également **\_ LoadProperty** , dont l’implémentation est illustrée dans le code suivant) une fois pour chaque propriété mappée.</span><span class="sxs-lookup"><span data-stu-id="acec2-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="acec2-176">**\_ LoadProperty** obtient la valeur de la propriété telle qu’elle est spécifiée dans l’élément **PropertyMap** du flux XML et l’assigne au cache en mémoire via un appel à [**IPropertyStoreCache :: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span><span class="sxs-lookup"><span data-stu-id="acec2-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="acec2-177">L' \_ indicateur normal PSC dans l’appel à **IPropertyStoreCache :: SetValueAndState** indique que la valeur de propriété n’a pas été modifiée depuis l’entrée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="acec2-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="acec2-178">Gestion des valeurs de PROPVARIANT-Based</span><span class="sxs-lookup"><span data-stu-id="acec2-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="acec2-179">Dans l’implémentation de **\_ LoadProperty**, une valeur de propriété est fournie sous la forme d’un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="acec2-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="acec2-180">Un ensemble d’API dans le kit de développement logiciel (SDK) est fourni pour la conversion de types primitifs tels que **PWSTR** ou **int** vers ou à partir de types **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="acec2-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="acec2-181">Ces API se trouvent dans Propvarutil. h.</span><span class="sxs-lookup"><span data-stu-id="acec2-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="acec2-182">Par exemple, pour convertir un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en chaîne, vous pouvez utiliser [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) , comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="acec2-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="acec2-183">Pour initialiser un PROPVARIANT à partir d’une chaîne, vous pouvez utiliser [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span><span class="sxs-lookup"><span data-stu-id="acec2-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="acec2-184">Comme vous pouvez le voir dans l’un des fichiers de recette inclus dans l’exemple, il peut y avoir plus d’un mot clé dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="acec2-185">Pour tenir compte de cela, le système de propriétés prend en charge les chaînes à valeurs multiples représentées sous forme de vecteur de chaînes (par exemple, « VT \_ Vector \| VT \_ LPWStr »).</span><span class="sxs-lookup"><span data-stu-id="acec2-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="acec2-186">La méthode **\_ LoadVectorProperty** dans l’exemple utilise des valeurs vectorielles.</span><span class="sxs-lookup"><span data-stu-id="acec2-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="acec2-187">Si une valeur n’existe pas dans le fichier, ne retourne pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="acec2-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="acec2-188">Au lieu de cela, définissez la valeur sur VT \_ vide et retournez **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acec2-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="acec2-189">VT \_ vide indique que la valeur de propriété n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="acec2-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="acec2-190">Prise en charge des métadonnées ouvertes</span><span class="sxs-lookup"><span data-stu-id="acec2-190">Supporting Open Metadata</span></span>

<span data-ttu-id="acec2-191">Cet exemple utilise un format de fichier basé sur XML.</span><span class="sxs-lookup"><span data-stu-id="acec2-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="acec2-192">Son schéma peut être étendu pour prendre en charge des propriétés qui n’ont pas été considérées pendant la developmet, par exemple.</span><span class="sxs-lookup"><span data-stu-id="acec2-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="acec2-193">Ce système est connu sous le nom de métadonnées ouvertes.</span><span class="sxs-lookup"><span data-stu-id="acec2-193">This system is known as open metadata.</span></span> <span data-ttu-id="acec2-194">Cet exemple étend le système de propriétés en créant un nœud sous l’élément **Recipe** appelé **ExtendedProperties**, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="acec2-195">Pour charger des propriétés étendues persistantes pendant l’initialisation, implémentez la méthode **\_ LoadExtendedProperties** , comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="acec2-196">Les API de sérialisation déclarées dans propsys. h sont utilisées pour sérialiser et désérialiser des types [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en objets BLOB de données, puis l’encodage Base64 est utilisé pour sérialiser ces objets BLOB dans des chaînes qui peuvent être enregistrées dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="acec2-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="acec2-197">Ces chaînes sont stockées dans l’attribut **EncodedValue** de l’élément **ExtendedProperties** .</span><span class="sxs-lookup"><span data-stu-id="acec2-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="acec2-198">La méthode utilitaire suivante, implémentée dans le fichier util. cpp de l’exemple, effectue la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="acec2-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="acec2-199">Elle commence par un appel à la fonction [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) pour effectuer la sérialisation binaire, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="acec2-200">Ensuite, la fonction [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â, déclarée dans wincrypt. h, effectue la conversion en base64.</span><span class="sxs-lookup"><span data-stu-id="acec2-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="acec2-201">La fonction **DeserializePropVariantFromString** , également trouvée dans util. cpp, inverse l’opération et désérialise les valeurs à partir du fichier XML.</span><span class="sxs-lookup"><span data-stu-id="acec2-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="acec2-202">Pour plus d’informations sur la prise en charge des métadonnées ouvertes, consultez « types de fichiers prenant en charge les métadonnées ouvertes » dans [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="acec2-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="acec2-203">Contenu de Full-Text</span><span class="sxs-lookup"><span data-stu-id="acec2-203">Full-Text Contents</span></span>

<span data-ttu-id="acec2-204">Les gestionnaires de propriétés peuvent également faciliter une recherche en texte intégral sur le contenu du fichier, et constituent un moyen simple de fournir cette fonctionnalité si le format de fichier n’est pas trop complexe.</span><span class="sxs-lookup"><span data-stu-id="acec2-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="acec2-205">Il existe une méthode alternative plus puissante pour fournir le texte intégral du fichier par le biais de l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="acec2-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="acec2-206">Le tableau suivant récapitule les avantages de chaque approche à l’aide d' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="acec2-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="acec2-207">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="acec2-207">Capability</span></span>                                   | <span data-ttu-id="acec2-208">Filtres</span><span class="sxs-lookup"><span data-stu-id="acec2-208">IFilter</span></span>                      | <span data-ttu-id="acec2-209">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="acec2-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="acec2-210">Autorise l’écriture différée dans les fichiers ?</span><span class="sxs-lookup"><span data-stu-id="acec2-210">Allows write back to files?</span></span>                  | <span data-ttu-id="acec2-211">Non</span><span class="sxs-lookup"><span data-stu-id="acec2-211">No</span></span>                           | <span data-ttu-id="acec2-212">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-212">Yes</span></span>            |
| <span data-ttu-id="acec2-213">Fournit une combinaison de contenu et de propriétés ?</span><span class="sxs-lookup"><span data-stu-id="acec2-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="acec2-214">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-214">Yes</span></span>                          | <span data-ttu-id="acec2-215">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-215">Yes</span></span>            |
| <span data-ttu-id="acec2-216">Multilingue?</span><span class="sxs-lookup"><span data-stu-id="acec2-216">Multilingual?</span></span>                                | <span data-ttu-id="acec2-217">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-217">Yes</span></span>                          | <span data-ttu-id="acec2-218">Non</span><span class="sxs-lookup"><span data-stu-id="acec2-218">No</span></span>             |
| <span data-ttu-id="acec2-219">MIME/Embedded ?</span><span class="sxs-lookup"><span data-stu-id="acec2-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="acec2-220">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-220">Yes</span></span>                          | <span data-ttu-id="acec2-221">Non</span><span class="sxs-lookup"><span data-stu-id="acec2-221">No</span></span>             |
| <span data-ttu-id="acec2-222">Limites du texte ?</span><span class="sxs-lookup"><span data-stu-id="acec2-222">Text boundaries?</span></span>                             | <span data-ttu-id="acec2-223">Phrase, paragraphe, chapitre</span><span class="sxs-lookup"><span data-stu-id="acec2-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="acec2-224">Aucun</span><span class="sxs-lookup"><span data-stu-id="acec2-224">None</span></span>           |
| <span data-ttu-id="acec2-225">Implémentation prise en charge pour SPS/SQL Server ?</span><span class="sxs-lookup"><span data-stu-id="acec2-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="acec2-226">Oui</span><span class="sxs-lookup"><span data-stu-id="acec2-226">Yes</span></span>                          | <span data-ttu-id="acec2-227">Non</span><span class="sxs-lookup"><span data-stu-id="acec2-227">No</span></span>             |
| <span data-ttu-id="acec2-228">Implémentation</span><span class="sxs-lookup"><span data-stu-id="acec2-228">Implementation</span></span>                               | <span data-ttu-id="acec2-229">Complex</span><span class="sxs-lookup"><span data-stu-id="acec2-229">Complex</span></span>                      | <span data-ttu-id="acec2-230">Simple</span><span class="sxs-lookup"><span data-stu-id="acec2-230">Simple</span></span>         |



 

<span data-ttu-id="acec2-231">Dans l’exemple de gestionnaire de recette, le format de fichier de recette n’a pas d’exigences complexes, donc seul [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a été implémenté pour la prise en charge de la recherche en texte intégral.</span><span class="sxs-lookup"><span data-stu-id="acec2-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="acec2-232">La recherche en texte intégral est implémentée pour les nœuds XML nommés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="acec2-233">Le système de propriétés contient la `System.Search.Contents` propriété (contenu de recherche de groupe de \_ \_ caractères), créée pour fournir le contenu de texte intégral à l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="acec2-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="acec2-234">La valeur de cette propriété n’est jamais affichée directement dans l’interface utilisateur ; le texte de tous les nœuds XML nommés dans le tableau ci-dessus est concaténé dans une chaîne unique.</span><span class="sxs-lookup"><span data-stu-id="acec2-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="acec2-235">Cette chaîne est ensuite fournie à l’indexeur en tant que contenu de texte intégral du fichier de recette via un appel à [**IPropertyStoreCache :: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="acec2-236">Fournir des valeurs pour les propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-236">Providing Values for Properties</span></span>

<span data-ttu-id="acec2-237">Lorsqu’ils sont utilisés pour lire des valeurs, les gestionnaires de propriétés sont généralement appelés pour l’une des raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="acec2-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="acec2-238">Pour énumérer toutes les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="acec2-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="acec2-239">Pour obtenir la valeur d’une propriété spécifique.</span><span class="sxs-lookup"><span data-stu-id="acec2-239">To get the value of a specific property.</span></span>

<span data-ttu-id="acec2-240">Pour l’énumération, un gestionnaire de propriétés est invité à énumérer ses propriétés lors de l’indexation ou lorsque la boîte de dialogue Propriétés demande l’affichage des propriétés dans l' **autre** groupe.</span><span class="sxs-lookup"><span data-stu-id="acec2-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="acec2-241">L’indexation s’effectue constamment en tant qu’opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="acec2-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="acec2-242">Chaque fois qu’un fichier est modifié, l’indexeur est notifié et réindexe le fichier en demandant au gestionnaire de propriétés d’énumérer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="acec2-243">Par conséquent, il est essentiel que les gestionnaires de propriétés soient implémentés efficacement et retournent des valeurs de propriété aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="acec2-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="acec2-244">Énumérez toutes les propriétés pour lesquelles vous avez des valeurs, comme vous le feriez pour n’importe quelle collection, mais n’énumérez pas les propriétés qui impliquent des calculs gourmands en mémoire ou des demandes réseau qui pourraient les rendre plus lentes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="acec2-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="acec2-245">Lors de l’écriture d’un gestionnaire de propriétés, vous devez généralement prendre en compte les deux ensembles de propriétés suivants.</span><span class="sxs-lookup"><span data-stu-id="acec2-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="acec2-246">Propriétés principales : propriétés que votre type de fichier prend en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="acec2-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="acec2-247">Par exemple, un gestionnaire de propriétés de photos pour les métadonnées EXIF (Exchangeable Image File) prend en charge en mode natif `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="acec2-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="acec2-248">Propriétés étendues : propriétés que votre type de fichier prend en charge dans le cadre des métadonnées ouvertes.</span><span class="sxs-lookup"><span data-stu-id="acec2-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="acec2-249">Étant donné que l’exemple utilise le cache en mémoire, l’implémentation des méthodes [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) est simplement une question de délégation à ce cache, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acec2-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="acec2-250">Si vous choisissez de ne pas déléguer au cache en mémoire, vous devez implémenter vos méthodes pour fournir> le comportement attendu suivant :</span><span class="sxs-lookup"><span data-stu-id="acec2-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="acec2-251">[**IPropertyStore :: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): s’il n’existe aucune propriété, cette méthode retourne **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acec2-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="acec2-252">[**IPropertyStore :: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): si *iProp* est supérieur ou égal à *CProps*, cette méthode retourne E \_ INVALIDARG et la structure vers laquelle pointe le paramètre *de* la ligne de base est remplie avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="acec2-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="acec2-253">[**IPropertyStore :: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) et [**IPropertyStore :: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflètent l’état actuel du gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="acec2-254">Si une [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) est ajoutée ou supprimée du fichier via [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), ces deux méthodes doivent refléter cette modification la prochaine fois qu’elles sont appelées.</span><span class="sxs-lookup"><span data-stu-id="acec2-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="acec2-255">[**IPropertyStore :: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): si cette méthode est demandée pour une valeur qui n’existe pas, elle retourne **S \_ OK** avec la valeur signalée comme VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="acec2-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="acec2-256">Écriture des valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="acec2-256">Writing Back Values</span></span>

<span data-ttu-id="acec2-257">Quand le gestionnaire de propriétés écrit la valeur d’une propriété à l’aide de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), il n’écrit pas la valeur dans le fichier tant que [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="acec2-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="acec2-258">Le cache en mémoire peut être utile pour implémenter ce schéma.</span><span class="sxs-lookup"><span data-stu-id="acec2-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="acec2-259">Dans l’exemple de code, l’implémentation de **IPropertyStore :: SetValue** définit simplement la nouvelle valeur dans le cache en mémoire et définit l’état de cette propriété sur PSC \_ Dirty.</span><span class="sxs-lookup"><span data-stu-id="acec2-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="acec2-260">Dans toute implémentation de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , le comportement suivant est attendu de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="acec2-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="acec2-261">Si la propriété existe déjà, la valeur de la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="acec2-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="acec2-262">Si la propriété n’existe pas, la nouvelle propriété est ajoutée et sa valeur est définie.</span><span class="sxs-lookup"><span data-stu-id="acec2-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="acec2-263">Si la valeur de propriété ne peut pas être rendue persistante à la même précision que celle donnée (par exemple, la troncation en raison de limitations de taille dans le format de fichier), la valeur est définie autant que possible et les inplaces \_ \_ tronquées sont retournées.</span><span class="sxs-lookup"><span data-stu-id="acec2-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="acec2-264">Si la propriété n’est pas prise en charge par le gestionnaire de propriétés, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` est retourné.</span><span class="sxs-lookup"><span data-stu-id="acec2-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="acec2-265">S’il existe une autre raison pour laquelle la valeur de la propriété ne peut pas être définie, comme le fichier verrouillé ou le manque de droits à modifier via les listes de contrôle d’accès (ACL), STG \_ E \_ ACCESSDENIED est retourné.</span><span class="sxs-lookup"><span data-stu-id="acec2-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="acec2-266">L’un des principaux avantages de l’utilisation de flux, comme l’exemple, est la fiabilité.</span><span class="sxs-lookup"><span data-stu-id="acec2-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="acec2-267">Les gestionnaires de propriétés doivent toujours considérer qu’ils ne peuvent pas conserver un fichier dans un état incohérent dans le cas d’une défaillance catastrophique.</span><span class="sxs-lookup"><span data-stu-id="acec2-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="acec2-268">L’endommagement des fichiers d’un utilisateur est évidemment évité, et la meilleure façon de le faire est d’utiliser un mécanisme de « copie sur écriture ».</span><span class="sxs-lookup"><span data-stu-id="acec2-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="acec2-269">Si votre gestionnaire de propriétés utilise un flux pour accéder à un fichier, vous recevez ce comportement automatiquement. le système écrit toutes les modifications apportées au flux, en remplaçant le fichier par la nouvelle copie uniquement pendant l’opération de validation.</span><span class="sxs-lookup"><span data-stu-id="acec2-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="acec2-270">Pour remplacer ce comportement et contrôler manuellement le processus d’enregistrement du fichier, vous pouvez désactiver le comportement d’enregistrement sécurisé en définissant la valeur ManualSafeSave dans l’entrée de registre de votre gestionnaire, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="acec2-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="acec2-271">Lorsqu’un gestionnaire spécifie la valeur ManualSafeSave, le flux avec lequel il est initialisé n’est pas un flux traité (STGM \_ traité).</span><span class="sxs-lookup"><span data-stu-id="acec2-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="acec2-272">Le gestionnaire lui-même doit implémenter la fonction Safe Save pour s’assurer que le fichier n’est pas endommagé si l’opération d’enregistrement est interrompue.</span><span class="sxs-lookup"><span data-stu-id="acec2-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="acec2-273">Si le gestionnaire implémente l’écriture sur place, il écrit dans le flux de données qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="acec2-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="acec2-274">Si le gestionnaire ne prend pas en charge cette fonctionnalité, il doit récupérer un flux avec lequel écrire la copie mise à jour du fichier à l’aide de [**IDestinationStreamFactory :: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span><span class="sxs-lookup"><span data-stu-id="acec2-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="acec2-275">Une fois l’écriture terminée, le gestionnaire doit appeler [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) sur le flux d’origine pour terminer l’opération et remplacer le contenu du flux d’origine par la nouvelle copie du fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="acec2-276">ManualSafeSave est également la situation par défaut si vous n’initialisez pas votre gestionnaire avec un flux.</span><span class="sxs-lookup"><span data-stu-id="acec2-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="acec2-277">Sans un flux d’origine pour recevoir le contenu du flux temporaire, vous devez utiliser [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) pour effectuer un remplacement atomique du fichier source.</span><span class="sxs-lookup"><span data-stu-id="acec2-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="acec2-278">Les formats de fichiers volumineux qui seront utilisés de manière à produire des fichiers de plus de 1 Mo doivent implémenter la prise en charge de l’écriture de propriété sur place ; dans le cas contraire, le comportement des performances ne répond pas aux attentes des clients du système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="acec2-279">Dans ce scénario, la durée nécessaire à l’écriture des propriétés ne doit pas être affectée par la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="acec2-280">Pour les fichiers de très grande taille, par exemple un fichier vidéo de 1 Go ou plus, une autre solution est requise.</span><span class="sxs-lookup"><span data-stu-id="acec2-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="acec2-281">S’il n’y a pas assez d’espace dans le fichier pour effectuer une écriture sur place, le gestionnaire peut échouer à la mise à jour de propriété si la quantité d’espace réservée à l’écriture de propriété sur place est épuisée.</span><span class="sxs-lookup"><span data-stu-id="acec2-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="acec2-282">Cet échec se produit pour éviter des performances médiocres dues à 2 Go d’e/s (1 à lire, 1 à écrire).</span><span class="sxs-lookup"><span data-stu-id="acec2-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="acec2-283">En raison de cette défaillance potentielle, ces formats de fichier doivent réserver suffisamment d’espace pour l’écriture de propriété sur place.</span><span class="sxs-lookup"><span data-stu-id="acec2-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="acec2-284">Si le fichier a suffisamment d’espace dans son en-tête pour écrire des métadonnées, et si l’écriture de ces métadonnées n’entraîne pas l’augmentation ou la réduction du fichier, l’écriture sur place peut être sécurisée.</span><span class="sxs-lookup"><span data-stu-id="acec2-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="acec2-285">Nous vous recommandons 64 Ko comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="acec2-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="acec2-286">L’écriture sur place équivaut au gestionnaire qui demande ManualSafeSave et appelle [**IStream :: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) dans l’implémentation de [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), et offre de bien meilleures performances que la copie en écriture.</span><span class="sxs-lookup"><span data-stu-id="acec2-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="acec2-287">Si la taille du fichier change en raison des modifications apportées à la valeur de la propriété, l’écriture sur place ne doit pas être tentée en raison du risque de corruption d’un fichier dans le cas d’un arrêt anormal.</span><span class="sxs-lookup"><span data-stu-id="acec2-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="acec2-288">Pour des raisons de performances, nous vous recommandons d’utiliser l’option ManualSafeSave avec les gestionnaires de propriétés qui utilisent des fichiers de 100 Ko ou plus.</span><span class="sxs-lookup"><span data-stu-id="acec2-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="acec2-289">Comme illustré dans l’exemple d’implémentation suivant de [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), le gestionnaire de ManualSafeSave est inscrit pour illustrer l’option d’enregistrement sécurisé manuel.</span><span class="sxs-lookup"><span data-stu-id="acec2-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="acec2-290">La méthode **\_ SaveCacheToDom** écrit les valeurs de propriété stockées dans le cache en mémoire dans l’objet XMLdocument.</span><span class="sxs-lookup"><span data-stu-id="acec2-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="acec2-291">Ensuite, demandez si pécifiée prend en charge [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span><span class="sxs-lookup"><span data-stu-id="acec2-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="acec2-292">Ensuite, validez le flux d’origine, qui écrit les données dans le fichier d’origine de manière sûre.</span><span class="sxs-lookup"><span data-stu-id="acec2-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="acec2-293">Examinez ensuite l’implémentation de **\_ SaveCacheToDom** .</span><span class="sxs-lookup"><span data-stu-id="acec2-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="acec2-294">Ensuite, récupérez le nombre de propriétés stockées dans le cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="acec2-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="acec2-295">À présent, itérez au sein des propriétés pour déterminer si la valeur d’une propriété a été modifiée depuis son chargement en mémoire.</span><span class="sxs-lookup"><span data-stu-id="acec2-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="acec2-296">La méthode [**IPropertyStoreCache :: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) obtient l’état de la propriété dans le cache.</span><span class="sxs-lookup"><span data-stu-id="acec2-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="acec2-297">L’indicateur de modification du PSC \_ , qui a été défini dans l’implémentation de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marque une propriété comme modifiée.</span><span class="sxs-lookup"><span data-stu-id="acec2-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="acec2-298">Mappez la propriété au nœud XML comme spécifié dans le tableau **exemple \_ rgPropertyMap** .</span><span class="sxs-lookup"><span data-stu-id="acec2-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="acec2-299">Si une propriété ne figure pas dans le mappage, il s’agit d’une nouvelle propriété qui a été définie par l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="acec2-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="acec2-300">Étant donné que les métadonnées ouvertes sont prises en charge, enregistrez la nouvelle propriété dans la section **ExtendedProperties** du document XML.</span><span class="sxs-lookup"><span data-stu-id="acec2-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="acec2-301">Implémentation de IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="acec2-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="acec2-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informe l’interface utilisateur de l’interpréteur de commandes si une propriété particulière peut être modifiée dans l’interface utilisateur de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="acec2-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="acec2-303">Il est important de noter que cela concerne uniquement la possibilité de modifier la propriété dans l’interface utilisateur, pas si vous pouvez appeler [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) sur la propriété.</span><span class="sxs-lookup"><span data-stu-id="acec2-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="acec2-304">Une propriété qui provoque une valeur de retour de S \_ false à partir de [**IPropertyStoreCapabilities :: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) peut toujours être capable d’être définie par le biais d’une application.</span><span class="sxs-lookup"><span data-stu-id="acec2-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="acec2-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) retourne **S \_ OK** pour indiquer que les utilisateurs finaux doivent être autorisés à modifier la propriété directement ; S \_ false indique qu’elles ne doivent pas.</span><span class="sxs-lookup"><span data-stu-id="acec2-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="acec2-306">S \_ false peut signifier que les applications sont responsables de l’écriture de la propriété, et non des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="acec2-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="acec2-307">L’interpréteur de commandes désactive les contrôles d’édition selon les besoins en fonction des résultats des appels à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="acec2-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="acec2-308">Un gestionnaire qui n’implémente pas [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) est supposé prendre en charge les métadonnées ouvertes via la prise en charge de l’écriture d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="acec2-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="acec2-309">Si vous générez un gestionnaire qui gère uniquement les propriétés en lecture seule, vous devez implémenter votre méthode **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) afin qu’il retourne STG \_ E ACCESSDENIED lorsqu’il est \_ appelé avec l' \_ indicateur STGM ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="acec2-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="acec2-310">L’attribut [isInnate](./propdesc-schema-typeinfo.md) de certaines propriétés est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="acec2-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="acec2-311">Les propriétés innées présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="acec2-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="acec2-312">La propriété est généralement calculée d’une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="acec2-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="acec2-313">Par exemple, `System.Image.BitDepth` est calculé à partir de l’image elle-même.</span><span class="sxs-lookup"><span data-stu-id="acec2-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="acec2-314">La modification de la propriété n’a pas de sens sans modifier le fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="acec2-315">Par exemple, la modification de `System.Image.Dimensions` l’image ne peut pas être redimensionnée, donc il n’est pas judicieux d’autoriser l’utilisateur à la modifier.</span><span class="sxs-lookup"><span data-stu-id="acec2-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="acec2-316">Dans certains cas, ces propriétés sont fournies automatiquement par le système.</span><span class="sxs-lookup"><span data-stu-id="acec2-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="acec2-317">Les exemples incluent `System.DateModified` , qui est fourni par le système de fichiers, et `System.SharedWith` , qui est basé sur la personne avec laquelle l’utilisateur partage le fichier.</span><span class="sxs-lookup"><span data-stu-id="acec2-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="acec2-318">En raison de ces caractéristiques, les propriétés marquées comme *IsInnate* sont fournies à l’utilisateur dans l’interface utilisateur du shell uniquement en tant que propriétés en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="acec2-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="acec2-319">Si une propriété est marquée comme *IsInnate*, le système de propriétés ne stocke pas cette propriété dans le gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="acec2-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="acec2-320">Par conséquent, les gestionnaires de propriétés n’ont pas besoin de code spécial pour prendre en compte ces propriétés dans leurs implémentations.</span><span class="sxs-lookup"><span data-stu-id="acec2-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="acec2-321">Si la valeur de l’attribut *IsInnate* n’est pas explicitement indiquée pour une propriété particulière, la valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="acec2-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="acec2-322">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="acec2-323">Avec le gestionnaire de propriétés implémenté, il doit être enregistré et son extension de nom de fichier associée au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="acec2-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="acec2-324">Pour plus d’informations, consultez [inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="acec2-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acec2-325">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acec2-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acec2-326">Fonctionnement des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="acec2-327">Utilisation des noms de genres</span><span class="sxs-lookup"><span data-stu-id="acec2-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="acec2-328">Utilisation des listes de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="acec2-329">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="acec2-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="acec2-330">Meilleures pratiques pour le gestionnaire de propriétés et FAQ</span><span class="sxs-lookup"><span data-stu-id="acec2-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
