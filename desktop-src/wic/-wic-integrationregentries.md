---
description: Cette rubrique s’applique à Windows Vista et versions ultérieures.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Intégration à la Galerie de photos Windows et à l’Explorateur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545835"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="c7852-103">Intégration à la Galerie de photos Windows et à l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="c7852-104">Cette rubrique s’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c7852-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="c7852-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7852-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="c7852-106">Introduction</span><span class="sxs-lookup"><span data-stu-id="c7852-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="c7852-107">Intégration au magasin de propriétés Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="c7852-108">Intégration à la Galerie de photos Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="c7852-109">Intégration au cache de miniatures Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="c7852-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7852-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="c7852-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="c7852-111">Introduction</span></span>

<span data-ttu-id="c7852-112">Pour permettre à la Galerie de photos Windows et à l’Explorateur Windows d’afficher des miniatures et de rechercher et mettre à jour des métadonnées d’image standard, un codec doit avoir une implémentation des interfaces [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) et [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associées.</span><span class="sxs-lookup"><span data-stu-id="c7852-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="c7852-113">L’interface IThumbnailProvider est utilisée pour récupérer des miniatures et remplir le cache de miniatures, et l’interface IPropertyStore est utilisée pour la recherche et la mise à jour des métadonnées associées à un fichier.</span><span class="sxs-lookup"><span data-stu-id="c7852-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="c7852-114">À compter de Windows Vista, tous les types de fichiers ont des miniatures et des métadonnées, mais différents types de fichiers requièrent des implémentations différentes de ces interfaces pour extraire ou générer les miniatures et les métadonnées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c7852-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="c7852-115">Le système fournit des implémentations par défaut de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="c7852-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="c7852-116">L’implémentation par défaut de IThumbnailProvider peut être utilisée pour tout format d’image compatible WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="c7852-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="c7852-117">L’implémentation par défaut de IPropertyStore peut être utilisée avec n’importe quel format d’image compatible WIC basé sur un conteneur TIFF (Tagged Image File Format) ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="c7852-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="c7852-118">Pour associer votre format d’image aux implémentations par défaut de ces deux interfaces, vous devez ajouter quelques entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="c7852-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="c7852-119">Les entrées suivantes indiquent à la Galerie de photos Windows et à l’Explorateur Windows qu’une extension de nom de fichier (. ext) et son type MIME associé sont associés à un format d’image.</span><span class="sxs-lookup"><span data-stu-id="c7852-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="c7852-120">L’entrée suivante indique aux fenêtres et aux applications qui utilisent le type de contenu (également appelé type MIME) qu’un fichier avec une extension donnée (. ext) est un format d’image.</span><span class="sxs-lookup"><span data-stu-id="c7852-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="c7852-121">Le propriétaire du type de fichier doit choisir un `<image sub type value>` qui identifie de façon unique le format de fichier et cette valeur de type de contenu doit être inscrite auprès de l’IANA.</span><span class="sxs-lookup"><span data-stu-id="c7852-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="c7852-122">L’entrée suivante indique à Windows, Windows Search et les applications qui utilisent [System. Kind](../properties/props-system-kind.md) qu’une extension de nom de fichier (. ext) doit être traitée comme une image.</span><span class="sxs-lookup"><span data-stu-id="c7852-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="c7852-123">Plus précisément, elle indique que la propriété System. Kind de l’extension de fichier doit être définie sur Picture.</span><span class="sxs-lookup"><span data-stu-id="c7852-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="c7852-124">Intégration au magasin de propriétés Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="c7852-125">Parfois, les mêmes propriétés de métadonnées sont exposées dans différents schémas de métadonnées, souvent avec des noms de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="c7852-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="c7852-126">Quand l’une de ces propriétés est mise à jour, mais que les autres ne le sont pas, les métadonnées dans le fichier peuvent être désynchronisées. Le gestionnaire de propriétés de photos fournit l’implémentation par défaut de **IPropertyStore** pour les images, et est utilisé par les applications, ainsi que par la Galerie de photos Windows et l’Explorateur Windows, pour s’assurer que toutes les métadonnées d’une image restent synchronisées et que les propriétés affichées par les applications sont cohérentes avec celles affichées par la Galerie de photos Windows et l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c7852-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="c7852-127">Quand le gestionnaire de propriétés de photos met à jour des métadonnées, il vérifie que ces propriétés sont mises à jour de manière cohérente dans tous les formats de métadonnées courants présents dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c7852-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="c7852-128">Le gestionnaire de propriétés de photos doit comprendre le format du conteneur et comment localiser les différentes propriétés qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="c7852-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="c7852-129">En général, le gestionnaire de propriétés de photos ne peut pas savoir comment les différents blocs de métadonnées sont disposés dans un format de conteneur propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c7852-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="c7852-130">Toutefois, si les métadonnées de votre format de conteneur sont disposées de la même façon que les métadonnées dans un format de conteneur TIFF ou JPEG, le gestionnaire de propriétés de photos peut tirer parti de cette connaissance pour mettre à jour les métadonnées de manière cohérente dans votre format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="c7852-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="c7852-131">Vous pouvez inscrire cette association en créant l’entrée de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="c7852-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="c7852-132">Cette entrée notifie le gestionnaire de propriétés de photos que le format de conteneur identifié par ce GUID comprend les mêmes chemins d’accès de langage de requête de métadonnées que le format de conteneur avec le GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span><span class="sxs-lookup"><span data-stu-id="c7852-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="c7852-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 est le GUID pour le format de conteneur TIFF.)</span><span class="sxs-lookup"><span data-stu-id="c7852-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="c7852-134">L’entrée suivante associe l’implémentation par défaut de **IPropertyStore** du gestionnaire de propriétés de photos à des fichiers portant l’extension « . ext ».</span><span class="sxs-lookup"><span data-stu-id="c7852-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="c7852-135">Le premier GUID est l’IID de l’interface **IPropertyStore** , tandis que le second est le GUID de l’implémentation du gestionnaire de propriétés de photos.</span><span class="sxs-lookup"><span data-stu-id="c7852-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="c7852-136">Les codecs qui utilisent un format propriétaire qui n’est pas compatible avec le format de conteneur TIFF ou JPEG doivent écrire leur propre implémentation **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="c7852-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="c7852-137">Intégration à la Galerie de photos Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="c7852-138">La Galerie de photos Windows est basée sur WIC et peut afficher tout format d’image compatible WIC pour lequel le codec est installé.</span><span class="sxs-lookup"><span data-stu-id="c7852-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="c7852-139">Pour informer le système que votre format d’image peut être ouvert dans la Galerie de photos Windows, vous devez créer une association de fichiers en créant les entrées de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7852-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="c7852-140">Le ProgID est généralement l’extension de nom de fichier ajoutée au mot « fichier ».</span><span class="sxs-lookup"><span data-stu-id="c7852-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="c7852-141">(Par exemple, si l’extension de nom de fichier est. txt, le ProgID est généralement « txtfile ».)</span><span class="sxs-lookup"><span data-stu-id="c7852-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="c7852-142">Il existe d’autres entrées de Registre standard que vous devrez peut-être créer pour prendre en charge les associations de fichiers. Toutefois, étant donné que les the’y ne sont pas spécifiques à WIC, ils n’entrent pas dans le cadre de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c7852-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="c7852-143">Intégration au cache de miniatures Windows</span><span class="sxs-lookup"><span data-stu-id="c7852-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="c7852-144">Les deux entrées suivantes indiquent que l’implémentation du fournisseur de miniatures WIC standard peut être utilisée pour récupérer des miniatures pour les fichiers avec cette extension.</span><span class="sxs-lookup"><span data-stu-id="c7852-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="c7852-145">Le premier GUID est l’IID de l’interface [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , tandis que le second est le GUID de l’implémentation standard du système de cette interface.</span><span class="sxs-lookup"><span data-stu-id="c7852-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="c7852-146">(Toutes les entrées sous HLCR \\ . ext \\ shellex \\ sont répétées sous HKCR \\ SystemFileAssociations \\ . ext \\ shellex \\ .)</span><span class="sxs-lookup"><span data-stu-id="c7852-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="c7852-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7852-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c7852-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c7852-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7852-149">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="c7852-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="c7852-150">Installation et inscription du CODEC</span><span class="sxs-lookup"><span data-stu-id="c7852-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="c7852-151">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c7852-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c7852-152">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c7852-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
