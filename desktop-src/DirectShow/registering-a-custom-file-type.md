---
description: Cet article décrit comment le gestionnaire de graphes de filtre localise un filtre source, en fonction d’un nom de fichier.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Inscription d’un type de fichier personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515307"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="24f72-103">Inscription d’un type de fichier personnalisé</span><span class="sxs-lookup"><span data-stu-id="24f72-103">Registering a Custom File Type</span></span>

<span data-ttu-id="24f72-104">Cet article décrit comment le gestionnaire de graphes de filtre localise un filtre source, en fonction d’un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="24f72-105">Vous pouvez utiliser ce mécanisme pour inscrire vos propres types de fichiers personnalisés.</span><span class="sxs-lookup"><span data-stu-id="24f72-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="24f72-106">Une fois le type de fichier inscrit, DirectShow charge automatiquement le filtre source approprié chaque fois qu’une application appelle [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="24f72-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="24f72-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="24f72-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="24f72-108">Protocoles</span><span class="sxs-lookup"><span data-stu-id="24f72-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="24f72-109">Extensions de fichier</span><span class="sxs-lookup"><span data-stu-id="24f72-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="24f72-110">Vérifier les octets</span><span class="sxs-lookup"><span data-stu-id="24f72-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="24f72-111">Chargement du filtre source</span><span class="sxs-lookup"><span data-stu-id="24f72-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="24f72-112">Types de fichiers personnalisés dans le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="24f72-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="24f72-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24f72-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="24f72-114">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="24f72-114">Overview</span></span>

<span data-ttu-id="24f72-115">Pour localiser un filtre source à partir d’un nom de fichier donné, le gestionnaire de graphes de filtre tente d’effectuer les opérations suivantes, dans l’ordre :</span><span class="sxs-lookup"><span data-stu-id="24f72-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="24f72-116">Correspond au protocole, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="24f72-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="24f72-117">Correspond à l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-117">Match the file extension.</span></span>
3.  <span data-ttu-id="24f72-118">Correspond aux modèles d’octets dans le fichier, appelés *octets de vérification*.</span><span class="sxs-lookup"><span data-stu-id="24f72-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="24f72-119">Protocoles</span><span class="sxs-lookup"><span data-stu-id="24f72-119">Protocols</span></span>

<span data-ttu-id="24f72-120">Les noms de protocole tels que « FTP » ou « http » sont inscrits sous le</span><span class="sxs-lookup"><span data-stu-id="24f72-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="24f72-121">**\_racine des classes HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="24f72-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="24f72-122">clé, avec la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="24f72-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="24f72-123">Si le nom ou l’URL du fichier contient un signe deux-points («  : »), le gestionnaire de graphes de filtre tente d’utiliser la partie avant le «  : » comme nom de protocole.</span><span class="sxs-lookup"><span data-stu-id="24f72-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="24f72-124">Par exemple, si le nom est « myprot://myfile.ext », il recherche une clé de Registre nommée **myprot**.</span><span class="sxs-lookup"><span data-stu-id="24f72-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="24f72-125">Si cette clé existe et contient une sous-clé nommée « extensions », le gestionnaire de graphique de filtre recherche dans cette sous-clé les entrées qui correspondent à l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="24f72-126">La valeur de la clé doit être un GUID sous forme de chaîne ; par exemple, « {00000000-0000-0000-0000-000000000000} ».</span><span class="sxs-lookup"><span data-stu-id="24f72-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="24f72-127">Si le gestionnaire de graphique de filtre ne peut pas correspondre à n’importe quelle valeur dans la sous-clé **Extensions** , il recherche une sous-clé nommée **filtre source**, qui doit également être un GUID sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="24f72-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="24f72-128">Si le gestionnaire de graphique de filtre trouve un GUID correspondant, il l’utilise comme CLSID du filtre source et tente de charger le filtre.</span><span class="sxs-lookup"><span data-stu-id="24f72-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="24f72-129">S’il ne trouve pas de correspondance, il utilise le filtre de [source de fichier (URL)](file-source--url--filter.md) , qui traite le nom de fichier comme une URL.</span><span class="sxs-lookup"><span data-stu-id="24f72-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="24f72-130">Il existe deux exceptions à cet algorithme :</span><span class="sxs-lookup"><span data-stu-id="24f72-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="24f72-131">Pour exclure des lettres de pilotes, les chaînes à un seul caractère ne sont pas considérées comme des protocoles.</span><span class="sxs-lookup"><span data-stu-id="24f72-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="24f72-132">Si la chaîne est « file : » ou « file:// », elle n’est pas traitée comme un protocole.</span><span class="sxs-lookup"><span data-stu-id="24f72-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="24f72-133">Extensions de fichier</span><span class="sxs-lookup"><span data-stu-id="24f72-133">File Extensions</span></span>

<span data-ttu-id="24f72-134">S’il n’y a aucun protocole dans le nom de fichier, le gestionnaire de graphique de filtre recherche dans le registre les entrées avec les **\_ \_ \\ \\ extensions \\ clé HKEY de type média racine**.*ext* \\ , où.*ext* est l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="24f72-135">Si cette clé existe, le filtre de la **source** de valeur contient le CLSID du filtre source, sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="24f72-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="24f72-136">Éventuellement, la clé peut avoir des valeurs pour le type et le sous- **type** de **média** , qui fournissent les GUID de type et de sous-type principaux.</span><span class="sxs-lookup"><span data-stu-id="24f72-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="24f72-137">Vérifier les octets</span><span class="sxs-lookup"><span data-stu-id="24f72-137">Check Bytes</span></span>

