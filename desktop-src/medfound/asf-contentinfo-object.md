---
description: Objet ASF ContentInfo
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objet ASF ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517215"
---
# <a name="asf-contentinfo-object"></a>Objet ASF ContentInfo

L’objet ASF *ContentInfo* stocke les informations de l’objet d’en-tête ASF d’un fichier. Une application peut utiliser l’objet ContentInfo pour les raisons suivantes :

-   Lire l’objet d’en-tête d’un fichier multimédia existant. Dans ce cas, l’objet ContentInfo analyse l’objet d’en-tête et stocke les informations sur le fichier de caractéristiques. Media Foundation expose plusieurs de ces propriétés via des attributs et des interfaces. Celles-ci sont décrites dans [Media Foundation attributs pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md).
-   Écrire des informations d’en-tête et construire un objet d’en-tête pour un nouveau fichier.
-   Initialiser d’autres objets ASF tels que le [séparateur ASF](asf-splitter.md), le [multiplexeur ASF](asf-multiplexer.md)et l’indexeur ASF, lors de la lecture ou de l’écriture d’un fichier multimédia.

Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Création de l’objet ContentInfo

Pour créer une nouvelle instance de l’objet ContentInfo, appelez la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) . Cette méthode retourne un pointeur vers un objet ContentInfo vide qui doit être initialisé pour fonctionner avec un fichier ASF spécifique. Selon que l’application lit un fichier existant ou écrit un nouveau fichier ASF, elle doit appeler [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ou [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour remplir l’objet vide.

Pour plus d’informations sur ces appels de méthode, consultez les rubriques suivantes :

-   [Lecture de l’objet d’en-tête ASF d’un fichier existant](reading-the-asf-header-object-of-an-existing-file.md)
-   [Obtention d’informations à partir d’objets d’en-tête ASF](getting-information-from-asf-header-objects.md)
-   [Écriture d’un objet d’en-tête ASF pour un nouveau fichier](writing-an-asf-header-object-for-a-new-file.md)
-   [Attributs Media Foundation pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



