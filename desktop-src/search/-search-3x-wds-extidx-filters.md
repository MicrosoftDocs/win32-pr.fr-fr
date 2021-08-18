---
description: découvrez les meilleures pratiques pour la création de gestionnaires de filtres dans Windows recherche. La recherche utilise des filtres pour extraire les éléments à inclure dans un index de recherche en texte intégral.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: meilleures pratiques pour les gestionnaires de filtres dans Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8320cf0f85bf86f7d61df09437271af67d0e4096fc3a917d037914854c9bad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463698"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search

Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral. vous pouvez étendre Windows recherche pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des gestionnaires de filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers. Les filtres sont associés à des types de fichiers, tels qu’ils sont dénotés par des extensions de nom de fichier, des types MIME ou des identificateurs de classe (CLSID). Alors qu’un filtre peut gérer plusieurs types de fichiers, chaque type fonctionne avec un seul filtre.

Cette rubrique contient les sections suivantes :

-   [Code natif](#native-code)
-   [pratiques de Code sécurisé pour la recherche de Windows](#secure-code-practices-for-windows-search)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="native-code"></a>Code natif

dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement. Les filtres doivent être écrits en code natif en raison des éventuels problèmes de versioning du CLR avec le processus dans lequel plusieurs compléments s’exécutent.

## <a name="secure-code-practices-for-windows-search"></a>pratiques de Code sécurisé pour la recherche de Windows

voici quelques pratiques pour écrire des applications sécurisées pour une utilisation avec Windows Search.

**Pour les applications de requête :**

-   Lorsque vous écrivez des clients de recherche, vous devez choisir l’API qui s’exécute dans un contexte de sécurité qui permet à l’utilisateur de disposer des privilèges minimum. Par exemple, les pages ASP peuvent utiliser l’objet de requête IXSSO, qui s’exécute en tant que processus utilisateur.

**Pour les IFilters et les ressources de langue :**

-   Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé. Il n’existe aucun mécanisme pour la chaîne de filtres. Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.
-   les IFilters, les analyseurs lexicaux et les générateurs de formes dérivées pour Windows recherche s’exécutent dans le contexte de sécurité Local. Elles doivent être écrites pour gérer les mémoires tampons et les empiler correctement. Toutes les copies de chaînes doivent avoir des vérifications explicites pour se protéger contre les dépassements de mémoire tampon. Vous devez toujours vérifier la taille allouée de la mémoire tampon et tester la taille des données en fonction de la taille de la mémoire tampon. Les dépassements de mémoire tampon sont une technique courante pour exploiter du code qui n’applique pas les restrictions de taille de mémoire tampon.
-   Les composants [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), analyseur lexical et générateur de formes dérivées ne doivent jamais appeler la fonction de [fonction EXITPROCESS](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou une API similaire qui termine un processus et tous ses threads.
-   N’allouez pas ou ne libérez pas de ressources dans le point d’entrée DllMain. Cela peut entraîner des échecs lors des tests de contrainte de faible ressource.
-   Coder tous les objets pour qu’ils soient thread-safe. Windows La recherche appelle une instance d’analyseur lexical ou de générateur de formes dérivées dans un thread à la fois, mais elle peut appeler plusieurs instances en même temps sur plusieurs threads.
-   Évitez de créer des fichiers temporaires ou d’écrire dans le registre.
-   si vous utilisez le compilateur Microsoft Visual C++, veillez à compiler votre application à l’aide de l’option **/gs** . L’option **/GS** est utilisée pour détecter les dépassements de mémoire tampon. L’option/GS place les contrôles de sécurité dans le code compilé. Pour plus d’informations, consultez [fonction DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (vérification de la sécurité de la mémoire tampon) dans la section Options du compilateur Visual C++ du kit de développement Platform SDK.

## <a name="additional-resources"></a>Ressources supplémentaires

-   L’exemple [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) montre comment créer une classe de base IFilter pour implémenter l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
-   Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
-   Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
-   Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)
</dt> <dt>

[à propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)
</dt> <dt>

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)
</dt> <dt>

[implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)
</dt> <dt>

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
