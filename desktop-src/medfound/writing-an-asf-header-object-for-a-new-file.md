---
description: Écriture d’un objet d’en-tête ASF pour un nouveau fichier
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Écriture d’un objet d’en-tête ASF pour un nouveau fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521153"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Écriture d’un objet d’en-tête ASF pour un nouveau fichier

L’objet ASF ContentInfo stocke les informations d’objet d’en-tête ASF pour un fichier. Lors de la création ou de la modification d’un fichier ASF, l’objet d’en-tête doit être généré. Pour ce faire, l’application doit fournir le profil d’encodage du contenu à l’objet ContentInfo afin qu’il sache les caractéristiques du fichier multimédia à créer.

Pour écrire un nouveau fichier, vous pouvez utiliser l’objet ContentInfo pour :

-   Collecter les informations d’en-tête à partir de l’objet profil du fichier à créer,
-   Remplir plusieurs objets d’en-tête dans la bibliothèque ASF gérée en interne par Media Foundation,
-   Initialiser le [multiplexeur ASF](asf-multiplexer.md) pour la génération de paquets de données ASF et
-   Construit l’objet d’en-tête de niveau supérieur au format binaire qui peut être écrit dans un fichier.

Pour plus d’informations sur les profils, consultez [ASF Profile](asf-profile.md).

Cette section contient les rubriques suivantes :



| Rubrique                                                                                                              | Description                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Initialisation de l’objet ContentInfo d’un nouveau fichier ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Décrit la méthode [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) qui initialise l’objet ContentInfo avec les informations d’en-tête stockées dans un objet de profil. |
| [Définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Informations sur les différentes propriétés de configuration qui doivent être définies sur l’objet ContentInfo.                                                                                         |
| [Génération d’un nouvel objet d’en-tête ASF](generating-a-new-asf-header-object.md)                                       | Comment générer une mémoire tampon de média, qui contient l’objet d’en-tête ASF réel du nouveau fichier, à partir de l’objet ContentInfo.                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objet ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

Structure de fichiers ASF
</dt> </dl>

 

 



