---
description: Indexeur ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexeur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544603"
---
# <a name="asf-indexer"></a>Indexeur ASF

L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format). Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

Une application peut utiliser l’indexeur pour effectuer une recherche en fonction de l’heure de la présentation ou pour générer de nouvelles entrées d’index pour un fichier ASF. L’indexeur ASF implémente l’interface [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type d’index</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Index basé sur l’heure de la présentation</td>
<td>Fournit une indexation basée sur la durée de la présentation pour les flux audio et vidéo dans des blocs d’index afin de rendre l’indexation plus efficace. Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets. <br/> Le décalage correspond à la position du paquet de données en cours de recherche, par rapport au début de l’objet de données ASF.<br/> GUID_NULL doit être utilisé comme type de GUID pour l’identificateur d’index. Pour plus d’informations, consultez <a href="using-the-indexer-to-write-a-new-index.md">utilisation de l’indexeur pour écrire un nouvel index</a>.<br/></td>
</tr>
<tr class="even">
<td>Index du code temporel</td>
<td>Facilite la recherche par code temporel dans les flux qui contiennent des métadonnées de code temporel. Les codes temporels sont conformes à un format SMPTE (<em>heures : minutes : secondes : images</em>). Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets. <br/> Le décalage correspond à la position du paquet de données en cours de recherche, par rapport au début de l’objet de données ASF.<br/>
<blockquote>
[!Note]<br />
Les objets d’index de code temporel ne sont pas pris en charge actuellement.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Index basé sur des frames</td>
<td>Fournit l’indexation basée sur des frames pour les flux vidéo. Les index dans l’index basé sur des trames sont en termes de nombres d’images, avec le premier frame pour un flux de fichier ASF correspondant à l’entrée 0 dans l’objet d’index basé sur des trames. Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets.<br/>
<blockquote>
[!Note]<br />
Les objets d’index basés sur des frames ne sont pas pris en charge actuellement.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Cette section contient les rubriques suivantes :



| Rubrique                                                                                | Description                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Création et configuration de l’indexeur](indexer-creation-and-configuration.md)         | Comment créer un objet indexeur et le configurer pour la lecture d’un index existant ou pour l’écriture d’un nouvel objet d’index ASF pour un fichier. |
| [Utilisation de l’indexeur pour rechercher dans un fichier](using-the-indexer-to-seek.md)                 | Comment utiliser l’indexeur pour rechercher dans un fichier ASF.                                                                               |
| [Utilisation de l’indexeur pour écrire un nouvel index](using-the-indexer-to-write-a-new-index.md) | Comment utiliser l’indexeur pour générer des entrées d’index et écrire un nouvel objet d’index pour un fichier ASF.                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




