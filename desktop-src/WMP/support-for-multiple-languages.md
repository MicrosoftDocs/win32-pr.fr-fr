---
title: Prise en charge de plusieurs langues
description: Prise en charge de plusieurs langues
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Sélections de métafichiers multimédias, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Windows Sélections de métafichiers multimédias, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Windows Sélections de métafichiers multimédias, prise en charge des langues
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002069"
---
# <a name="support-for-multiple-languages"></a>Prise en charge de plusieurs langues

Lecteur Windows Media série 9 ou version ultérieure prend en charge Windows les fichiers multimédias créés à l’aide du jeu de caractères Unicode. Cela vous permet d’inclure des métadonnées multilingues dans votre sélection de métafichiers. les règles suivantes régissent l’utilisation des métadonnées multilingues dans Windows les méta-fichiers multimédias :

-   Les caractères doivent être encodés à l’aide du schéma d’encodage UTF-8.
-   La sélection de métafichier doit inclure le **paramètre** suivant au niveau de la sélection :
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   seule Lecteur Windows Media série 9 ou ultérieure prend en charge cette fonctionnalité.
-   Si la sélection de métafichiers n’est pas enregistrée avec l’encodage UTF-8 et l’élément **param** correct, elle est analysée à l’aide de la page de codes des paramètres régionaux système par défaut de l’ordinateur de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Élément PARAM**](param-element.md)
</dt> <dt>

[**Windows Présentation des fichiers multimédias**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