<span data-ttu-id="24f72-138">Certains types de fichiers peuvent être identifiés par des modèles spécifiques de bits se produisant à des décalages d’octets spécifiques dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="24f72-139">Le gestionnaire de graphique de filtre recherche les clés dans le Registre sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="24f72-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="24f72-140">**HKEY \_ CLASSES \_ racine \\ MediaType \\**{ *major type* } \\ { *SubType* }</span><span class="sxs-lookup"><span data-stu-id="24f72-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="24f72-141">où le type et le sous- *type* *principaux* sont des GUID qui définissent le type de média pour le flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="24f72-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="24f72-142">Chaque clé contient une ou plusieurs sous-clés, généralement nommées 1, 2, etc., qui définissent les octets de vérification ; et une sous-clé nommée **source Filter** qui donne le CLSID du filtre source, sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="24f72-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="24f72-143">Les sous-clés de vérification d’octet sont des chaînes qui contiennent un ou plusieurs Quad de nombres appelés :</span><span class="sxs-lookup"><span data-stu-id="24f72-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="24f72-144">*offset*, *CB*, *Mask*, *Val*</span><span class="sxs-lookup"><span data-stu-id="24f72-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="24f72-145">Pour correspondre au fichier, le gestionnaire de graphique de filtre lit les octets CB, en commençant par le décalage de nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="24f72-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="24f72-146">Il effectue ensuite une opération and au niveau du bit sur la valeur du masque.</span><span class="sxs-lookup"><span data-stu-id="24f72-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="24f72-147">Si le résultat est égal à Val, le fichier est une correspondance pour ce Quad.</span><span class="sxs-lookup"><span data-stu-id="24f72-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="24f72-148">Les valeurs Mask et Val sont données au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="24f72-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="24f72-149">Une entrée vide pour Mask est traitée comme une chaîne de 1 de longueur CB.</span><span class="sxs-lookup"><span data-stu-id="24f72-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="24f72-150">Une valeur négative pour offset indique un décalage à partir de la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="24f72-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="24f72-151">Pour correspondre à la clé, le fichier doit correspondre à tous les Quad de l’une des sous-clés.</span><span class="sxs-lookup"><span data-stu-id="24f72-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="24f72-152">Par exemple, supposons que le registre contient les clés suivantes sous **\\ type de média HKCR**:</span><span class="sxs-lookup"><span data-stu-id="24f72-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="24f72-153">La première clé correspond au flux du MEDIATYPE de type principal \_ .</span><span class="sxs-lookup"><span data-stu-id="24f72-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="24f72-154">La sous-clé ci-dessous qui correspond au sous-type de MEDIATYPE \_ midi.</span><span class="sxs-lookup"><span data-stu-id="24f72-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="24f72-155">La valeur de la sous-clé de filtre source est CLSID \_ AsyncReader, CLSID du filtre de [source de fichier (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="24f72-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="24f72-156">Chaque entrée peut avoir plusieurs quadruples ; tous doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="24f72-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="24f72-157">Dans l’exemple suivant, les 4 premiers octets du fichier doivent être 0xAB, 0xCD, 0x12, 0x34 ; et les 4 derniers octets du fichier doivent être 0xAB, 0xAB, 0x00, 0xAB :</span><span class="sxs-lookup"><span data-stu-id="24f72-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="24f72-158">En outre, il peut y avoir plusieurs entrées listées sous un seul type de média.</span><span class="sxs-lookup"><span data-stu-id="24f72-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="24f72-159">Une correspondance avec l’une d’entre elles est suffisante.</span><span class="sxs-lookup"><span data-stu-id="24f72-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="24f72-160">Ce schéma autorise un ensemble de masques alternatifs. par exemple, les fichiers. wav qui peuvent avoir ou non un en-tête RIFF.</span><span class="sxs-lookup"><span data-stu-id="24f72-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="24f72-161">Ce schéma est similaire à celui utilisé par la fonction [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .</span><span class="sxs-lookup"><span data-stu-id="24f72-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="24f72-162">Chargement du filtre source</span><span class="sxs-lookup"><span data-stu-id="24f72-162">Loading the Source Filter</span></span>

<span data-ttu-id="24f72-163">En supposant que le gestionnaire de graphique de filtre trouve un filtre de source correspondant pour le fichier, il ajoute ce filtre au graphique, interroge le filtre de l’interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) et appelle [**IFileSourceFilter :: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span><span class="sxs-lookup"><span data-stu-id="24f72-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="24f72-164">Les arguments de la méthode **Load** sont le nom de fichier et le type de média, tel que déterminé à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="24f72-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="24f72-165">Si le gestionnaire de graphes de filtres ne trouve rien dans le registre, il utilise par défaut le filtre de source de fichier asynchrone.</span><span class="sxs-lookup"><span data-stu-id="24f72-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="24f72-166">Dans ce cas, il définit le type de média sur le **\_ flux de MediaType**, **MEDIASUBTYPE \_ aucun**.</span><span class="sxs-lookup"><span data-stu-id="24f72-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="24f72-167">Types de fichiers personnalisés dans le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="24f72-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="24f72-168">Le lecteur Windows Media utilise un ensemble supplémentaire d’entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="24f72-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="24f72-169">Pour plus d’informations, consultez Paramètres de registre de l' [extension de nom de fichier](../wmp/file-name-extension-registry-settings.md) dans le kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="24f72-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24f72-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24f72-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24f72-171">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="24f72-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 
