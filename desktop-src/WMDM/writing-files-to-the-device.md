---
title: Écriture de fichiers sur l’appareil
description: Écriture de fichiers sur l’appareil
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Gestionnaire de périphériques Windows Media, écriture de fichiers sur des appareils
- Gestionnaire de périphériques, écriture de fichiers sur des appareils
- Guide de programmation, écriture de fichiers sur des appareils
- applications de bureau, écriture de fichiers sur des appareils
- création d’applications Windows Media Gestionnaire de périphériques, écriture de fichiers sur des appareils
- écriture de fichiers sur des appareils, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507058"
---
# <a name="writing-files-to-the-device"></a>Écriture de fichiers sur l’appareil

Avant d’envoyer un fichier à un appareil, votre application doit connaître les types de fichiers et de formats que l’appareil peut gérer, afin que l’application puisse déterminer si le fichier doit être transcodé avant d’envoyer ou envoyé, ou s’il n’a pas été envoyé du tout.

Les étapes suivantes montrent comment envoyer un fichier existant à l’appareil. Pour créer un nouveau fichier sur l’appareil, par exemple une sélection, consultez [création d’une sélection sur l’appareil](creating-a-playlist-on-the-device.md).

1.  Obtient le format du fichier que vous souhaitez envoyer à l’appareil. Pour plus d’informations, consultez [découverte du format d’un fichier](discovering-a-files-format.md).
2.  Si l’appareil est destiné à lire le fichier,
    -   Interrogez le fichier sur ses fonctionnalités de format. Pour plus d’informations, consultez [découverte des fonctionnalités de format des appareils](discovering-device-format-capabilities.md).
    -   Recherchez un format acceptable que l’application peut créer à partir du fichier d’origine.
    -   Si le fichier doit être transcodé, transcodez-le.
3.  Recherchez un stockage parent pour le nouvel objet. Windows Media Gestionnaire de périphériques ne permet pas de découvrir l’emplacement de stockage standard pour tous les types de fichiers spécifiques (fichiers vidéo ou audio, WMV ou BMP, dossier « Favoris », etc.). vous devez donc examiner chaque appareil pour essayer de déterminer où stocker le nouvel objet. (D’autres applications appliquent une certaine structure de dossiers, par exemple, le lecteur Windows Media crée des albums, des sélections et des dossiers musicaux dans lesquels le dossier musique contient un artiste et une hiérarchie AlbumName. Pour cette raison, et comme certains périphériques n’ont peut-être pas été testés avec un logiciel autre que le lecteur Windows Media, sachez que le placement d’objets de sélection ou d’album dans un dossier autre que les dossiers de sélection ou d’albums peut parfois entraîner la non-fonctionnement des objets sur certains appareils.)
4.  Si le stockage cible prend en charge [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), créez une nouvelle interface de métadonnées en appelant [**IWMDMStorage3 :: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Définissez les métadonnées sur une interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) . Pour plus d’informations, consultez [définition de métadonnées sur un fichier](setting-metadata-on-a-file.md). Les seules métadonnées requises sont g \_ wszWMDMFormatCode (une valeur [**\_ FORMATCODE WMDM**](wmdm-formatcode.md) décrivant le contenu), mais plus vous pouvez fournir de métadonnées, plus le transfert sera efficace pour le fournisseur de services.
5.  Envoyez le fichier à l’appareil à l’aide de la méthode [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)ou [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) . **Insert3** vous permet d’inclure les métadonnées sur l’appareil dans le cadre de la méthode. Pour plus d’informations, consultez [envoi du fichier à l’appareil](sending-the-file-to-the-device.md).

Du code illustrant chacune de ces étapes est fourni sur les pages de rubrique liées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’une application Windows Media Gestionnaire de périphériques**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




