---
description: Microsoft fournit plusieurs filtres standard avec Windows Search. Les clients appellent ces gestionnaires de filtres (qui sont des implémentations de l’interface IFilter) pour extraire du texte et des propriétés d’un document.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Gestionnaires de filtres fournis avec Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112451"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Gestionnaires de filtres fournis avec Windows

Microsoft fournit plusieurs filtres standard avec Windows Search. Les clients appellent ces gestionnaires de filtres (qui sont des implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) pour extraire du texte et des propriétés d’un document.

Cette rubrique est organisée comme suit :

- [Remarques sur l’implémentation de Windows Search](#windows-search-implementation-notes)
  - [Implémentation de Windows 7 et 10](#windows-7-and-10-implementation)
  - [Implémentation de Windows Vista](#windows-vista-implementation)
  - [Implémentation héritée](#legacy-implementation)
- [Filtres de recherche Windows](#filter-handlers-that-ship-with-windows)
  - [Gestionnaire de filtre MIME](#mime-filter-handler)
  - [Gestionnaire de filtre HTML](#html-filter-handler)
  - [Gestionnaire de filtre de document](#document-filter-handler)
  - [Gestionnaire de filtre de texte brut](#plain-text-filter-handler)
  - [Gestionnaire de filtres binaire ou null](#binary-or-null-filter-handler)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

## <a name="windows-search-implementation-notes"></a>Remarques sur l’implémentation de Windows Search

Dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement. Les filtres doivent être écrits en code natif en raison des éventuels problèmes de versioning du CLR avec le processus dans lequel plusieurs compléments s’exécutent.

### <a name="windows-7-and-10-implementation"></a>Implémentation de Windows 7 et 10

Dans Windows 7 et versions ultérieures, un nouveau comportement se produit lors de l’inscription d’un gestionnaire de filtres, d’un gestionnaire de propriétés ou d’une nouvelle extension. Lorsqu’un nouveau gestionnaire de propriétés et/ou gestionnaire de filtres est installé, les fichiers avec les extensions correspondantes sont automatiquement réindexés.

Dans Windows 7 et versions ultérieures, nous vous recommandons d’installer un gestionnaire de filtres conjointement avec les gestionnaires de propriétés correspondants, et d’inscrire le gestionnaire de filtres avant le gestionnaire de propriétés. L’inscription du gestionnaire de propriétés lance la réindexation immédiate des fichiers précédemment indexés sans nécessiter un redémarrage, et tire parti des gestionnaires de filtres précédemment enregistrés pour l’indexation du contenu.

Si seul un gestionnaire de filtres est installé sans gestionnaire de propriétés correspondant, la réindexation automatique se produit soit après un redémarrage du service d’indexation, soit par un redémarrage du système.

Pour les indicateurs de description de propriété spécifiques à Windows 7, consultez les rubriques de référence suivantes : [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) et [PROPDESC \_ SEARCHINFO \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Implémentation de Windows Vista

Dans Windows Vista et les versions antérieures, l’installation d’un gestionnaire [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou d’un gestionnaire de propriétés n’initie pas la réindexation des éléments existants, à moins qu’un éditeur de logiciels indépendant (ISV) appelle explicitement une régénération ou une réindexation des URL correspondantes.

Il existe deux différences majeures entre les applications héritées telles que le service d’indexation et les applications plus récentes telles que Windows Search dont vous devez être conscient lors de l’implémentation de filtres :

- Utilisation de l’interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .
- Utilisation de gestionnaires de propriétés.

Tout d’abord, Windows Vista et Windows Search 3,0 et versions ultérieures requièrent que vous utilisiez [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour les raisons suivantes :

- Pour garantir les performances et la compatibilité future.
- Pour renforcer la sécurité. Les filtres implémentés avec [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sont plus sécurisés, car le contexte dans lequel le filtre s’exécute n’a pas besoin des droits pour ouvrir des fichiers sur le disque ou sur le réseau.

Alors que Windows Search utilise uniquement [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), vous pouvez également inclure l' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) et/ou les implémentations d' [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) dans vos filtres à des fins de compatibilité descendante.

La deuxième différence majeure réside dans le fait que Windows Vista et Windows Search 3,0 et versions ultérieures ont un nouveau [système de propriétés](../properties/building-property-handlers.md) qui utilise des gestionnaires de propriétés pour énumérer les propriétés des éléments.

Toutefois, il peut arriver que vous deviez implémenter un filtre qui gère à la fois le contenu et les propriétés afin d’effectuer les opérations suivantes :

- Prennent en charge les implémentations MSSearch héritées.
- Parcourez les liens.
- Conserver les informations de langue.
- Filtrer les éléments incorporés de manière récursive.

Dans ce cas, vous avez besoin d’une implémentation de filtre complète, y compris la méthode [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) pour accéder aux valeurs de propriété.

### <a name="legacy-implementation"></a>Implémentation héritée

Comme indiqué précédemment, Windows Vista et Windows Search incluent un nouveau système de propriétés qui encapsule les propriétés d’un élément qui sont séparées du contenu d’un élément. Ce système de propriétés n’existe pas dans les versions antérieures de Microsoft Windows Desktop Search (WDS) 2. x. Si votre filtre doit prendre en charge d’autres applications comme décrit ci-dessus, il peut être nécessaire de gérer le contenu et les propriétés.

Pour plus d’informations sur le développement d’un filtre compatible, consultez les rubriques suivantes, [IFilter (pour les applications héritées)](/windows/win32/api/filter/nn-filter-ifilter)et [développement de compléments de filtre (pour les applications héritées)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Filtres de recherche Windows

Microsoft fournit plusieurs filtres standard avec Windows Search. Le contenu de la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  est résumé dans le tableau suivant. Le fait de cliquer sur le nom d’un gestionnaire de filtres vous amène à la description de cette implémentation **IFilter** .

| Gestionnaire de filtres                                                  | Fichiers filtrés                              | DLL IFilter  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Gestionnaire de filtre MIME](#mime-filter-handler)                     | MIME (Multipurpose Internet Mail extension) | mimefilt.dll |
| [Gestionnaire de filtre HTML](#html-filter-handler)                     | HTML 3,0 ou version antérieure                         | nlhtml.dll   |
| [Gestionnaire de filtre de document](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Gestionnaire de filtre de texte brut](#plain-text-filter-handler)         | Fichiers texte brut-IFilter par défaut          | query.dll    |
| [Gestionnaire de filtres binaire ou null](#binary-or-null-filter-handler) | Fichiers binaires-IFilter null                 | query.dll    |

### <a name="mime-filter-handler"></a>Gestionnaire de filtre MIME

Le gestionnaire de filtre MIME (en mimefilt.dll) extrait les informations de texte et de propriété des fichiers avec les extensions. eml,. mht et. MHTML.

### <a name="html-filter-handler"></a>Gestionnaire de filtre HTML

Le gestionnaire de filtre HTML (en nlhtml.dll) extrait les informations de texte et de propriété de la classe « HtmlFiles » afin qu’elles puissent être indexées par la recherche Windows. Pour obtenir une description de l’association entre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et le type de fichier, consultez « recherche de la DLL IFilter pour un fichier » dans [inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md).

Vous pouvez utiliser la `META` fonctionnalité tag des documents html pour transmettre des demandes de traitement spéciales au [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)html. `META` les balises se produisent vers le début d’un fichier HTML au sein des `HEAD ... /HEAD` balises, comme illustré dans l’exemple suivant.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Certaines `META` balises HTML sont automatiquement mappées à des valeurs de jeu de propriétés et d’ID de propriété (PID) bien connues afin que les requêtes sur ces propriétés recherchent le contenu mappé. Certains exemples sont répertoriés dans le tableau suivant. Pour obtenir la liste des propriétés système que vous pouvez utiliser pour vos formats de fichier, consultez [propriétés définies par le système pour les formats de fichiers personnalisés](-shell-systemdefinedpropertiesforfileformats.md).

| Exemple de propriété                              | Mappé à                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| Meta Name = "Author" Content = "Ruth"             | Propriété Author dans la propriété informations récapitulatives définie.            |
| Meta Name = "subject" Content = "traitement de texte" | Propriété Subject dans la propriété informations récapitulatives définie.           |
| Meta Name = "Mots clés" Content = "polices, Serif"   | Propriété de mot clé dans la propriété informations récapitulatives définie.           |
| Meta Name = "ms. Category" Content = "fiction"     | Propriété Category dans la propriété informations récapitulatives du document définie. |

Certaines fonctionnalités du [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) HTML sont répertoriées dans le tableau suivant.

[comment]: # (Cette table doit être au format HTML pour que les exemples soient correctement formatés.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tâche</th>
<th>Action</th>
<th>Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Création d’abstractions spéciales à partir de fichiers</td>
<td>Utilisez la <code>META NAME=&quot;DESCRIPTION&quot;...</code> balise pour indiquer au <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> d’utiliser la chaîne qui suit le <code>CONTENT</code> mot clé comme Résumé du document.
<blockquote>
[!Note]<br />
Le processus de filtrage peut générer des abstractions pour chaque fichier filtré, qui est par défaut un ensemble de caractères au début du fichier.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Empêcher le filtrage de fichiers individuels</td>
<td>Ajoutez une <code>meta name</code> balise au fichier.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Définition du code de langue d’un fichier (pour s’assurer que le système choisit les analyseurs lexicaux de langue et les fichiers de mots parasites corrects)</td>
<td>Ajoutez la <code>meta name</code> balise suivante au fichier, où le champ de contenu spécifie le code de langue approprié (soit en caractères, soit en utilisant la valeur de paramètres régionaux).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Gestionnaire de filtre de document

Le gestionnaire de filtre de document (dans offilt.dll) filtre les fichiers pour certaines extensions de documents dans Microsoft Office. Il s’agit notamment des fichiers avec les extensions. doc,. mdb,. ppt et. xlt, par exemple.

### <a name="plain-text-filter-handler"></a>Gestionnaire de filtre de texte brut

Pour les fichiers en texte brut, Windows Search utilise le gestionnaire de filtre de texte, qui filtre les propriétés système (telles que les noms de fichiers) et le contenu d’un fichier. Lorsqu’un type de fichier n’a pas d’association [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) dans le registre, Windows Search indexe uniquement les propriétés de l’interpréteur de commandes pour le fichier. Toutefois, l’utilisateur peut utiliser les **Options avancées** dans les **options d’indexation** du panneau de configuration pour **indexer les propriétés** ou les propriétés d' **index et le contenu des fichiers**.

![capture d’écran montrant la boîte de dialogue Options avancées](images/ifilteradvancedoptions.png)

Si l’utilisateur choisit cette option pour un type de fichier sans [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associé, le gestionnaire de filtre de texte est utilisé pour extraire le contenu du fichier. Le gestionnaire de filtre de texte ne peut pas « comprendre » tout format de document ; lors du filtrage du contenu d’un fichier, il traite le fichier comme une séquence de caractères. Il vérifie la marque d’ordre d’octet Unicode au début du fichier.

### <a name="binary-or-null-filter-handler"></a>Gestionnaire de filtres binaire ou null

Lorsqu’un fichier binaire enregistré est rencontré, le gestionnaire de filtre null est utilisé. Le gestionnaire de filtre null récupère uniquement les propriétés système. Le contenu d’un fichier binaire n’est pas filtré. **Nom de fichier**, **LastWriteTime**, **taille** et **attributs** sont des exemples de propriétés système.

## <a name="additional-resources"></a>Ressources supplémentaires

- L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[À propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)

[Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)

[Implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
