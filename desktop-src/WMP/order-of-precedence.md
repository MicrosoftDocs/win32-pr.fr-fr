---
title: Ordre de priorité
description: Ordre de priorité
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Fichiers multimédias, ordre de priorité
- Windows Fichiers multimédias, priorité
- sous-fichiers, ordre de priorité
- fichiers de préversion, précédence
- Windows Médias, sous-fichiers
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416213"
---
# <a name="order-of-precedence"></a>Ordre de priorité

Tous les attributs d’élément de métafichier ne sont pas égaux. Certains attributs d’éléments de métafichier remplacent d’autres attributs d’élément. Les attributs d’élément peuvent être remplacés par des attributs d’élément similaires en fonction de la position et de l’ordre. tous les attributs d’une sélection de métafichier remplacent ceux contenus dans un fichier multimédia Windows référencé. Un attribut qui remplace un autre a une priorité plus élevée.

La hiérarchie, prioritaire vers la plus faible, est indiquée dans le tableau suivant. L’élément de priorité la plus élevée n’est jamais remplacé.



| Étendue                    | Hierarchy                                   |
|--------------------------|---------------------------------------------|
| « Contenu DRM signé »     | Jamais substitué.                           |
| Portée de l’élément de **référence**    | Substitué uniquement par du contenu DRM signé.      |
| Portée de l’élément d' **entrée**  | Remplace les éléments des catégories ci-dessous. |
| Étendue **ASX**            | Remplace les éléments du fichier multimédia.              |
| Windows Étendue du fichier multimédia | Remplacé par tous les éléments ci-dessus.             |



 

-   « Contenu DRM signé »-objet de signature numérique.

    Les attributs du contenu DRM signé remplacent tous les autres. Par exemple, les informations de copyright de « contenu DRM signé » ne seront pas remplacées. Elle sera toujours diffusée en continu et présentée.

-   Portée de l’élément de **référence**

    Les attributs de l’élément **ref** remplacent les autres attributs d’élément, mais pas le contenu DRM signé.

-   Étendue de l' **entrée**

    Les attributs de l’élément **entry** seront remplacés par l’attribut de l’élément **ref** , mais ils remplaceront les autres attributs d’élément. Les métadonnées de **titre** de l’élément **entry** s’affichent à la place des informations de titre du fichier multimédia.

-   Étendue **ASX**

    toutes les propriétés entrées dans le métafichier remplacent celles contenues dans le fichier multimédia Windows. Les attributs de l’élément **entry** remplacent les attributs de l’élément **ASX** . Pendant la diffusion du clip multimédia référencé de l’élément d' **entrée** , les métadonnées de **titre** de l’élément d' **entrée** sont affichées à la place des informations de titre de l’élément **ASX** .

-   Windows Étendue du fichier multimédia

    les attributs du fichier multimédia Windows sont remplacés par tous les attributs de métafichier. Les métadonnées de fichier multimédia s’affichent uniquement si aucune métadonnée n’est définie pour cet élément dans le métafichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




