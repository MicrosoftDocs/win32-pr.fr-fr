---
description: Encoder-Specific les entrées de Registre
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific les entrées de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711228"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific les entrées de Registre


en plus des entrées listées ci-dessus pour l’encodeur, vous devez également inscrire votre encodeur sous la catégorie des encodeurs de composant Windows Imaging (WIC) pour que le moteur de découverte puisse le trouver. Pour ce faire, vous devez créer les entrées de Registre suivantes. Le premier GUID dans les entrées suivantes est l’identificateur de catégorie (CATID) pour WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Inscription d’un format de conteneur avec des enregistreurs de métadonnées

Si vous créez un nouveau format de conteneur pour votre codec, vous devez également créer des entrées de Registre pour prendre en charge les enregistreurs de métadonnées pour les blocs de métadonnées dans vos images. Les entrées suivantes doivent être créées sous l’identificateur de classe (CLSID) de l’enregistreur de métadonnées pour chaque format de métadonnées pris en charge dans votre format de conteneur. Si votre codec utilise un conteneur TIFF (Tagged Image File Format), ces informations se trouvent déjà dans le registre et vous n’avez pas besoin de créer ces entrées.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

Si vous utilisez un format de conteneur de style TIFF ou JPEG, vous devez inscrire une association entre votre conteneur et ce format de conteneur. pour plus d’informations, consultez la présentation de l' [intégration avec Windows galerie de photos et Windows Explorer](-wic-integrationregentries.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Entrées de Registre générales](-wic-generalregentries.md)
</dt> <dt>

[Entrées de Registre spécifiques à l’encodeur](-wic-decoderregentries.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



