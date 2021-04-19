---
description: Prise en charge ASF dans Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Prise en charge ASF dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522274"
---
# <a name="asf-support-in-media-foundation"></a>Prise en charge ASF dans Media Foundation

Media Foundation prend en charge les fichiers multimédias au format ASF (Advanced Systems Format) :

-   Windows Media Video (fichiers WMV)
-   Windows Media Audio (fichiers WMA)

Media Foundation fournit plusieurs objets pour la lecture et l’écriture de fichiers ASF. Ces objets sont fournis dans deux couches architecturales différentes.

Tout d’abord, la couche de *pipeline* contient des objets qui fonctionnent dans le [pipeline Media Foundation](media-foundation-pipeline.md) et sont conformes aux API définies par le pipeline. La couche de pipeline ASF contient les éléments suivants :

-   [Source du média ASF](asf-media-source.md): analyse les fichiers ASF et remet les paquets de données audio/vidéo.
-   [Codecs Windows Media](windows-media-codecs.md): décodez ou encodez des flux audio ou vidéo Windows Media.
-   [Récepteur multimédia ASF](asf-media-sinks.md): reçoit les paquets de données et écrit un fichier ASF.

Deuxièmement, la couche de conteneur WM offre un contrôle de bas niveau de l’analyse et de l’écriture d’un fichier ASF. La couche de pipeline utilise WMContainer en interne. Les applications peuvent également utiliser WMContainer pour l’analyse et l’écriture ASF de bas niveau.

![Diagramme montrant les éléments de la couche de pipeline et le conteneur WM](images/asf-components.png)

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                         | Description                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Structure de fichiers ASF](asf-file-structure.md)<br/>                       | Vue d’ensemble de la structure de fichiers ASF et des objets fournis par Media Foundation pour travailler avec des fichiers ASF.<br/> |
| [Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)<br/> | Décrit comment analyser et créer des fichiers ASF à l’aide de la couche de pipeline.<br/>                                   |
| [Composants WMContainer ASF](wmcontainer-asf-components.md)<br/>       | Décrit comment analyser et créer des fichiers ASF à l’aide de la couche WMContainer.<br/>                                |



 

Pour plus d’informations sur la structure d’un fichier ASF, consultez la spécification ASF, qui peut être téléchargée à partir de ce [site Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




