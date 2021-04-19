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
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Intégration à la Galerie de photos Windows et à l’Explorateur Windows

Cette rubrique s’applique à Windows Vista et versions ultérieures. Il contient les sections suivantes :

-   [Introduction](#introduction)
-   [Intégration au magasin de propriétés Windows](#integration-with-the-windows-property-store)
-   [Intégration à la Galerie de photos Windows](#integration-with-the-windows-photo-gallery)
-   [Intégration au cache de miniatures Windows](#integration-with-the-windows-thumbnail-cache)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Pour permettre à la Galerie de photos Windows et à l’Explorateur Windows d’afficher des miniatures et de rechercher et mettre à jour des métadonnées d’image standard, un codec doit avoir une implémentation des interfaces [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) et [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associées. L’interface IThumbnailProvider est utilisée pour récupérer des miniatures et remplir le cache de miniatures, et l’interface IPropertyStore est utilisée pour la recherche et la mise à jour des métadonnées associées à un fichier. À compter de Windows Vista, tous les types de fichiers ont des miniatures et des métadonnées, mais différents types de fichiers requièrent des implémentations différentes de ces interfaces pour extraire ou générer les miniatures et les métadonnées correspondantes. Le système fournit des implémentations par défaut de ces interfaces. L’implémentation par défaut de IThumbnailProvider peut être utilisée pour tout format d’image compatible WIC (Windows Imaging Component). L’implémentation par défaut de IPropertyStore peut être utilisée avec n’importe quel format d’image compatible WIC basé sur un conteneur TIFF (Tagged Image File Format) ou JPEG. Pour associer votre format d’image aux implémentations par défaut de ces deux interfaces, vous devez ajouter quelques entrées de registre.

Les entrées suivantes indiquent à la Galerie de photos Windows et à l’Explorateur Windows qu’une extension de nom de fichier (. ext) et son type MIME associé sont associés à un format d’image.

L’entrée suivante indique aux fenêtres et aux applications qui utilisent le type de contenu (également appelé type MIME) qu’un fichier avec une extension donnée (. ext) est un format d’image. Le propriétaire du type de fichier doit choisir un `<image sub type value>` qui identifie de façon unique le format de fichier et cette valeur de type de contenu doit être inscrite auprès de l’IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

L’entrée suivante indique à Windows, Windows Search et les applications qui utilisent [System. Kind](../properties/props-system-kind.md) qu’une extension de nom de fichier (. ext) doit être traitée comme une image. Plus précisément, elle indique que la propriété System. Kind de l’extension de fichier doit être définie sur Picture.

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

## <a name="integration-with-the-windows-property-store"></a>Intégration au magasin de propriétés Windows

Parfois, les mêmes propriétés de métadonnées sont exposées dans différents schémas de métadonnées, souvent avec des noms de propriété différents. Quand l’une de ces propriétés est mise à jour, mais que les autres ne le sont pas, les métadonnées dans le fichier peuvent être désynchronisées. Le gestionnaire de propriétés de photos fournit l’implémentation par défaut de **IPropertyStore** pour les images, et est utilisé par les applications, ainsi que par la Galerie de photos Windows et l’Explorateur Windows, pour s’assurer que toutes les métadonnées d’une image restent synchronisées et que les propriétés affichées par les applications sont cohérentes avec celles affichées par la Galerie de photos Windows et l’Explorateur Windows. Quand le gestionnaire de propriétés de photos met à jour des métadonnées, il vérifie que ces propriétés sont mises à jour de manière cohérente dans tous les formats de métadonnées courants présents dans le fichier.

Le gestionnaire de propriétés de photos doit comprendre le format du conteneur et comment localiser les différentes propriétés qu’il contient. En général, le gestionnaire de propriétés de photos ne peut pas savoir comment les différents blocs de métadonnées sont disposés dans un format de conteneur propriétaire. Toutefois, si les métadonnées de votre format de conteneur sont disposées de la même façon que les métadonnées dans un format de conteneur TIFF ou JPEG, le gestionnaire de propriétés de photos peut tirer parti de cette connaissance pour mettre à jour les métadonnées de manière cohérente dans votre format de conteneur.

Vous pouvez inscrire cette association en créant l’entrée de Registre suivante. Cette entrée notifie le gestionnaire de propriétés de photos que le format de conteneur identifié par ce GUID comprend les mêmes chemins d’accès de langage de requête de métadonnées que le format de conteneur avec le GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 est le GUID pour le format de conteneur TIFF.)

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

L’entrée suivante associe l’implémentation par défaut de **IPropertyStore** du gestionnaire de propriétés de photos à des fichiers portant l’extension « . ext ». Le premier GUID est l’IID de l’interface **IPropertyStore** , tandis que le second est le GUID de l’implémentation du gestionnaire de propriétés de photos.

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

Les codecs qui utilisent un format propriétaire qui n’est pas compatible avec le format de conteneur TIFF ou JPEG doivent écrire leur propre implémentation **IPropertyStore** .

## <a name="integration-with-the-windows-photo-gallery"></a>Intégration à la Galerie de photos Windows

La Galerie de photos Windows est basée sur WIC et peut afficher tout format d’image compatible WIC pour lequel le codec est installé. Pour informer le système que votre format d’image peut être ouvert dans la Galerie de photos Windows, vous devez créer une association de fichiers en créant les entrées de Registre suivantes.

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

Le ProgID est généralement l’extension de nom de fichier ajoutée au mot « fichier ». (Par exemple, si l’extension de nom de fichier est. txt, le ProgID est généralement « txtfile ».)

Il existe d’autres entrées de Registre standard que vous devrez peut-être créer pour prendre en charge les associations de fichiers. Toutefois, étant donné que les the’y ne sont pas spécifiques à WIC, ils n’entrent pas dans le cadre de cette rubrique.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Intégration au cache de miniatures Windows

Les deux entrées suivantes indiquent que l’implémentation du fournisseur de miniatures WIC standard peut être utilisée pour récupérer des miniatures pour les fichiers avec cette extension. Le premier GUID est l’IID de l’interface [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , tandis que le second est le GUID de l’implémentation standard du système de cette interface. (Toutes les entrées sous HLCR \\ . ext \\ shellex \\ sont répétées sous HKCR \\ SystemFileAssociations \\ . ext \\ shellex \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Entrées de Registre spécifiques à l’encodeur](-wic-decoderregentries.md)
</dt> <dt>

[Installation et inscription du CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
