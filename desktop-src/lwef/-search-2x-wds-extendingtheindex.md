---
title: extension de l’Index (fonctionnalités héritées de l’environnement Windows)
description: découvrez comment étendre l’index dans Windows Desktop Search 2. x. pour les versions de Windows ultérieures à Windows XP et Windows Server 2003, utilisez Windows Search à la place.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73bbf1ab143bcac581a59467e7a3813511e7b20204434ee5ae7dd7d8893b636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480921"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>extension de l’Index (fonctionnalités héritées de l’environnement Windows)

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

l’utilisation de et du développement pour les versions 2. x de Microsoft Windows Desktop Search (WDS) est fortement déconseillée en faveur de la [recherche Windows](../search/-search-3x-wds-overview.md).

WDS peut être étendu pour indexer le contenu de nouveaux types de fichiers et de nouveaux magasins de données. Actuellement, WDS 2. x contient des filtres pour plus de 200 types d’éléments (y compris des éléments en texte brut tels que des fichiers HTML, XML et de code source) et utilise la même technologie [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)et le même gestionnaire de protocole que SharePoint Services. Si vous avez déjà installé des implémentations de filtre pour vos nouveaux types de fichiers, WDS peut utiliser les interfaces de filtre existantes pour indexer ces données.

Les compléments WDS 2. x permettent à l’index de traverser et d’analyser les nouvelles données et structures de données pour les informations à ajouter au catalogue pouvant faire l’objet d’une recherche. ces compléments peuvent également étendre l’interpréteur de commandes Windows pour associer des icônes et des gestionnaires de menus contextuels aux nouveaux types de fichiers et banques de données. Pour inclure de nouveaux types de fichiers dans le catalogue WDS, un complément doit implémenter l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter). Pour inclure de nouveaux magasins de données, un complément doit être un gestionnaire de protocole. Si le nouveau magasin de données comprend des fichiers incorporés ou de nouveaux types de fichiers, vous devrez également écrire un filtre approprié.

> [!Note]
>
> Les filtres et les gestionnaires de protocole doivent être écrits en code natif en raison de problèmes potentiels de contrôle de version CLR avec le processus dans lequel tous les compléments s’exécutent.

 

## <a name="adding-file-types-to-the-index"></a>Ajout de types de fichiers à l’index

Les compléments peuvent étendre WDS pour indexer les types de fichiers nouveaux ou propriétaires et associer chaque nouveau type de fichier à une icône ou un menu contextuel propre au fichier. Pour ce faire, vous pouvez créer et inscrire un complément qui :

1.  Implémente une interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour chaque type de fichier afin que WDS puisse accéder et indexer le texte et les métadonnées du type de fichier.
2.  Implémente les interfaces **IExtractIcon** et **IContextMenu** pour ajouter des icônes et des menus contextuels pour une intégration et une convivialité supérieures.

Pour plus d’informations sur l’implémentation des filtres, consultez [développement de compléments IFilter](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Ajout de magasins de données à l’index

Les compléments peuvent étendre WDS pour indexer de nouveaux magasins de données et associer des fichiers à une icône ou un menu contextuel propre à un fichier. Pour ce faire, vous pouvez créer et inscrire un gestionnaire de protocole qui :

1.  Implémente les interfaces **ISearchProtocol** et **IUrlAccessor** pour traiter et lier des éléments individuels dans la source de contenu. WDS utilise des URL pour identifier de manière unique les éléments, que ces éléments se trouvent dans le système de fichiers, à l’intérieur d’un magasin de base de données ou sur le Web.
2.  Implémente l’interface **IPersistFolder** et des parties de l’interface **IShellFolder** pour ajouter des icônes et des menus contextuels pour une intégration et une convivialité supérieures.

Pour plus d’informations sur l’implémentation de gestionnaires de protocole, consultez [développement de gestionnaires de protocole](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Instructions du programme d’installation du complément

L’installation d’un complément doit suivre les instructions suivantes :

-   Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.
-   Des notes de publication doivent être fournies.
-   Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.
-   Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.
-   Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.
-   Si un complément plus récent a remplacé le complément précédent, il devrait y avoir la possibilité de restaurer les fonctionnalités du complément précédent et de le faire en tant que complément par défaut pour ce type de fichier ou en magasin.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Développement de compléments IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-2x-wds-phaddins.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**Filtres**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
