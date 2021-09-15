---
description: Les gestionnaires de filtres, qui sont des implémentations de l’interface IFilter, recherchent du texte et des propriétés dans les documents.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: fonctionnement des gestionnaires de filtres dans la recherche Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313226"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>fonctionnement des gestionnaires de filtres dans la recherche Windows

Les gestionnaires de filtres, qui sont des implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , recherchent du texte et des propriétés dans les documents. Les gestionnaires de filtres extraient les blocs de texte de ces éléments, en filtrant la mise en forme incorporée et en conservant les informations relatives à la position du texte. Elles extraient également des blocs de valeurs, qui sont des propriétés de document. **IFilter** est la base de la création d’applications de niveau supérieur, telles que les indexeurs de documents et les visionneuses indépendantes des applications.

Cette rubrique est organisée comme suit :

- [À propos de l’interface IFilter](#about-the-ifilter-interface)
  - [Processus d’isolation](#isolation-process)
  - [DLL IFilter](#ifilter-dlls)
  - [Structure IFilter](#ifilter-structure)
  - [Code natif](#native-code)
- [Recherche de l’identificateur de classe IFilter](#finding-the-ifilter-class-identifier)
  - [IFilter :: GetChunk et identificateurs de code de paramètres régionaux](#ifiltergetchunk-and-locale-code-identifiers)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

## <a name="about-the-ifilter-interface"></a>À propos de l’interface IFilter

Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral. vous pouvez étendre Windows recherche pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers.

L’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est conçue pour répondre aux besoins spécifiques des moteurs de recherche en texte intégral. les moteurs de recherche en texte intégral comme Windows recherche appellent les méthodes **IFilter** pour extraire du texte et des informations de propriété et les ajouter à un index. Windows La recherche fractionne les résultats de la méthode [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retournée en mots, les normalise et les enregistre dans un index. S’il est disponible, le moteur de recherche utilise l’identificateur de code de langue (LCID) d’un segment de texte pour effectuer une césure et une normalisation des mots propres à la langue.

Windows La recherche utilise trois fonctions, décrites dans le tableau suivant, pour accéder aux gestionnaires de filtres enregistrés (implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ). Ces fonctions sont particulièrement utiles lors du chargement et de la liaison au gestionnaire de filtres d’un objet incorporé.

| Fonction               | Description                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LoadIFilter            | Obtient un pointeur vers le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) qui est le plus approprié pour le type de contenu spécifié.                                                                                            |
| BindIFilterFromStorage | Obtient un pointeur vers le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) le plus approprié pour le contenu d’un objet d' [interface IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . |
| BindIFilterFromStream  | Obtient un pointeur vers le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) qui est le plus approprié pour un identificateur de classe (CLSID) spécifié récupéré d’une variable de flux.                                                 |

L’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a cinq méthodes, décrites dans le tableau suivant.

| Méthode                                                    | Description                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Initialise une session de filtrage.                                                                                   |
| [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Positionne [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) au début du premier segment ou du prochain bloc et retourne un descripteur. |
| [**IFilter :: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Récupère le texte du bloc actuel.                                                                             |
| [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Récupère les valeurs du bloc actuel.                                                                           |
| [**IFilter :: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Récupère une interface représentant la partie spécifiée de l’objet. Réservé pour un usage futur.                      |

### <a name="isolation-process"></a>Processus d’isolation

Windows La recherche exécute les IFilters dans le contexte de sécurité du système local avec des droits restreints. Dans ce processus d’isolation d’hôte [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , un certain nombre de droits sont supprimés :

- Code restreint
- Tout le monde
- Local
- Interactive
- Utilisateurs authentifiés
- Utilisateurs intégrés
- Identificateur de sécurité (SID) des utilisateurs

La suppression de ces droits signifie que l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) n’a pas accès au système de disque ou au réseau ou à une interface utilisateur ou à une fonction de presse-papiers. En outre, le processus d’isolation s’exécute sous un objet de traitement qui empêche la création de processus enfants et impose une limite de 100 Mo à la plage de travail. le processus d’isolation de l’hôte de l’interface **IFilter** augmente la stabilité de la plateforme d’indexation, en raison de la possibilité d’implémenter des filtres tiers de manière incorrecte.

> [!NOTE]  
> Les gestionnaires de filtres doivent être écrits pour gérer les mémoires tampons et s’empiler correctement. Toutes les copies de chaînes doivent avoir des vérifications explicites pour se protéger contre les dépassements de mémoire tampon. Vous devez toujours vérifier la taille allouée de la mémoire tampon. Vous devez toujours tester la taille des données par rapport à la taille de la mémoire tampon.

### <a name="ifilter-dlls"></a>DLL IFilter

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Les dll implémentent l’interface **IFilter** pour permettre à un client d’extraire des informations de texte et de valeur de propriété à partir d’un type de fichier, d’une classe ou d’un type perçu. le processus de filtrage de recherche Windows **SearchFilterHost.exe** crée une liaison avec le **IFilter** inscrit pour la classe, le type perçu ou l’extension de nom de l’élément.

### <a name="ifilter-structure"></a>Structure IFilter

Chaque [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est un fichier dll qui implémente un serveur COM (Component Object Model) in-process pour fournir les fonctionnalités de filtrage spécifiées. La figure ci-dessous illustre la structure globale d’une dll **IFilter** classique. Un exemple plus complexe peut implémenter plusieurs classes **IFilter** .

![diagramme de la structure d’une DLL IFilter classique](images/ifilter-structure.png)

### <a name="native-code"></a>Code natif

Les filtres doivent être écrits en code natif en raison de problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent. dans Windows 7 et versions ultérieures et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement.

## <a name="finding-the-ifilter-class-identifier"></a>Recherche de l’identificateur de classe IFilter

La classe de la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est inscrite sous la clé de Registre PersistentHandler L’exemple suivant, pour les fichiers HTML, illustre la recherche de la dll **IFilter** pour un document HTML. Cet exemple suit une logique similaire à celle utilisée par le système pour rechercher le **IFilter** associé à un élément.

1. Vérifiez si l’extension pour le type de fichiers que la DLL filtre a un PersistentHandler inscrit sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes. Laissez cette clé `Value1` . Si cette entrée existe déjà, passez à l’étape 4 de cette procédure et utilisez-la `Value1` dans cette clé. Les valeurs sont de type REG \_ sz.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. Sinon, si aucun PersistentHandler n’est inscrit pour l’extension, recherchez le CLSID associé au type de document sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes. Laissez cette clé `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Déterminez si un PersistentHandler est inscrit pour le CLSID. À l’aide `Value2` de déterminé à l’étape 2, recherchez le PersistentHandler pour l' \\ \_ entrée HKEY local \_ machine \\ Software \\ classes \\ CLSID \\ value2. Laissez cette clé `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Déterminez le GUID du gestionnaire persistant [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . À l’aide `Value1` de et de `Value3` , recherchez le GUID du gestionnaire persistant **IFilter** pour le type de document. La valeur sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes \\ CLSID \\ Value1 ou 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> produit le GUID PersistentHandler **IFilter** pour ce type de document. Laissez cette clé `Value4` . Dans cet exemple, le GUID d’interface **IFilter** est 89BCB740-6119-101A-BCB7-00DD010655AF.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> Dans cet exemple, la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour les documents HTML est nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter :: GetChunk et identificateurs de code de paramètres régionaux

Le LCID de texte peut être modifié dans un fichier unique. Par exemple, le texte d’un manuel d’instruction peut alterner entre l’anglais (en-US) et l’espagnol (es), ou le texte peut inclure un mot unique dans une langue autre que la langue principale. Dans les deux cas, votre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) doit commencer un nouveau bloc chaque fois que le LCID change. Étant donné que le LCID est utilisé pour choisir un analyseur lexical approprié, il est très important que vous l’identifiiez correctement. Si le **IFilter** ne peut pas déterminer les paramètres régionaux du texte, il doit retourner un LCID de zéro avec le segment. si vous renvoyez un LCID de zéro, Windows recherche utilise la technologie de détection automatique de langue (diagnostic linux) pour déterminer l’ID de paramètres régionaux du segment. si Windows recherche ne peut pas trouver de correspondance, elle est définie par défaut sur les paramètres régionaux par défaut du système (en appelant la fonction [GetSystemDefaultLocaleName](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) function). Pour plus d’informations, consultez [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**Chunk \_ BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)et [**Stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk).

Si vous contrôlez le format de fichier et qu’il ne contient pas d’informations de paramètres régionaux, vous devez ajouter une fonctionnalité utilisateur pour permettre l’identification des paramètres régionaux appropriés. L’utilisation d’un analyseur lexical incompatible peut entraîner une mauvaise expérience de requête pour l’utilisateur. Pour plus d’informations, consultez [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> Les filtres sont associés à des types de fichiers, tels qu’ils sont dénotés par des extensions de nom de fichier, des types MIME ou des CLSID. Alors qu’un filtre peut gérer plusieurs types de fichiers, chaque type fonctionne avec un seul filtre.

## <a name="additional-resources"></a>Ressources supplémentaires

- l’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), illustre la création d’une classe de base ifilter pour l’implémentation de l’interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
