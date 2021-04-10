---
description: Décrit comment créer un fichier de description OpenSearch (. fichier osdx) pour connecter des magasins de données externes au client Windows via le protocole OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Création d’un fichier de description OpenSearch dans Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951032"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Création d’un fichier de description OpenSearch dans Windows Federated Search

Décrit comment créer un fichier de description OpenSearch (. fichier osdx) pour connecter des magasins de données externes au client Windows via le protocole [OpenSearch](https://github.com/dewitt/opensearch) . La recherche fédérée permet aux utilisateurs de rechercher dans un magasin de données distant et d’afficher les résultats à partir de l’Explorateur Windows.

Cette rubrique contient les sections suivantes :

-   [Fichier de description OpenSearch](#opensearch-description-file)
    -   [Minimale les éléments enfants requis](#mininum-required-child-elements)
-   [Éléments standard dans Windows Federated Search](#standard-elements-in-windows-federated-search)
    -   [Nom court](#shortname)
    -   [Description](#description)
    -   [Modèle d’URL pour les résultats RSS/Atom](#url-template-for-rssatom-results)
    -   [Modèle d’URL pour les résultats Web](#url-template-for-web-results)
    -   [Paramètres de modèle d’URL](#url-template-parameters)
    -   [Résultats paginés](#paged-results)
    -   [Pagination à l’aide de l’index de l’élément](#paging-using-the-item-index)
    -   [Pagination à l’aide de l’index de page](#paging-using-the-page-index)
    -   [Taille de la page](#page-size)
-   [Éléments étendus dans la recherche fédérée Windows](#extended-elements-in-windows-federated-search)
    -   [Nombre maximal de résultats](#maximum-result-count)
    -   [Mappage de propriétés](#property-mapping)
-   [Versions préliminaires](#previews)
-   [Élément de menu ouvrir l’emplacement du fichier](#open-file-location-menu-item)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="opensearch-description-file"></a>Fichier de description OpenSearch

Un fichier de description OpenSearch (. fichier osdx) pour Windows Federated Search doit respecter les règles suivantes :

-   Être un document de description OpenSearch valide, tel que défini par la spécification [opensearch](https://github.com/dewitt/opensearch) 1,1.
-   Fournissez un modèle d’URL avec un type de format RSS ou Atom.
-   Utilisez l’extension de nom de fichier. fichier osdx ou associez-la à l’extension de nom de fichier. fichier osdx lors du téléchargement à partir du Web. Par exemple, un serveur n’est pas obligé d’utiliser. fichier osdx. Un serveur peut retourner le fichier avec n’importe quelle extension de nom de fichier, par exemple. xml, et traité comme s’il s’agissait d’un fichier. fichier osdx s’il utilise le type MIME correct pour les documents de description OpenSearch (fichiers. fichier osdx).
-   Fournissez une valeur de l’élément **ShortName** (recommandé).

### <a name="mininum-required-child-elements"></a>Minimale les éléments enfants requis

L’exemple de fichier. fichier osdx suivant comprend les éléments **ShortName** et `Url` , qui sont les éléments enfants requis minimaux.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Éléments standard dans Windows Federated Search

Outre les éléments enfants minimaux, la recherche fédérée prend en charge les éléments standard suivants.

### <a name="shortname"></a>Nom court

Windows utilise la valeur de l’élément **ShortName** pour nommer le fichier. searchconnector-ms (connecteur de recherche) qui est créé lorsque l’utilisateur ouvre le fichier. fichier osdx. Windows garantit que le nom de fichier généré utilise uniquement les caractères autorisés dans les noms de fichiers Windows. Si aucune valeur **ShortName** n’est fournie, le fichier. searchconnector-MS essaie d’utiliser le nom de fichier du fichier. fichier osdx à la place.

Le code suivant illustre l’utilisation de l’élément **ShortName** dans un fichier. fichier osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Description

Windows utilise la valeur de l’élément **Description** pour renseigner la description du fichier affichée dans le volet Détails de l’Explorateur Windows lorsqu’un utilisateur sélectionne un fichier. searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Modèle d’URL pour les résultats RSS/Atom

Le fichier. fichier osdx doit inclure un élément de **format d’URL** et un attribut de **modèle** (un modèle d’URL) qui retourne les résultats au format RSS ou Atom. L’attribut format doit avoir la valeur `application/rss+xml` pour les résultats au format RSS ou `application/atom+xml` pour les résultats au format Atom, comme indiqué dans le code suivant.

> [!Note]  
> L’élément de **format d’URL** et l’attribut de **modèle** sont communément appelés modèles d’URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Modèle d’URL pour les résultats Web

Si une version des résultats de la recherche peut être affichée dans un navigateur Web, vous devez fournir un attribut **format d’URL =** `text/html` et un attribut de **modèle** , comme indiqué dans le code suivant.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Si vous fournissez un élément **URL format = "text/html"** et un attribut de **modèle** , un bouton apparaît dans la barre de commandes de l’Explorateur Windows, comme illustré dans la capture d’écran suivante, qui permet à l’utilisateur d’ouvrir un navigateur Web pour afficher les résultats de la recherche lorsque l’utilisateur effectue une requête.

![capture d’écran montrant le bouton de restauration de recherche sur le Web.](images/websearchroll-overcommandbarbutton.png)

La restauration de la requête vers l’interface utilisateur Web du magasin de données est importante dans certains scénarios. Par exemple, un utilisateur peut souhaiter afficher plus de 100 résultats (le nombre par défaut d’éléments demandés par le fournisseur OpenSearch). Dans ce cas, l’utilisateur peut également utiliser les fonctionnalités de recherche disponibles uniquement sur le site Web du magasin de données, telles que la nouvelle requête avec un ordre de tri différent, ou le pivotement et le filtrage de la requête avec les métadonnées associées.

### <a name="url-template-parameters"></a>Paramètres de modèle d’URL

Le fournisseur OpenSearch effectue toujours les actions suivantes :

1.  Utilise le modèle d’URL pour envoyer la demande au service Web.
2.  Tente de remplacer les jetons trouvés dans le modèle d’URL avant d’envoyer la requête au service Web, comme suit :
    -   Remplace les jetons OpenSearch standard répertoriés dans le tableau suivant.
    -   Supprime tous les jetons qui ne sont pas répertoriés dans le tableau suivant.



| Jeton pris en charge  | Utilisation par le fournisseur OpenSearch                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Remplacé par les termes de recherche que l’utilisateur tape dans la zone de recherche de l’Explorateur Windows.<br/>                                         |
| startIndex     | Utilisé lors de l’obtention des résultats dans des « pages ».<br/> Remplacé par l’index du premier élément de résultat à retourner.<br/>                        |
| StartPage      | Utilisé lors de l’obtention des résultats dans des « pages ».<br/> Remplacé par le numéro de page de l’ensemble des résultats de recherche à retourner.<br/>               |
| saut          | Utilisé lors de l’obtention des résultats dans des « pages ».<br/> Remplacé par le nombre de résultats de recherche par page demandés par l’Explorateur Windows.<br/> |
| sous       | Remplacé par une chaîne qui indique la langue de la requête en cours d’envoi.<br/>                                                          |
| {inputEncoding}  | Remplacé par une chaîne (telle que « UTF-16 ») qui indique l’encodage de caractères de la requête en cours d’envoi.<br/>                                |
| OutputEncoding | Remplacé par une chaîne (par exemple, « UTF-16 ») qui indique l’encodage de caractères souhaité pour la réponse du service Web.<br/>       |



 

### <a name="paged-results"></a>Résultats paginés

Vous souhaiterez peut-être limiter le nombre de résultats retournés par requête. Vous pouvez choisir de retourner une « page » de résultats à la fois, ou de faire en sorte que le fournisseur OpenSearch récupère des pages supplémentaires de résultats par numéro d’élément ou numéro de page. Par exemple, si vous envoyez vingt résultats par page, la première page que vous envoyez commence à l’index d’élément 1 et à la page 1 ; la deuxième page que vous envoyez commence à l’index d’élément 21 et à la page 2. Vous pouvez définir la façon dont vous souhaitez que le fournisseur OpenSearch demande des éléments à l’aide du `{startItem}` `{startPage}` jeton ou dans le modèle d’URL.

### <a name="paging-using-the-item-index"></a>Pagination à l’aide de l’index de l’élément

Un index d’élément identifie le premier élément de résultat dans une page de résultats. Si vous souhaitez que les clients envoient des requêtes à l’aide d’un index d’élément, vous pouvez utiliser le `{startIndex}` jeton dans votre attribut de **modèle** d’élément **URL** , comme indiqué dans le code suivant.


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) remplace ensuite le jeton dans l’URL par une valeur d’index de départ. La première demande commence par le premier élément, comme illustré dans l’exemple suivant :


```
https://example.com/rss.php?query=frogs&start=1
```



Le fournisseur OpenSearch peut obtenir des éléments supplémentaires en modifiant la `{startIndex}` valeur du paramètre et en émettant une nouvelle requête. Le fournisseur répète ce processus jusqu’à ce qu’il ait obtenu des résultats suffisants pour respecter sa limite, ou qu’il atteigne la fin des résultats. Le fournisseur OpenSearch examine le nombre d’éléments renvoyés par le service Web dans la première page de résultats et définit la taille de page attendue sur ce nombre. Il utilise ce nombre pour incrémenter la `{startIndex}` valeur pour les demandes suivantes. Par exemple, si le service Web retourne 20 résultats dans la première requête, le fournisseur définit la taille de page attendue sur 20. Pour la requête suivante, le fournisseur remplace `{startIndex}` par la valeur 21 pour obtenir les 20 éléments suivants.

> [!Note]  
> Si une page de résultats retournée par le service Web a moins d’éléments que la taille de page attendue, le fournisseur OpenSearch suppose qu’il a reçu la dernière page des résultats et arrête d’effectuer des requêtes.

 

### <a name="paging-using-the-page-index"></a>Pagination à l’aide de l’index de page

Un index de page identifie la page de résultats spécifiée. Si vous souhaitez que les clients envoient des requêtes à l’aide d’un numéro de page, vous pouvez utiliser le `{startPage}` jeton dans votre attribut de **modèle** d’élément de **format d’URL** pour indiquer que, comme illustré dans l’exemple suivant :


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Le fournisseur OpenSearch remplace ensuite le jeton dans l’URL par un paramètre de numéro de page. La première demande commence par la première page, comme illustré dans l’exemple suivant :


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Si une page de résultats retournée par le service Web a moins d’éléments que la taille de page attendue, le fournisseur OpenSearch suppose qu’il a reçu la dernière page des résultats et arrête d’effectuer des requêtes.

 

### <a name="page-size"></a>Taille de la page

Vous pouvez configurer votre service Web pour autoriser une requête à spécifier la taille des pages à l’aide d’un paramètre dans l’URL. Une demande doit être spécifiée dans le fichier. fichier osdx à l’aide du `{count}` jeton, comme suit :


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) peut ensuite définir la taille de page souhaitée, en nombre de résultats par page, comme indiqué dans l’exemple suivant :


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Par défaut, le fournisseur OpenSearch effectue des demandes à l’aide d’une taille de page de 50. Si vous souhaitez une taille de page différente, ne fournissez pas de `{count}` jeton, et placez plutôt le nombre souhaité directement dans l’élément de **modèle d’URL** .

Le fournisseur OpenSearch détermine la taille de la page en fonction du nombre de résultats renvoyés lors de la première requête. Si la première page de résultats reçue a moins d’éléments que le nombre demandé, le fournisseur réinitialise la taille de page pour toutes les demandes de page suivantes. Si les demandes de page suivantes retournent moins d’éléments que le nombre demandé, le fournisseur OpenSearch part du principe qu’il a atteint la fin des résultats.

## <a name="extended-elements-in-windows-federated-search"></a>Éléments étendus dans la recherche fédérée Windows

Outre les éléments standard, la recherche fédérée prend en charge les éléments étendus suivants : **MaximumResultCount** et **ResultsProcessing**.

Étant donné que ces éléments enfants étendus ne sont pas pris en charge dans la spécification [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, ils doivent être ajoutés à l’aide de l’espace de noms suivant :


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Nombre maximal de résultats

Par défaut, les connecteurs de recherche sont limités à 100 résultats par requête utilisateur. Cette limite peut être personnalisée en incluant l’élément **MaximumResultCount** dans le fichier OSD, comme indiqué dans l’exemple suivant :


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



L’exemple précédent déclare le préfixe de l’espace `ms-ose` de noms dans l’élément **OpenSearchDescription** de niveau supérieur, puis l’utilise comme préfixe dans le nom de l’élément. Cette déclaration est obligatoire, car **MaximumResultCount** n’est pas pris en charge dans la spécification de la version 1.1 de [OpenSearch](https://github.com/dewitt/opensearch) .

### <a name="property-mapping"></a>Mappage de propriétés

Lorsque les résultats sont retournés par le service Web sous la forme d’un flux RSS ou Atom, le fournisseur OpenSearch doit mapper les métadonnées de l’élément dans les flux aux propriétés que le shell Windows peut utiliser. La capture d’écran suivante illustre la façon dont le fournisseur OpenSearch mappe certains des éléments RSS par défaut.

![capture d’écran montrant les mappages de propriétés RSS vers Windows-Shell intégrés](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Mappages par défaut

Les mappages par défaut des éléments XML RSS aux propriétés système de l’interpréteur de commandes Windows, sont répertoriés dans le tableau suivant. Les chemins d’accès XML sont relatifs à l’élément item. Le `"media:"` préfixe est défini par l’espace de noms de l' [espace de noms de recherche Yahoo](https://www.rssboard.org/media-rss) .



| Chemin d’accès XML RSS                  | Propriété de l’interpréteur de commandes Windows (nom canonique) |
|-------------------------------|-----------------------------------------|
| Lien                          | System. ItemUrl                          |
| Intitulé                         | System. ItemName                         |
| Auteur                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| Description                   | Résumé système.                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System. MIMEType                         |
| enclosure/@length             | System. Size                             |
| enclosure/@url                | System. ContentUrl                       |
| média : catégorie                | System.Keywords                         |
| media:content/@fileSize       | System. Size                             |
| media:content/@type           | System. MIMEType                         |
| media:content/@url            | System. ContentUrl                       |
| media:group/content/@fileSize | System. Size                             |
| media:group/content/@type     | System. MIMEType                         |
| media:group/content/@url      | System. ContentUrl                       |
| media:thumbnail/@url          | System. ItemThumbnailUrl                 |



 

> [!Note]  
> Outre les mappages par défaut des éléments RSS ou Atom standard, vous pouvez mapper d’autres propriétés système de l’interpréteur de commandes Windows en incluant des éléments XML supplémentaires dans l’espace de noms Windows pour chacune des propriétés. Vous pouvez également mapper des éléments à partir d’autres espaces de noms XML existants tels que MediaRSS, iTunes, etc., en ajoutant un mappage de propriété personnalisée dans le fichier. fichier osdx.

 

### <a name="custom-property-mappings"></a>Mappages de propriétés personnalisées

Vous pouvez personnaliser le mappage des éléments de votre sortie RSS vers les propriétés système de l’interpréteur de commandes Windows en spécifiant le mappage dans le fichier. fichier osdx.

La sortie RSS spécifie :

-   Un espace de noms XML, et
-   Pour tout élément enfant d’un élément, nom d’élément à mapper.

Le fichier. fichier osdx identifie une propriété de l’interpréteur de commandes Windows pour chaque nom d’élément dans un espace de noms. Les mappages de propriétés que vous définissez dans votre fichier. fichier osdx remplacent les mappages par défaut, s’ils existent, pour les propriétés spécifiées.

Le diagramme suivant illustre la façon dont une extension RSS est mappée aux propriétés Windows (nom canonique).

![Diagramme montrant que la combinaison de l’espace de noms XML et du chemin XML produit le nom canonique](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Exemples de résultats RSS et mappage des propriétés OSD

L’exemple de sortie RSS suivant identifie `https://example.com/schema/2009` en tant qu’espace de noms XML avec le préfixe « example ». Ce préfixe doit apparaître à nouveau avant l’élément **e-mail** .


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



Dans l’exemple de fichier. fichier osdx suivant, l’élément **email** XML est mappé à la propriété shell Windows [. contact. EmailAddress](../properties/props-system-contact-emailaddress.md).


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



Certaines propriétés ne peuvent pas être mappées, car leurs valeurs sont remplacées ultérieurement ou ne sont pas modifiables. Par exemple, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) ou [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) ne peuvent pas être mappés, car ils sont calculés à partir de la valeur URL fournie dans les éléments Link ou Enclosure.

### <a name="thumbnails"></a>Miniatures

Les URL d’image miniature peuvent être fournies pour n’importe quel élément à l’aide de l’élément **Media : thumbnail URL = ""** . La résolution idéale est 150 x 150 pixels. Les plus grandes miniatures prises en charge sont 256 x 256 pixels. Le fait de fournir des images de grande taille prend plus de bande passante sans avantage supplémentaire pour l’utilisateur.

### <a name="open-file-location-context-menu"></a>Ouvrir le menu contextuel de l’emplacement du fichier

Windows fournit un menu contextuel nommé **emplacement du fichier ouvert** pour les éléments de résultat. Si l’utilisateur sélectionne un élément dans ce menu, l’URL « parent » pour l’élément sélectionné est ouverte. Si l’URL est une URL Web, par exemple `https://...` , le navigateur Web est ouvert et navigue vers cette URL. Votre flux doit fournir une URL personnalisée pour chaque élément afin de s’assurer que Windows ouvre une URL valide. Pour ce faire, vous pouvez inclure l’URL dans un élément à l’intérieur du code XML de l’élément, comme illustré dans l’exemple suivant :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



Si cette propriété n’est pas définie explicitement dans le XML de l’élément, le fournisseur OpenSearch le définit sur le dossier parent de l’URL de l’élément. Dans l’exemple ci-dessus, le fournisseur OpenSearch utilise la valeur de lien et définit la valeur de la propriété d’environnement Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) sur `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personnaliser les affichages de l’Explorateur Windows avec les listes de description des propriétés

Certaines dispositions de vue de l’Explorateur Windows sont définies par les listes de description des propriétés ou par les exemples de configuration. Un PropList est une liste de propriétés délimitées par des points-virgules, telles que `"prop:System.ItemName; System.Author"` , qui est utilisée pour contrôler l’affichage de vos résultats dans l’Explorateur Windows.

Les zones de l’interface utilisateur de l’Explorateur Windows qui peuvent être personnalisées à l’aide de PropList sont illustrées dans la capture d’écran suivante :

![capture d’écran montrant les zones de l’interface utilisateur de l’Explorateur Windows qui peuvent être personnalisées à l’aide de PropList](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Chaque zone de l’Explorateur Windows est associée à un ensemble de PropList, qui sont eux-mêmes spécifiés en tant que propriétés. Vous pouvez spécifier des proplis personnalisés pour des éléments individuels dans vos jeux de résultats ou pour tous les éléments d’un ensemble de résultats.



| Zone de l’interface utilisateur à personnaliser               | Propriété de l’interpréteur de commandes Windows qui implémente la personnalisation |
|------------------------------------|----------------------------------------------------------|
| Mode d’affichage de contenu (lors de la recherche) | System. PropList. ContentViewModeForSearch                 |
| Mode d’affichage de contenu (lors de la navigation)  | System. PropList. ContentViewModeForBrowse                 |
| Mode d’affichage en mosaïque                     | System. PropList. TileInfo                                 |
| Volet Détails                       | System. PropList. PreviewDetails                           |
| Info-bulle (info-bulle de pointage de l’élément)     | System. PropList. info-bulle                                  |



 

 

**Pour spécifier un PropList unique pour un élément individuel :**

1.  Dans votre sortie RSS, ajoutez un élément personnalisé représentant l’PropList que vous souhaitez personnaliser. Par exemple, l’exemple suivant définit la liste pour le volet d’informations :
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Pour appliquer une propriété à chaque élément dans les résultats de la recherche sans modifier la sortie RSS, spécifiez un PropList dans un élément **MS-ose : PropertyDefaultValues** dans le fichier. fichier osdx, comme indiqué dans l’exemple suivant :

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Disposition du mode d’affichage du contenu des propriétés

La liste des propriétés spécifiées dans **System. PropList. ContentViewModeForSearch** et **System. PropList. ContentViewModeForBrowse** PropList détermine ce qui est affiché en mode d’affichage de contenu. Pour plus d’informations sur les listes de propriétés, consultez [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

Les propriétés sont présentées selon les nombres indiqués dans le modèle de disposition suivant :

![capture d’écran montrant le modèle de disposition par défaut dans l’affichage du contenu](images/propertiesnumberslayoutpattern.png)

Si nous utilisons la liste de propriétés suivante,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



L’affichage suivant s’affiche :

![capture d’écran montrant l’exemple de disposition des propriétés.](images/samplepropertylayout.png)

> [!Note]  
> Pour une meilleure lisibilité, les propriétés affichées dans la colonne la plus à droite doivent être étiquetées.

 

### <a name="property-list-flags"></a>Indicateurs de liste de propriétés

Seul l’un des indicateurs définis dans la documentation de PropList s’applique à l’affichage des éléments en mode d’affichage de contenu : ` "~"` . Dans les exemples précédents, la vue de l’Explorateur Windows étiquette certaines des propriétés, telles que `Tags: animals; zoo; lion` . C’est le comportement par défaut lorsque vous spécifiez une propriété dans la liste. Par exemple, le PropList `"System.Author"` est affiché sous la forme `"Authors: value"` . Lorsque vous souhaitez masquer l’étiquette de la propriété, placez un `"~"` devant le nom de la propriété. Par exemple, si PropList a la `"~System.Size"` valeur, la propriété est affichée comme une seule valeur, sans l’étiquette.

## <a name="previews"></a>Versions préliminaires

Lorsque l’utilisateur sélectionne un élément de résultat dans l’Explorateur Windows et que le volet de visualisation est ouvert, le contenu de l’élément est aperçu.

Le contenu à afficher dans l’aperçu est spécifié par une URL, qui est déterminée comme suit :

1.  Si la propriété de l’interpréteur de commandes Windows **System. WebPreviewUrl** est définie pour l’élément, utilisez cette URL.
    > [!Note]  
    > La propriété doit être fournie dans le RSS à l’aide de l’espace de noms du shell Windows ou mappée explicitement dans le fichier. fichier osdx.

     

2.  Si ce n’est pas le cas, utilisez l’URL du lien à la place.

L’organigramme suivant illustre cette logique.

![Organigramme illustrant la manière dont l’Explorateur Windows sélectionne l’URL à utiliser pour les aperçus](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

Il est possible d’utiliser une URL différente pour la version préliminaire que pour l’élément lui-même. Cela signifie que si vous fournissez des URL différentes pour l’URL de lien et le boîtier ou `media:content URL` , l’Explorateur Windows utilise l’URL de lien pour les aperçus de l’élément, mais utilise l’autre URL pour la détection de type de fichier, l’ouverture, le téléchargement, etc.

Comment l’Explorateur Windows détermine l’URL à utiliser :

1.  Si vous fournissez un mappage à [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), l’Explorateur Windows utilise cette URL
2.  Si vous ne fournissez pas de mappage, l’Explorateur Windows indique si les URL de lien et de boîtier sont différentes. Dans ce cas, l’Explorateur Windows utilise l’URL du lien.
3.  Si les URL sont identiques ou s’il existe uniquement une URL de lien, l’Explorateur Windows analyse le lien pour rechercher le conteneur parent en supprimant le nom de fichier de l’URL complète.
    > [!Note]  
    > Si vous reconnaissez que l’analyse d’URL entraînerait des liens inactifs pour votre service, vous devez fournir un mappage explicite pour la propriété.

     

## <a name="open-file-location-menu-item"></a>Élément de menu ouvrir l’emplacement du fichier

Quand vous cliquez avec le bouton droit sur un élément, la commande de menu **ouvrir l’emplacement du fichier** s’affiche. Cette commande dirige l’utilisateur vers le conteneur ou l’emplacement de cet élément. Par exemple, dans une recherche SharePoint, si vous sélectionnez cette option pour un fichier dans une bibliothèque de documents, la racine de la bibliothèque de documents s’ouvre dans le navigateur Web.

Lorsqu’un utilisateur clique sur **ouvrir l’emplacement du fichier**, l’Explorateur Windows tente de trouver un conteneur parent, à l’aide de la logique illustrée dans l’organigramme suivant :

![Organigramme illustrant comment l’Explorateur Windows identifie un conteneur parent](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Meilleures pratiques suivantes dans Windows Federated Search](-search-fedsearch-best.md)
</dt> <dt>

[Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
