---
title: Informations de référence sur les métafichiers Windows Media
description: Informations de référence sur les métafichiers Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Fichiers Windows Media, référence
- sous-fichiers, référence
- référence pour les fichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029174"
---
# <a name="windows-media-metafile-reference"></a>Informations de référence sur les métafichiers Windows Media

Cette référence décrit les éléments et les extensions de nom de fichier pour les fichiers Windows Media. La référence est divisée en sections suivantes.



| Section                                                                                    | Description                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Informations de référence sur les éléments de métafichier Windows Media](windows-media-metafile-elements-reference.md) | Documente les éléments de métafichier, y compris les définitions, les attributs et leurs valeurs, ainsi que les conditions spéciales associées à chaque élément. |
| [Extensions de noms de fichiers](file-name-extensions.md)                                           | Documente les extensions de nom de fichier de métafichier avec des règles et des instructions sur leur utilisation.                                                  |



 

Les fichiers Windows Media sont des fichiers texte qui fournissent des informations sur un flux de fichier et sa présentation. Les sous-fichiers sont basés sur la syntaxe du Extensible Markup Language (XML) et sont constitués d’éléments de type XML avec leurs balises et leurs attributs. Chaque élément définit un paramètre ou une action pour la diffusion multimédia en continu.

Deux ensembles de balises d’éléments sont disponibles pour les fichiers de configuration. Les fichiers de configuration côté client ont un ensemble d’éléments, et les fichiers de configuration côté serveur ont un autre ensemble d’éléments.

Si une balise d’élément n’a pas d’éléments enfants (ceux qui modifient ou sont contenus dans un autre élément), un caractère de barre oblique (/) peut être utilisé à la fin de la balise d’ouverture à la place d’une balise de fermeture. Si les éléments enfants n’apparaissent pas entre les balises d’ouverture et de fermeture d’un élément, ils ne sont pas des éléments enfants pour cet élément et sont ignorés ou provoquent une erreur dans la syntaxe du métafichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des fichiers Windows Media**](about-windows-media-metafiles.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Fichiers Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




