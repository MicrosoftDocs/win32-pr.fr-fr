---
description: Le kit de développement logiciel (SDK) Windows Search fournit un assembly d’interopérabilité pour que vous utilisiez des objets COM (Component Object Model) exposés par Windows Search et d’autres programmes sur les interfaces et les classes utilisant du code managé.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Utilisation de code managé avec Shell Data et Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112491"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Utilisation de code managé avec Shell Data et Windows Search

Le kit de développement logiciel (SDK) Windows Search fournit un assembly d’interopérabilité pour que vous utilisiez des objets COM (Component Object Model) exposés par Windows Search et d’autres programmes sur les interfaces et les classes utilisant du code managé. L’assembly d’interopérabilité est signé numériquement par Microsoft et se trouve dans les [exemples de recherche Windows](-search-samples-ovw.md).

Cette rubrique est organisée comme suit :

-   [Utilisation de l’API Windows CodePack](#using-the-windows-api-codepack)
    -   [Accès aux résultats de l’index](#accessing-index-results)
    -   [Exemple d’application utilisant l’API Windows Codepack](#sample-application-using-the-windows-api-codepack)
-   [Rubriques connexes](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Utilisation de l’API Windows CodePack

Si vous travaillez dans l’environnement Microsoft .NET, utilisez le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) pour obtenir des résultats de recherche, ou simplement parcourir l’espace de noms. Le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) vous fournit une collection d’éléments de Shell qui sont essentiellement des wrappers autour de l' [interface IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)native. Vous pouvez effectuer une itération sur cette collection et obtenir les différentes valeurs de propriété d’une manière similaire à la façon dont vous pouvez énumérer les résultats d’une table à partir d’une requête de base de données (OLE DB) de liaison et d’incorporation d’objets.

L’extrait de code suivant montre comment itérer au sein des éléments de recherche et obtenir les valeurs de propriété pour chacun d’eux.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Accès aux résultats de l’index

Vous pouvez accéder aux résultats de l’index par le biais de OLE DB ou du modèle de données Shell. Les deux approches présentent des avantages et des inconvénients. L’un des avantages est que OLE DB et langage SQL (SQL) sont familiers aux programmeurs de base de données. D’autres avantages sont un meilleur contrôle des performances lors de l’interrogation de l’indexeur, et l’accès à des fonctionnalités supplémentaires telles que la possibilité de localiser rapidement les résultats précédents dans un nouvel ensemble de lignes.

L’avantage du modèle de données Shell est qu’il est abstrait sur différentes sources d’informations, telles que OpenSearch, et permet d’accéder à des fonctionnalités supplémentaires telles que des miniatures et des gestionnaires de propriétés. Le modèle d’objet Shell ne nécessite pas non plus de prise en charge de cas spéciaux pour les résultats autres que les noms de fichiers tels que les éléments de messagerie et les résultats OneNote, ni pour les éléments qui se trouvent dans l’index de l’utilisateur. Notez que dans l’interpréteur de commandes [KNOWNFOLDERID](../shell/knownfolderid.md) est l’étendue du dossier connu pour le contenu indexé local. Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Les sources de données OpenSearch ne sont pas exposées via OLE DB pour la recherche fédérée dans Windows 7 et versions ultérieures. Pour cette raison, nous vous recommandons d’envisager d’écrire un fournisseur LINQ pour l’espace de noms Shell au lieu d’utiliser OLE DB pour accéder aux résultats de l’indexeur. Pour plus d’informations, consultez [procédure pas à pas : création d’un fournisseur LINQ IQueryable](/previous-versions/bb546158(v=vs.140)).

### <a name="sample-application-using-the-windows-api-codepack"></a>Exemple d’application utilisant l’API Windows Codepack

La capture d’écran suivante représente une simulation d’un exemple d’application créé avec le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).

![capture d’écran de l’application de lecteur multimédia montrant les messages électroniques](images/folderid-searchhome.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Interopérabilité interlangage](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
