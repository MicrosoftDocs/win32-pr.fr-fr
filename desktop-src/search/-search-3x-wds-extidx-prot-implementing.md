---
description: Certaines applications stockent leurs éléments dans des bases de données ou des types de fichiers personnalisés.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Fonctionnement des gestionnaires de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313278"
---
# <a name="understanding-protocol-handlers"></a>Fonctionnement des gestionnaires de protocole

Certaines applications stockent leurs éléments dans des bases de données ou des types de fichiers personnalisés. si Windows recherche peut indexer le nom et les propriétés du fichier, Windows n’a aucune connaissance du contenu du fichier. par conséquent, ces éléments ne peuvent pas être indexés ou exposés dans le Shell Windows. En créant un gestionnaire de protocole, vous pouvez rendre ces éléments disponibles pour l’indexation. Vous pouvez également indexer un format de fichier composé, tel qu’un fichier .zip.

Cette rubrique est organisée comme suit :

-   [Indexation des magasins de données à l’aide de gestionnaires de protocole](#indexing-data-stores-with-protocol-handlers)
    -   [Magasins de données Shell](#shell-data-stores)
    -   [Gestionnaires de protocoles](#protocol-handlers)
    -   [Filtres et gestionnaires de protocole](#filters-and-protocol-handlers)
-   [Indexation d’un format de fichier composé](#indexing-a-compound-file-format)
-   [Rubriques connexes](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexation des magasins de données à l’aide de gestionnaires de protocole

lorsque les utilisateurs doivent effectuer des recherches dans les bases de données héritées, les magasins de courrier électronique ou d’autres structures de données qui ne sont pas prises en charge par Windows recherche, vous devez d’abord déterminer si un gestionnaire de protocole existe déjà pour ce magasin de données, peut-être pour une utilisation avec une autre application telle que SharePoint Server. Dans ce cas, vous pouvez installer ce gestionnaire de protocole sur le système. Windows les gestionnaires de protocoles de recherche utilisent des spécifications de conception similaires à SharePoint Server et peuvent souvent être utilisés de manière interchangeable.

pour plus d’informations sur le déploiement du serveur de recherche 2008 avec Office SharePoint server 2007, consultez recherche [fédérée search \[ server \] 2008](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Magasins de données Shell

pour qu’un développeur tiers de nouveaux formats de fichier et de magasins de données puisse faire apparaître ces formats et magasins dans les résultats de la requête dans Windows Explorer, le développeur doit implémenter une source de données Shell. Une source de données Shell est un composant qui est utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données. Un magasin de données est un référentiel de données. Un magasin de données peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur qui utilise une source de données Shell. les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole. Le gestionnaire de protocole implémente le protocole d’accès à une source de contenu dans son format natif. Les interfaces [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) et [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) permettent d’implémenter un gestionnaire de protocole personnalisé pour développer les sources de données qui peuvent être indexées.

si vous souhaitez que les résultats de la requête s’affichent dans l’explorateur de Windows, vous devez implémenter une source de données Shell avant de pouvoir créer un gestionnaire de protocole pour étendre l’index. Toutefois, si toutes les requêtes sont par programmation (par exemple OLE DB) et interprétées par le code de l’application plutôt que par l’interpréteur de commandes, un espace de noms de Shell, alors que préféré n’est pas strictement requis.

> [!Note]  
> Une source de données Shell est parfois appelée extension d’espace de noms Shell. Un gestionnaire est parfois appelé extension d’interpréteur de commandes ou gestionnaire d’extensions de Shell.

 

si vous souhaitez que les utilisateurs affichent leurs résultats de recherche dans Windows Explorer, vous devez créer un gestionnaire de protocole et un ou plusieurs des compléments suivants :

-   Gestionnaire de menu contextuel
-   Gestionnaire d’icône
-   Tout autre type de gestionnaire de fichiers

pour obtenir la liste des gestionnaires identifiés par le scénario de développement que vous essayez d’atteindre, consultez « vue d’ensemble des gestionnaires » dans [Windows la recherche en tant que plateforme de développement](-search-3x-wds-development-ovr.md). Pour plus d’informations sur la création de gestionnaires, consultez [inscription d’extensions de Shell](../shell/reg-shell-exts.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))et [gestionnaires de types de fichiers](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Gestionnaires de protocoles

Si le magasin de données est également un conteneur (tel qu’un dossier de système de fichiers), vous devez implémenter un filtre pour énumérer les URL dans le conteneur. si le magasin de données contient des données ou des types de fichier autres que l’un des types de fichiers 200 pris en charge par Windows Search, vous devez implémenter un filtre pour accéder au contenu des éléments du magasin et l’indexer. Windows la recherche utilise un gestionnaire de protocole et une technologie [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) similaires à celles utilisées par SharePoint Server. si vous avez déjà des filtres pour un magasin et un type de fichier spécifiques installés sur le système en cours d’indexation, Windows recherche peut être en mesure d’utiliser les interfaces existantes pour indexer ces données.

Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md). Pour obtenir des informations conceptuelles sur les gestionnaires de filtres, consultez [développement de gestionnaires de filtres](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filtres et gestionnaires de protocole

les gestionnaires de protocole accordent à l’indexeur de recherche Windows l’accès aux magasins de données, ce qui permet à l’indexeur d’analyser les nœuds d’un magasin de données et d’extraire les informations pertinentes vers l’index. Windows par exemple, la recherche est fournie avec des gestionnaires de protocole pour les magasins de système de fichiers et pour certaines versions des deux banques de données Microsoft Outlook. lors de l’indexation Outlook e-mail, le gestionnaire de protocole analyse tous les messages d’un ensemble de Outlook dossiers et extrait des informations de chaque message et pièce jointe. ces informations sont transmises à l’indexeur pour inclusion dans le catalogue de recherche Windows.

Pour obtenir une vue d’ensemble du gestionnaire de catalogues et du gestionnaire de portée d’analyse (CSM), consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indexation d’un format de fichier composé

Un format de fichier composé peut être indexé afin que les éléments individuels du fichier puissent être retournés en tant que résultats individuels. Un format de fichier composé, tel qu’un fichier compressé avec une extension de nom de fichier .zip, est essentiellement un magasin de données et peut être traité comme tel à des fins d’indexation. L’exemple suivant affiche un fichier .zip dans l’espace de noms du système de fichiers (FILE://c:/test/test.zip) dans lequel se trouvent à la fois des sous-dossiers et des éléments individuels.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

Le gestionnaire de protocole de fichier Découvre quand FILE://c:/test/test.zip change en surveillant les journaux de modification du système de fichiers, et il appelle un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) inscrit pour .zip fichiers de ce fichier lorsque le fichier est modifié, mais il n’a aucune connaissance de la structure interne du fichier .zip lui-même.

Vous devez informer l’indexeur que le format de fichier composé est un magasin de données. Cela est nécessaire pour que les éléments individuels soient indexés et récupérés en tant qu’entités uniques. Une fois que vous avez implémenté une source de données Shell et effectué les étapes suivantes, vous disposerez d’un gestionnaire de protocole capable de traiter et d’exposer les données à partir d’un format de fichier composé (fichier .zip) en tant qu’éléments individuels.

**Pour informer l’indexeur qu’un fichier composé est un magasin de données :**

1.  Créez un gestionnaire de protocole (à l’aide de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) ou [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) pour les fichiers .zip qui ont la possibilité d’établir une liaison avec le fichier source. Pour plus d’informations, consultez [installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md).

    Par exemple, vous pouvez utiliser un chemin d’échappement vers le fichier .zip comme nom de dossier racine, puis utiliser une syntaxe de hiérarchie comme tout autre format de fichier.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    À l’aide des exemples de données ci-dessus pour c : \\ test \\test.zip, les URL uniques sont les suivantes. Avec ces URL, le gestionnaire de protocole a les informations nécessaires pour établir une liaison avec le fichier .zip et énumérer les URL enfants, y compris les fichiers internes, afin qu’ils puissent être liés et indexés par le .doc et les filtres de .txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Assurez-vous que votre gestionnaire de protocole respecte les deux conditions suivantes :
    -   Les URL racines d’un fichier .zip doivent émettre une \_ recherche de \_ IsClosedDirectory ([System. Search. IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) sur les URL qui sont les url de fichier racine .zip. Par exemple, .zip:///FILE :% 2F% 2F% 2fc :% 2Ftest% 2ftest.zip/doit émettre IsClosedDirectory = **true**. Cela indique à l’indexeur que si la date sur cette URL n’a pas changé, il n’est pas nécessaire de traiter les URL enfants.
    -   Chaque URL enfant pour cette URL doit émettre une \_ recherche de \_ IsFullyContained ([System. Search. IsFullyContained](../properties/props-system-search-isfullycontained.md)) sur les URL enfants de l’URL de .zip racine. Normalement à la fin d’une analyse incrémentielle, l’indexeur traite toutes les URL non visitées comme des éléments qui doivent être supprimés. Toutefois, le fichier de .zip racine ne doit pas traiter les URL racine, car rien n’a changé. L’émission de cette propriété avec la **valeur true** indique à l’indexeur que si cette URL n’a pas été traitée à la fin d’une analyse incrémentielle, elle ne doit pas être supprimée. Elle sera supprimée uniquement si l’élément racine a été modifié et qu’il n’est pas visité.

Windows La recherche nécessite une page de démarrage pour un protocole afin de savoir quelles URL analyser de façon incrémentielle et quelles URL doivent être ignorées lorsqu’elles sont trouvées. Toutefois, nous ne pouvons pas démarrer avec une URL pour chaque fichier .zip, car nous ne savons pas où se trouve chaque fichier .zip. Par conséquent, l’URL de la page de démarrage du gestionnaire de protocole .zip doit être en mesure d’énumérer tout ce qui se trouve à la racine des chemins d’échappement de tous les fichiers de .zip. Ces fichiers .zip ne sont pas nécessairement dans le fichier : namespace et peuvent être une URL de type MAPI qui pointe vers un fichier .zip en tant que pièce jointe, par exemple.

**Pour inscrire une racine comme page de démarrage :**

1.  Inscrivez une racine telle que .zip:///comme page de démarrage afin que tous les fichiers .zip démarrent ici, en vigueur. lors du traitement de la racine .zip : URL, votre gestionnaire de protocole doit générer la liste des url enfants à émettre en interrogeant Windows rechercher toutes les url avec System. FileExtension = ".zip".
2.  Échapper ces URL pour supprimer les barres obliques et les retourner en tant qu’URL enfants. Voici un exemple de requête pour récupérer les types souhaités.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  lorsque Windows recherche effectue périodiquement une analyse incrémentielle sur votre URL racine .zip:///, vous devez refléter la liste des url que Windows recherche est déjà en cours de gestion qui sont des url .zip. Si une suppression est détectée dans le magasin natif où le fichier .zip est stocké, elle n’apparaît pas dans votre énumération, et cette branche de l’arborescence dans le .zip est supprimée.
4.  Pour créer une liaison avec les données de .zip pour un autre gestionnaire de protocole, vous devez idéalement parcourir le [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) pour cette URL afin de lier le stockage de l’objet et ne pas supposer qu’il s’agit toujours d’un fichier. Cela vous permet de travailler avec des pièces jointes dans des magasins de courrier électronique, par exemple.
5.  Lors de l’émission d’URL enfants pour chaque fichier de .zip, vous devez utiliser \_ la recherche de \_ UrlToIndexWithModificationTime ([System. Search. UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) pour transmettre la valeur \_ de la valeur de la valeur de la valeur de la file d' .zip .zip[](../properties/props-system-datemodified.md).

Pour que vos URL .zip indexées immédiatement après leur création ou leur modification, et qu’il n’est pas nécessaire d’attendre qu’une analyse incrémentielle Découvre leur nouvel État, vous pouvez surveiller le système de fichiers vous-même pour les modifications de fichiers .zip. Toutefois, une telle approche ne fonctionnerait pas pour d’autres magasins de données tels que MAPI.

**Pour que vos URL .zip indexées lorsqu’elles sont créées ou modifiées :**

1.  Créez un filtre (et l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) pour le type de fichier .zip. pour plus d’informations, consultez [développement de gestionnaires de propriétés pour la recherche de Windows](-search-3x-wds-extidx-propertyhandlers.md).
2.  Chaque fois que votre implémentation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est appelée, cela est dû au fait que l’URL a été découverte ou modifiée. Ensuite, générez un événement pour la .zip URL appropriée pour l’URL source, via l’interface [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) . Cela vous donne la possibilité d’indiquer immédiatement à l’indexeur qu’il existe de nouvelles données à indexer sans devoir attendre l’analyse incrémentielle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Ajout d’icônes et de menus contextuels](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Création d’un connecteur de recherche pour un gestionnaire de protocole](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
