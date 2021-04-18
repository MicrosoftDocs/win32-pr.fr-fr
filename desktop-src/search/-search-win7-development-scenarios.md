---
description: Décrit l’introduction des bibliothèques pour Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Bibliothèques de shell Windows dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106533699"
---
# <a name="windows-shell-libraries-in-windows"></a>Bibliothèques de shell Windows dans Windows

Cette rubrique décrit l’introduction des bibliothèques pour Windows 7 et versions ultérieures. Les bibliothèques sont une fonctionnalité de l’interpréteur de commandes Windows. Pour accéder aux fonctionnalités de l’interpréteur de commandes Windows, telles que les bibliothèques, les développeurs tiers d’applications de recherche Windows doivent tout d’abord implémenter un magasin de données Shell. Pour plus d’informations, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Cette rubrique est organisée comme suit :

- [Bibliothèques](#libraries)
  - [Points d’entrée des données utilisateur](#user-data-entry-points)
  - [Collections de dossiers](#collections-of-folders)
  - [Dossiers pris en charge dans les bibliothèques](#supported-folders-in-libraries)
  - [Stockage-sauvegardé](#storage-backed)
  - [Conteneurs d’interpréteur de commandes de système non-fichier](#non-file-system-shell-containers)
  - [Descriptions de la bibliothèque](#library-descriptions)
- [Rubriques connexes](#related-topics)

## <a name="libraries"></a>Bibliothèques

Dans Windows 7 et versions ultérieures, les bibliothèques sont le référentiel par défaut des données utilisateur. Les utilisateurs peuvent parcourir leurs fichiers de la même façon qu’ils le font dans un dossier, ou ils peuvent afficher leurs fichiers organisés par propriétés telles que date, type et auteur. Contrairement à un dossier, une bibliothèque ne stocke pas réellement d’éléments, mais affiche des fichiers qui sont stockés dans plusieurs dossiers en même temps. Les bibliothèques fournissent un point d’accès unique et une vue enrichie pour les utilisateurs de leur contenu agrégé. Par exemple, si un utilisateur a des fichiers musicaux dans des dossiers situés sur un lecteur externe, en plus du dossier **ma musique** , il peut accéder immédiatement à tous les fichiers musicaux via la bibliothèque musique.

### <a name="user-data-entry-points"></a>Points d’entrée des données utilisateur

Les bibliothèques par défaut (telles que **Mes documents**, **Mes images**, etc.) sont l’équivalent d’un [dossier connu](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). Les bibliothèques par défaut fournissent des points d’entrée familiers aux utilisateurs, mais étant donné que le contenu de la bibliothèque n’est pas limité aux bibliothèques de contenu de dossiers connus, les utilisateurs peuvent plus de liberté pour déterminer l’emplacement de stockage des documents et des médias. Les bibliothèques sont exposées par le biais de l’espace de noms Shell (source de données Shell). Votre application peut fournir aux utilisateurs les mêmes points d’entrée familiers à leurs données en activant la reconnaissance de la bibliothèque et en parcourant la navigation.

### <a name="collections-of-folders"></a>Collections de dossiers

Les bibliothèques sont des collections de contenu définies par l’utilisateur. Windows Search indexe les dossiers pris en charge lorsqu’ils sont inclus dans les bibliothèques. Cela permet d’effectuer une recherche instantanée et des vues de la structure de pile basée sur les propriétés dans les bibliothèques.

### <a name="supported-folders-in-libraries"></a>Dossiers pris en charge dans les bibliothèques

Pour que les dossiers soient pris en charge dans les bibliothèques, ils doivent être indexables sur l’ordinateur local et indexés sur un ordinateur Windows distant, ou indexés sur un serveur avec les fichiers indexés par la recherche Windows.

Les utilisateurs ne peuvent pas ajouter de dossiers non pris en charge par les utilisateurs dans la boîte de dialogue gestion de la bibliothèque Windows. Si des dossiers distants non indexés sont ajoutés à une bibliothèque à l’aide de l’API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) , l’expérience utilisateur de la bibliothèque repassera en **mode sans échec** de la bibliothèque. En **mode sans échec** , les fonctionnalités telles que les vues d’organisation de pile basées sur les propriétés, les suggestions de filtre et la prise en charge de la recherche de **menu Démarrer** sont supprimées de la bibliothèque affectée.

Le tableau suivant répertorie les dossiers inclus dans les bibliothèques à l’aide de la boîte de dialogue gestion de la bibliothèque de l’Explorateur Windows, et les dossiers qui ne sont pas pris en charge en **mode sans échec**:

| Dossiers pris en charge                                                                                                                            | Dossiers non pris en charge                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Disques durs NTFS et NTFS fixes et externes                                                                                                | Lecteurs amovibles (tels que les cartes thumbdrives et SD)                                                     |
| Les partages qui sont indexés par la recherche Windows (tels que les serveurs départementaux et sur les ordinateurs exécutant Windows 10 et Windows 7 édition familial) | Support amovible (par exemple, CDs et DVD)                                                                  |
| Partages disponibles hors connexion (par exemple, **Mes documents redirigés**, **cache côté client**)                                               | Partages réseau qui ne sont pas disponibles hors connexion ni indexés à distance (tels que les lecteurs NAS)             |
| n/a                                                                                                                                          | Autres sources de données (telles que Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive, etc.) |

### <a name="storage-backed"></a>Storage-Backed

Les bibliothèques sont des collections de dossiers de stockage. Les utilisateurs peuvent enregistrer et copier des fichiers directement dans une bibliothèque, puisque chaque bibliothèque a un emplacement d’enregistrement par défaut auquel envoyer ces fichiers. Pour les bibliothèques par défaut, il s’agit d’un dossier connu de l’utilisateur qui est inclus dans une bibliothèque (par exemple, **Mes documents**) ou du premier dossier ajouté à une bibliothèque personnalisée. Il s’agit du dossier dans lequel les fichiers sont placés lorsqu’un utilisateur fait glisser des fichiers dans une bibliothèque ou les enregistre dans une bibliothèque à l’aide de la boîte de dialogue de fichier commune. L’utilisateur peut modifier l’emplacement d’enregistrement par défaut d’une bibliothèque à tout moment, mais si elle supprime l’emplacement d’enregistrement par défaut, le dossier suivant de la bibliothèque est sélectionné comme nouvel emplacement d’enregistrement. En outre, les utilisateurs peuvent enregistrer dans n’importe quel dossier auquel ils ont des autorisations qui ont été inclus dans une bibliothèque.

### <a name="non-file-system-shell-containers"></a>Conteneurs d’interpréteur de commandes de système non-fichier

Les bibliothèques peuvent contenir des conteneurs Shell du système de fichiers, tels que l' **ordinateur** et **le panneau** de configuration, mais ils contiennent des éléments de système de fichiers. Les dossiers et le contenu de la bibliothèque peuvent être énumérés et consultés à l’aide des API pour les fichiers et les dossiers du système de fichiers dans les systèmes d’exploitation précédents. Si votre application dépend fortement des API spécifiques au système de fichiers, l’API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) peut être utilisée pour obtenir les chemins d’accès du système de fichiers des dossiers et des fichiers dans les bibliothèques. Dans la plupart des cas, il est recommandé d’utiliser le modèle de programmation de l’interpréteur de commandes pour prendre en charge plusieurs versions de Windows et la flexibilité des éléments. Pour plus d’informations, consultez [navigation dans l’espace de noms Shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descriptions de la bibliothèque

Les descriptions de bibliothèque sont enregistrées sur le disque sous la forme d’un fichier XML dans le dossier de bibliothèques% AppData% Microsoft \\ Windows \\ (et éventuellement en tant que **\_ bibliothèques FOLDERID**. Pour plus d’informations sur les **\_ bibliothèques FOLDERID**, consultez [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Les fichiers de description de bibliothèque sont des fichiers XML avec l’extension de nom de fichier. Library-ms. Ils ne doivent jamais être consultés ou modifiés par les applications. Le texte du chemin d’accès au dossier persistant dans les fichiers de description de la bibliothèque n’est pas toujours à jour. Les dossiers de bibliothèque sont conservés dans le fichier de description de la bibliothèque au format de [liens de Shell](/windows/desktop/shell/links) binaire sérialisé. Pour plus d’informations sur les bibliothèques et le schéma de description de la bibliothèque, consultez [schéma de description](../shell/library-schema-entry.md)de la bibliothèque. Pour plus d’informations sur les connecteurs de recherche fédérée et le schéma de la description du connecteur de recherche, [recherchez schéma de description du connecteur](search-sconn-desc-schema-entry.md).

> [REMARQUE]  
> Les applications doivent toujours utiliser le modèle de programmation de l’interpréteur de commandes ou l’API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pour consommer et manipuler le contenu de la bibliothèque et ne jamais tenter d’accéder ou de modifier manuellement le fichier de description de la bibliothèque.

## <a name="related-topics"></a>Rubriques connexes

[Recherche Windows 7](./-search-3x-wds-overview.md)

[Nouvelle recherche pour Windows 7](new-for-windows-7-search.md)

[Indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7](indexing-prioritization-and-rowset-events.md)