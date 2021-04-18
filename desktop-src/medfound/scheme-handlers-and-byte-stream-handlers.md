---
description: Cette rubrique décrit les détails internes de la façon dont le programme de résolution source crée une source de média.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Gestionnaires de schémas et gestionnaires de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519581"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="95621-103">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="95621-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="95621-104">Cette rubrique décrit les détails internes de la façon dont le programme de résolution source crée une source de média.</span><span class="sxs-lookup"><span data-stu-id="95621-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="95621-105">Lisez cette rubrique si vous implémentez une source de média personnalisée pour Media Foundation, et que vous souhaitez que la source du média soit disponible pour les applications via le programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="95621-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="95621-106">Le programme de résolution source peut créer une source de média à partir d’une URL ou d’un flux d’octets (autrement dit, un pointeur [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ).</span><span class="sxs-lookup"><span data-stu-id="95621-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="95621-107">Pour ce faire, il utilise des objets d’assistance appelés *gestionnaires*.</span><span class="sxs-lookup"><span data-stu-id="95621-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="95621-108">Pour les URL, le programme de résolution source utilise des *gestionnaires de schémas*.</span><span class="sxs-lookup"><span data-stu-id="95621-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="95621-109">Pour les flux d’octets, elle utilise des *gestionnaires de flux d’octets*.</span><span class="sxs-lookup"><span data-stu-id="95621-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="95621-110">Un gestionnaire de schéma prend une URL comme entrée et crée une source de média ou un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="95621-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="95621-111">Si elle crée un flux d’octets, le programme de résolution source le transmet à un gestionnaire de flux d’octets, qui crée la source du média.</span><span class="sxs-lookup"><span data-stu-id="95621-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="95621-112">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="95621-112">The following image illustrates this process.</span></span>

![Diagramme montrant le processus de résolution source](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="95621-114">Gestionnaires de schéma</span><span class="sxs-lookup"><span data-stu-id="95621-114">Scheme Handlers</span></span>

<span data-ttu-id="95621-115">Les gestionnaires de schéma sont utilisés quand l’application appelle [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou son équivalent asynchrone [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="95621-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="95621-116">Le programme de résolution source recherche les gestionnaires de schéma dans le registre.</span><span class="sxs-lookup"><span data-stu-id="95621-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="95621-117">Les gestionnaires de modèles sont répertoriés par schéma d’URL, sous les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="95621-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="95621-118">où *<scheme>* est le schéma d’URL que le gestionnaire est conçu pour analyser.</span><span class="sxs-lookup"><span data-stu-id="95621-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="95621-119">Le schéma comprend le caractère «  : » de fin ; par exemple, « http : ».</span><span class="sxs-lookup"><span data-stu-id="95621-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="95621-120">Pour inscrire un nouveau gestionnaire de schéma, ajoutez une entrée dont le nom est le CLSID du gestionnaire de schémas, sous forme de chaîne canonique : `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="95621-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="95621-121">La valeur de l’entrée est une chaîne (REG \_ SZ) contenant une brève description du gestionnaire, telle que « mon gestionnaire de schémas ».</span><span class="sxs-lookup"><span data-stu-id="95621-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="95621-122">La partie importante de l’entrée est le CLSID.</span><span class="sxs-lookup"><span data-stu-id="95621-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="95621-123">Le programme de résolution source crée le gestionnaire en appelant **CoCreateInstance** avec ce CLSID.</span><span class="sxs-lookup"><span data-stu-id="95621-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="95621-124">Les gestionnaires de schéma exposent l’interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) .</span><span class="sxs-lookup"><span data-stu-id="95621-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="95621-125">Si le programme de résolution source trouve un gestionnaire de schéma qui correspond au schéma d’URL, le programme de résolution source appelle [**IMFSchemeHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), en passant l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="95621-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="95621-126">Le gestionnaire de schéma ouvre l’URL et tente d’analyser le contenu.</span><span class="sxs-lookup"><span data-stu-id="95621-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="95621-127">À ce stade, le gestionnaire de schéma a deux options :</span><span class="sxs-lookup"><span data-stu-id="95621-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="95621-128">Créez une source de média.</span><span class="sxs-lookup"><span data-stu-id="95621-128">Create a media source.</span></span>
-   <span data-ttu-id="95621-129">Créez un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="95621-129">Create a byte stream.</span></span>

<span data-ttu-id="95621-130">Si elle crée une source de média, le programme de résolution source retourne la source du média à l’application.</span><span class="sxs-lookup"><span data-stu-id="95621-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="95621-131">Si elle crée un flux d’octets, le programme de résolution source tente de trouver un gestionnaire de flux d’octets approprié, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="95621-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="95621-132">Gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="95621-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="95621-133">Les gestionnaires de flux d’octets sont utilisés quand l’application appelle [**IMFSourceResolver :: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) ou son équivalent asynchrone [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span><span class="sxs-lookup"><span data-stu-id="95621-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="95621-134">Ils sont également utilisés lorsqu’un gestionnaire de schéma retourne un flux d’octets, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="95621-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="95621-135">Comme avec les gestionnaires de modèles, les gestionnaires de flux d’octets sont répertoriés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="95621-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="95621-136">Elles sont répertoriées par extension de nom de fichier ou type MIME (ou les deux), sous les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="95621-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="95621-137">où *<ExtensionOrMimeType>* est l’extension de nom de fichier ou le type MIME.</span><span class="sxs-lookup"><span data-stu-id="95621-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="95621-138">Les extensions de fichier incluent le caractère'. 'initial ; par exemple, « . wmv ».</span><span class="sxs-lookup"><span data-stu-id="95621-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="95621-139">L’extension de nom de fichier fait partie de l’URL, fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="95621-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="95621-140">Le type MIME peut être disponible via l’attribut de [**\_ \_ \_ type de contenu BYTESTREAM MF**](mf-bytestream-content-type-attribute.md) sur le flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="95621-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="95621-141">Pour inscrire un nouveau gestionnaire de flux d’octets, ajoutez une entrée dont le nom est le CLSID du gestionnaire, sous forme de chaîne canonique.</span><span class="sxs-lookup"><span data-stu-id="95621-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="95621-142">La valeur de l’entrée est une chaîne (REG \_ SZ) contenant une brève description du gestionnaire, telle que « mon gestionnaire de Byte-Stream ».</span><span class="sxs-lookup"><span data-stu-id="95621-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="95621-143">Le programme de résolution source appelle **CoCreateInstance** pour créer le gestionnaire à partir du CLSID.</span><span class="sxs-lookup"><span data-stu-id="95621-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="95621-144">Vous pouvez inscrire le même gestionnaire sous plusieurs extensions ou types MIME.</span><span class="sxs-lookup"><span data-stu-id="95621-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="95621-145">Les gestionnaires de flux d’octets exposent l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="95621-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="95621-146">Si le programme de résolution source trouve un gestionnaire de flux d’octets correspondant, il appelle [**IMFByteStreamHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="95621-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="95621-147">L’entrée de cette méthode est un pointeur vers le flux d’octets, plus l’URL d’origine, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="95621-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="95621-148">Le gestionnaire de flux d’octets lit à partir du flux d’octets jusqu’à ce qu’il analyse suffisamment de données pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="95621-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95621-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95621-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95621-150">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="95621-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



