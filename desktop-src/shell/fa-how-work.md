---
description: Les associations de fichiers définissent la façon dont l’interpréteur de commandes traite un type de fichier sur le système.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Fonctionnement des associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd12386ec7e850d160a6377ddff9b807e6dccfe101ad45285bdc9d7f2661a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032727"
---
# <a name="how-file-associations-work"></a>Fonctionnement des associations de fichiers

Les associations de fichiers définissent la façon dont l’interpréteur de commandes traite un [type de fichier](fa-file-types.md) sur le système.

Cette rubrique est organisée comme suit :

-   [À propos des associations de fichiers](#about-file-associations)
-   [Lorsque vous devez implémenter ou modifier des associations de fichiers](#when-you-should-implement-or-modify-file-associations)
-   [Fonctionnement des associations de fichiers](#how-file-associations-work)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-file-associations"></a>À propos des associations de fichiers

Les associations de fichiers contrôlent les fonctionnalités suivantes :

-   L’application qui démarre lorsqu’un utilisateur double-clique sur un fichier.
-   L’icône qui s’affiche pour un fichier par défaut.
-   mode d’affichage du type de fichier dans Windows Explorer.
-   Les commandes qui s’affichent dans le menu contextuel d’un fichier.
-   Autres fonctionnalités de l’interface utilisateur, telles que les info-bulles, les informations de vignette et le volet d’informations.

Les développeurs d’applications peuvent utiliser des associations de fichiers pour contrôler la façon dont l’interpréteur de commandes traite les types de fichiers personnalisés, ou pour associer une application à des types de fichiers existants. Par exemple, lorsqu’une application est installée, l’application peut vérifier la présence d’associations de fichiers existantes et créer ou remplacer ces associations de fichiers.

Les utilisateurs peuvent contrôler certains aspects des associations de fichiers pour personnaliser la façon dont l’interpréteur de commandes traite un type de fichier à l’aide de l’interface utilisateur **ouverte** ou de la modification du Registre.

dans la fenêtre de l’explorateur de Windows présentée dans la capture d’écran ci-dessous, l’interpréteur de commandes affiche différentes icônes pour chaque fichier, en fonction de l’icône associée au type de fichier. si l’utilisateur double-clique sur l' **image Bitmap** de l’exemple de fichier, le Shell lance Paint et l’utilise pour ouvrir le fichier, car sur ce système, Paint est associé à .bmp fichiers. Les utilisateurs peuvent contrôler ces actions à l’aide d’associations de fichiers.

![illustration du fonctionnement des associations de fichiers dans la pratique](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Lorsque vous devez implémenter ou modifier des associations de fichiers

Les applications peuvent utiliser des fichiers à diverses fins : certains fichiers sont utilisés exclusivement par l’application et ne sont généralement pas accessibles aux utilisateurs, tandis que d’autres fichiers sont créés par l’utilisateur et sont souvent ouverts, recherchés et consultés à partir de l’interpréteur de commandes.

À moins que votre type de fichier personnalisé ne soit utilisé exclusivement par l’application, vous devez implémenter des associations de fichiers pour celui-ci. En règle générale, implémentez des associations de fichiers pour votre type de fichier personnalisé si vous vous attendez à ce que l’utilisateur interagisse directement avec ces fichiers. Cela comprend l’utilisation de l’interpréteur de commandes pour parcourir et ouvrir les fichiers, Rechercher le contenu ou les propriétés des fichiers et afficher un aperçu des fichiers.

Si votre application gère un type de fichier existant, ne modifiez pas l’Association de fichiers, sauf si vous souhaitez modifier la façon dont l’interpréteur de commandes gère tous les fichiers de ce type.

## <a name="how-file-associations-work"></a>Fonctionnement des associations de fichiers

Les fichiers sont exposés dans le shell en tant qu’éléments de l’interpréteur de commandes. Pour contrôler les associations de fichiers, les développeurs d’applications peuvent inscrire un mappage entre le type de fichier et les gestionnaires (objets COM qui fournissent des fonctionnalités pour les éléments de Shell du type de fichier). Lorsque l’interpréteur de commandes doit interroger les associations de fichiers d’un type de fichier, il crée un tableau de clés de registre contenant les associations pour le type de fichier et vérifie ces clés pour les associations de fichiers appropriées à utiliser.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour obtenir des informations conceptuelles sur les associations de fichiers, consultez [vue d’ensemble des verbes et des associations de fichiers](fa-verbs.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 



