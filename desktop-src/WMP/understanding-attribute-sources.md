---
title: Fonctionnement des sources d’attributs
description: Fonctionnement des sources d’attributs
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Lecteur Windows Media, attributs pour les éléments multimédias
- Lecteur Windows Media modèle objet, attributs pour les éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Lecteur Windows Media Mobile, attributs pour les éléments multimédias
- Lecteur Windows Media ActiveX contrôle, attributs pour les éléments multimédias
- Lecteur Windows Media contrôle de ActiveX Mobile, attributs pour les éléments multimédias
- contrôle ActiveX, attributs pour les éléments multimédias
- bibliothèque de Lecteur Windows Media, attributs des éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403791"
---
# <a name="understanding-attribute-sources"></a>Fonctionnement des sources d’attributs

Les attributs, ou métadonnées, que vous pouvez utiliser proviennent de diverses sources. Cette rubrique décrit ces sources, en passant de scénarios avec moins d’attributs potentiels à ceux avec des attributs plus potentiels.

Pendant que l’utilisateur lit un CD ou un DVD, vous avez accès à très peu de métadonnées sur le disque lui-même ou le contenu multimédia du disque. Les disques commerciaux n’incluent généralement pas de métadonnées d’attribut.

Si l’utilisateur a lu un CD ou un DVD alors qu’ils étaient connectés à Internet, vous pouvez avoir accès à davantage d’attributs lorsque ce disque se trouve dans le lecteur de CD ou de DVD. si Lecteur Windows Media est connecté à Internet et lit un CD ou un DVD, le lecteur récupère les métadonnées de ce disque à partir d’une base de données en ligne. Le lecteur affiche ces informations dans la **lecture** et dans un nœud distinct de la bibliothèque. Les attributs ne sont pas stockés dans la base de données de bibliothèque, mais ils sont mis en cache. Si le cache n’a pas encore été vidé, votre application aura accès aux attributs pendant que le disque se trouve dans le lecteur.

> [!Note]  
> Les utilisateurs peuvent choisir de ne pas autoriser la récupération d’informations sur le média à partir d’une base de données en ligne. Dans ce cas, les seuls attributs disponibles sont ceux d’un fichier multimédia numérique, ceux que l’utilisateur a entrés manuellement dans la bibliothèque et ceux générés par le lecteur lui-même (par exemple, les attributs liés à la fréquence de lecture d’un élément).

 

Si l’utilisateur lit un fichier multimédia numérique qui n’est pas ajouté à la bibliothèque, vous avez accès aux attributs qui se trouvent dans le fichier.

Si l’utilisateur lit un fichier multimédia numérique qui a été ajouté à la bibliothèque, vous avez accès aux attributs qui sont stockés uniquement dans la bibliothèque, aux attributs stockés uniquement dans le fichier et aux attributs stockés à la fois dans la bibliothèque et dans le fichier.

Les attributs qui sont disponibles pour les éléments multimédias ajoutés à la bibliothèque varient en fonction de la façon dont le fichier multimédia numérique source a été créé et des actions effectuées par l’utilisateur depuis son ajout.

-   Le créateur du contenu peut insérer des informations d’attribut dans le fichier lors de sa création. Par exemple, si vous créez et distribuez un fichier multimédia numérique avec votre application, vous contrôlez les attributs insérés à l’origine dans le fichier.
-   si l’utilisateur modifie les données d’attribut d’un élément multimédia qui a été ajouté à la bibliothèque, à l’aide de l’éditeur de balises avancé ou de l’interface utilisateur de la bibliothèque, Lecteur Windows Media ajoute ces données à la base de données de bibliothèque. Le lecteur ajoute des attributs directement au fichier, car ils sont stockés uniquement dans le fichier. À un moment indéterminé, les attributs de lecture/écriture se synchronisent avec le fichier, de sorte que les attributs stockés dans la bibliothèque et le fichier ont la même valeur.
-   si l’utilisateur copie une piste à partir d’un CD à l’aide d’Lecteur Windows Media tout en étant connecté à Internet, l’effet est quasiment le même que si l’utilisateur avait modifié des attributs à l’aide de Lecteur Windows Media. Les attributs sont ajoutés à la base de données de bibliothèque, à partir du fichier lui-même et d’une base de données en ligne. Certains attributs sont stockés uniquement dans le fichier. À un moment indéterminé, la base de données de la bibliothèque se synchronise avec le fichier.
-   si vous écrivez du code à l’aide du contrôle Lecteur Windows Media pour modifier la valeur d’un attribut de lecture/écriture existant dans un élément multimédia qui a été ajouté à la bibliothèque, l’effet est quasiment le même que si l’utilisateur avait modifié l’attribut à l’aide de Lecteur Windows Media. La valeur est écrite dans la base de données de la bibliothèque et, à un moment indéterminé, la base de données est synchronisée avec le fichier.
-   [!Note]  
    > si vous incorporez le contrôle dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique, jusqu’à ce que l’utilisateur exécute Lecteur Windows Media. Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications. Dans les deux cas, les modifications sont immédiatement disponibles dans la bibliothèque.

     

-   si vous écrivez du code à l’aide du contrôle Lecteur Windows Media pour insérer un attribut personnalisé dans un élément multimédia, l’attribut et sa valeur persistent uniquement tant que votre application a une référence à l’objet **multimédia** . Ni l’attribut ni sa valeur ne seront stockés dans la base de données de bibliothèque ou le fichier multimédia numérique, le cas échéant.

La situation la plus simple est quand vous travaillez avec des fichiers multimédias numériques que vous avez fournis. Dans ce scénario, vous savez que des attributs spécifiques se trouvent dans le fichier. Lorsque vous ajoutez l’élément multimédia à la bibliothèque, vous savez que vous pouvez utiliser ces attributs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> </dl>

 

 




