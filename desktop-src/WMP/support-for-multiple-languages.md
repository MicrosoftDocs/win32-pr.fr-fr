---
title: Prise en charge de plusieurs langues
description: Prise en charge de plusieurs langues
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Sélections de métafichiers Windows Media, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Sélections de métafichiers Windows Media, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Sélections de métafichiers Windows Media, prise en charge des langues
- sélections de métafichiers, prise en charge des langues
- sélections, prise en charge des langues
- prise en charge de plusieurs langues
- prise en charge multilingue
- prise en charge d'autres langues
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029691"
---
# <a name="support-for-multiple-languages"></a>Prise en charge de plusieurs langues

Le lecteur Windows Media série 9 ou version ultérieure prend en charge les fichiers Windows Media créés à l’aide du jeu de caractères Unicode. Cela vous permet d’inclure des métadonnées multilingues dans votre sélection de métafichiers. Les règles suivantes régissent l’utilisation des métadonnées multilingues dans les fichiers Windows Media :

-   Les caractères doivent être encodés à l’aide du schéma d’encodage UTF-8.
-   La sélection de métafichier doit inclure le **paramètre** suivant au niveau de la sélection :
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Seul le lecteur Windows Media série 9 ou version ultérieure prend en charge cette fonctionnalité.
-   Si la sélection de métafichiers n’est pas enregistrée avec l’encodage UTF-8 et l’élément **param** correct, elle est analysée à l’aide de la page de codes des paramètres régionaux système par défaut de l’ordinateur de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Élément PARAM**](param-element.md)
</dt> <dt>

[**Présentation des fichiers Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




