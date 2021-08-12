---
title: Création d’une sélection sur l’appareil
description: Création d’une sélection sur l’appareil
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Gestionnaire de périphériques de média, sélections
- Gestionnaire de périphériques, sélections
- Guide de programmation, sélections
- applications de bureau, sélections
- création d’applications de Gestionnaire de périphériques multimédia Windows, sélections
- sélections abstraites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a61d45c234f1cdbe03a713e4d10568fa45c83bdd90227b815c85b0f544d2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585862"
---
# <a name="creating-a-playlist-on-the-device"></a>Création d’une sélection sur l’appareil

le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques offre à une application MTP la possibilité de créer une sélection sur un appareil. Ce type de playlist est appelé une sélection *abstraite* , car le fichier créé sur l’appareil ne contient aucune donnée multimédia, mais uniquement les métadonnées qui contiennent les liens vers les fichiers multimédias de la sélection.

Les autres éléments abstraits qui peuvent être créés sur l’appareil incluent les listes de sélection avec des propriétés supplémentaires, telles que les jaquettes, les contacts et les messages.

**Pour créer une sélection**

1.  Acquérir une interface [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) sur l’appareil cible.
2.  Appelez [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) pour obtenir la \_ propriété g wszWMDMFormatsSupported.
3.  Si aucun format de sélection n’est pris en charge, interdisez l’envoi de playlists à l’appareil et ignorez les étapes suivantes. Sinon, choisissez le code de format pris en charge par l’appareil qui correspond le mieux au type d’objet souhaité. Les codes de \_ format Generic WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST et WMDM \_ FORMATCODE ABSTRACTAUDIOLAYLIST \_ sont les plus couramment pris en charge.
4.  Obtenez une interface [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) pour le stockage (la racine ou un dossier) dans lequel vous souhaitez créer l’objet. Certains appareils fonctionnent mieux si l’objet de sélection est placé dans un dossier de niveau supérieur nommé « playlists ».
5.  Créez un objet de métadonnées vide à l’aide de [**IWMDMStorage3 :: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  À l’aide de l’interface **IWMDMMetaData** obtenue à l’étape précédente, appelez [**IWMDMMetaData :: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) pour ajouter le code de format que vous avez choisi (de l’étape 3) aux propriétés de métadonnées de stockage.
7.  Obtenez l’interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) à partir de l’interface **IWMDMStorage3** .
8.  Appelez [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) pour insérer un nouveau fichier de sélection dans le stockage sélectionné. Ce fichier contient les métadonnées représentées par l’interface **IWMDMMetaData** que vous avez créée à l’étape 5 et passée à **Insert3**. La méthode retourne une interface **IWMDMStorage** pour le fichier de sélection ; vous pouvez interroger l’interface [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .
9.  Appelez [**IWMDMStorage4 :: SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) pour créer des références aux interfaces **IWMDMStorage** des fichiers multimédias de la sélection.

Pour obtenir un exemple de code, consultez la \_ fonction OnCreatePlaylist dans l' [exemple d’application de bureau](sample-desktop-application.md).

> [!Note]  
> Le fournisseur de services MTP fourni par Microsoft permet à une application de définir des références dans les métadonnées. Pour implémenter des sélections, votre application doit communiquer avec un périphérique MTP ou à l’aide d’un fournisseur de services personnalisé capable de gérer des objets abstraits. Le fournisseur de services CE gère les objets de sélection et d’album.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers sur l’appareil**](writing-files-to-the-device.md)
</dt> </dl>

 

 




