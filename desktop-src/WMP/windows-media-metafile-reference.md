---
title: Windows Référence du métafichier multimédia
description: Windows Référence du métafichier multimédia
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Fichiers multimédias, référence
- sous-fichiers, référence
- référence pour Windows les fichiers multimédias
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b00cd604ec94c42ef90f08a8875edb4fda92ba8267c7e4a7d7b5505c2fb57932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862259"
---
# <a name="windows-media-metafile-reference"></a>Windows Référence du métafichier multimédia

cette référence décrit les éléments et les extensions de nom de fichier pour Windows les fichiers multimédias. La référence est divisée en sections suivantes.



| Section                                                                                    | Description                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Informations de référence sur les éléments de métafichier multimédia](windows-media-metafile-elements-reference.md) | Documente les éléments de métafichier, y compris les définitions, les attributs et leurs valeurs, ainsi que les conditions spéciales associées à chaque élément. |
| [Extensions de noms de fichiers](file-name-extensions.md)                                           | Documente les extensions de nom de fichier de métafichier avec des règles et des instructions sur leur utilisation.                                                  |



 

Windows Les sous-fichiers multimédias sont des fichiers texte qui fournissent des informations sur un flux de fichier et sa présentation. Les sous-fichiers sont basés sur la syntaxe du Extensible Markup Language (XML) et sont constitués d’éléments de type XML avec leurs balises et leurs attributs. Chaque élément définit un paramètre ou une action pour la diffusion multimédia en continu.

Deux ensembles de balises d’éléments sont disponibles pour les fichiers de configuration. Les fichiers de configuration côté client ont un ensemble d’éléments, et les fichiers de configuration côté serveur ont un autre ensemble d’éléments.

Si une balise d’élément n’a pas d’éléments enfants (ceux qui modifient ou sont contenus dans un autre élément), un caractère de barre oblique (/) peut être utilisé à la fin de la balise d’ouverture à la place d’une balise de fermeture. Si les éléments enfants n’apparaissent pas entre les balises d’ouverture et de fermeture d’un élément, ils ne sont pas des éléments enfants pour cet élément et sont ignorés ou provoquent une erreur dans la syntaxe du métafichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos des Windows de fichiers multimédias**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Fichiers multimédias**](windows-media-metafiles.md)
</dt> </dl>

 

 




