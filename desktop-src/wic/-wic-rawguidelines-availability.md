---
description: Disponibilité du codec et prise en charge des plateformes
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilité du codec et prise en charge des plateformes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204213"
---
# <a name="codec-availability-and-platform-support"></a>Disponibilité du codec et prise en charge des plateformes

Microsoft recommande aux fournisseurs d’appareils photo de mettre à jour les codecs WIC dans la distribution de logiciels avec les nouvelles caméras et d’installer le codec mis à jour avec l’installation du logiciel du fournisseur par défaut Windows 7, Windows Vista et Windows XP. Les fournisseurs d’appareils photo doivent également fournir le dernier codec WIC en téléchargement à partir de leurs sites de support.

## <a name="codec-discovery"></a>Détection de codec

Microsoft fait ce qui suit pour aider à pointer les utilisateurs vers les sites Web des fournisseurs pour les téléchargements de codec :

-   Dans l’Explorateur Windows, si un utilisateur double-clique sur un fichier qui n’est pas reconnu (cas par défaut lorsqu’un fichier brut se trouve sur l’ordinateur, mais que le codec n’est pas encore installé), une boîte de dialogue indique que le fichier n’est pas reconnu et vous demande si l’utilisateur souhaite trouver un programme qui comprend le fichier. Microsoft gère un service de redirection existant pour transférer les utilisateurs vers les sites Web des fournisseurs qui peuvent fournir le programme pour comprendre le fichier. Cette fonctionnalité existe dans Windows XP et Windows Vista.
-   La Galerie de photos Windows, la Galerie de photos Windows Live et la visionneuse de photos Windows 7 reconnaissent un ensemble d’extensions de fichier en tant que fichiers BRUTs. Si des fichiers de ce jeu sont trouvés dans des dossiers que ces applications examinent et qu’un codec pour le fichier n’est pas déjà installé, une boîte de dialogue s’affiche, comme décrit dans le paragraphe précédent.

Pour plus d’informations sur la détection des codecs, consultez disponibilité du codec et prise en charge de la plateforme.

## <a name="windows-xp-platform-support"></a>Prise en charge des plateformes Windows XP

Microsoft a publié Windows XP SP3 avec WIC et un programme d’installation autonome de WIC pour Windows XP SP2. Celles-ci utilisent des codecs WIC pour permettre la prise en charge des miniatures et des aperçus sur ces plateformes. Par conséquent, il est important que le téléchargement et l’installation du codec soient pris en charge et testés sur Windows 7, Windows Vista et Windows XP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



