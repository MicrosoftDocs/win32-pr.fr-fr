---
description: Vous pouvez inscrire une liste de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Inscrire un ensemble de propriétés et un modèle de disposition d’affichage de contenu pour un type de fichier ou un élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a3df2b65f0c977b5898e2fa35a28091052dde508c0d381379303119068ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820499"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Comment inscrire un ensemble de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément

Vous pouvez inscrire une liste de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément. Si votre type de fichier ou élément est également associé à un type, l’inscription de l’affichage de contenu spécifique du type de fichier ou de l’élément remplacera l’inscription de type. Cela peut être utile si les propriétés les plus importantes de cet élément sont différentes de celles d’autres éléments du même type. Si vous n’associez pas votre type de fichier ou élément à un type d’élément ou inscrivez directement l’affichage de contenu, le système utilise les informations d’affichage de contenu par défaut (stockées dans une clé de Registre référencée par le dernier élément dans le tableau d’association de tous les éléments, à savoir la \_ racine des classes HKEY \_ \\ \* )

Avant d’inscrire une liste de propriétés personnalisées pour votre type de fichier, vous devez comprendre le mode de résultat de la recherche et le mode de navigation, ainsi que les modèles de disposition qui sont à votre disposition.

## <a name="instructions"></a>Instructions

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Étape 1 : comprendre le mode de résultat de la recherche et le mode de navigation

L’affichage du contenu nécessite de définir un modèle de disposition et un ensemble de listes de propriétés pour un élément dans un jeu de résultats de recherche (mode de résultat de la recherche), et lorsque vous accédez à un emplacement de Shell (mode de navigation). Vous pouvez utiliser les mêmes valeurs pour les résultats de recherche et parcourir, comme `Kind.Music` c’est le cas. Vous pouvez également définir une liste de propriétés et/ou un modèle de disposition différent `Kind.Document` .

Dans le cas de `Kind.Document` , les utilisateurs recherchent souvent des mots dans le texte du document. Par conséquent, l’ajout d’un plus grand nombre d’exemples de texte dans les résultats de la recherche peut être le meilleur choix. L’exemple suivant illustre l’affichage parcourir le contenu de `Kind.Document` .

![Parcourir l’affichage du contenu de kind.document](images/content-view/browsecontentviewkinddocument.png)

Étant donné que les utilisateurs recherchent rarement du texte particulier lors de la recherche de documents, l’optimisation de votre choix de propriétés et de la mise en page pour s’adapter à d’autres résultats de recherche sur l’écran peut être le meilleur choix. La capture d’écran suivante illustre l’affichage du contenu de recherche de `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Étape 2 : présentation des modèles de disposition

Il existe quatre modèles de disposition : alpha, bêta, gamma et Delta.

**Disposition alpha**

Le modèle de disposition alpha est optimisé pour les résultats de recherche de documents qui contiennent des extraits. Il présente les spécifications suivantes :

-   Lignes : 4
-   Propriétés : 7
-   Disposition alpha lorsque l’élément a 350 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.

    ![modèle de disposition alpha](images/content-view/layout1.png)

-   L’illustration suivante montre la disposition alpha lorsque l’élément a 350 pixels ou plus d’espace horizontal.

    ![Diagramme illustrant un exemple de disposition alpha](images/content-view/alphaviewmore.png)

-   L’illustration suivante montre la disposition alpha lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![Capture d’écran montrant un exemple de disposition alpha dans Microsoft Word.](images/content-view/layout2.png)

-   L’illustration suivante montre la disposition alpha lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![exemple de disposition alpha](images/content-view/alphaviewless.png)

**Disposition bêta**

Le modèle de disposition bêta est optimisé pour les résultats de recherche de documents de courrier électronique qui contiennent des extraits. Il présente les spécifications suivantes :

-   Lignes : 4
-   Propriétés : 5
-   Disposition bêta lorsque l’élément a 350 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.

    ![Diagramme qui montre un exemple de disposition bêta.](images/content-view/layout3.png)

-   L’illustration suivante montre la disposition de la version bêta lorsque l’élément a 350 pixels ou plus d’espace horizontal.

    ![Capture d’écran montrant un exemple de disposition bêta pour le courrier électronique.](images/content-view/betaviewmore.png)

-   L’illustration suivante montre la disposition de la version bêta lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![Diagramme qui montre un exemple de disposition bêta avec moins de 350 pixels d’espace horizontal.](images/content-view/layout4.png)

-   L’illustration suivante montre la disposition de la version bêta lorsque l’élément a moins de 350 pixels d’espace horizontal :

    ![exemple de disposition bêta](images/content-view/betaviewless.png)

**Disposition gamma**

Le modèle de disposition gamma est semblable à alpha, mais utilise une disposition à deux lignes au lieu de quatre. Cette disposition est idéale pour les scénarios dans lesquels vous souhaitez afficher un extrait de code, mais vous souhaitez afficher plus d’éléments à l’écran, ou pour les types de fichiers qui nécessitent moins d’espace pour afficher les informations les plus critiques. La disposition gamma présente les spécifications suivantes :

-   Lignes : 2
-   Propriétés : 4
-   L’illustration suivante montre la disposition gamma lorsque l’élément a 350 pixels ou plus d’espace horizontal.

    ![Diagramme qui montre un exemple de disposition gamma.](images/content-view/layout5.png)

-   L’illustration suivante montre la disposition gamma lorsque l’élément a 350 pixels ou plus d’espace horizontal.

    ![Capture d’écran montrant un exemple de disposition gamma pour un élément de liste de vérification.](images/content-view/gammaviewmore.png)

-   L’illustration suivante montre la disposition gamma lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![Diagramme qui montre un exemple de disposition gamma avec moins de 350 pixels d’espace horizontal.](images/content-view/layout6.png)

-   Exemple de disposition gamma lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![exemple de disposition gamma](images/content-view/gammaviewless.png)

**Disposition Delta**

Le modèle de disposition Delta est optimisé pour afficher de nombreuses propriétés plus courtes, telles que pour la musique et les images. Il présente les spécifications suivantes :

-   Lignes : 2
-   Propriétés : 6
-   Disposition Delta lorsque l’élément a 700 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.

    ![Diagramme qui montre un exemple de disposition Delta.](images/content-view/layout7.png)

-   Exemple de disposition Delta lorsque l’élément a 700 pixels ou plus d’espace horizontal.

    ![Capture d’écran montrant un exemple de disposition Delta pour un fichier musical.](images/content-view/deltalayoutmore.png)

-   Disposition Delta lorsque l’élément a entre 350 et 700 pixels d’espace horizontal.

    ![Diagramme qui montre un exemple de disposition Delta qui a entre 350 et 700 pixels d’espace horizontal.](images/content-view/layout8.png)

-   Exemple de disposition Delta lorsque l’élément a entre 350 et 700 pixels d’espace horizontal.

    ![exemple de disposition Delta](images/content-view/deltaviewbetween.png)

-   Disposition Delta lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![exemple de disposition](images/content-view/layout9.png)

-   Exemple de disposition Delta lorsque l’élément a moins de 350 pixels d’espace horizontal.

    ![Capture d’écran montrant un exemple de disposition Delta pour un fichier musical contenant moins de 350 pixels d’espace horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Étape 3 : enregistrement des propriétés personnalisées et de la disposition pour votre type de fichier

Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier.

**Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier.**

1.  Choisissez parmi les quatre modèles de disposition : alpha, bêta, gamma ou Delta.
2.  Tenez compte des règles de mise en forme suivantes, qui s’appliquent également aux quatre modèles de disposition :
    -   La propriété 1 est toujours affichée dans une plus grande taille de police. Taille de police importante généralement utilisée pour le nom de l’élément, mais peut également être utilisée pour la propriété d’ancrage ou d’autre élément.
    -   La propriété 4 est destinée aux extraits des modèles de disposition alpha, bêta et gamma. Cette propriété est allouée en plus de l’espace dans ces modèles et s’affiche dans une couleur de police grise, par opposition aux autres propriétés, afin de les aider à se mettre en évidence.
    -   Les mesures en pixels ci-dessous se trouvent en pixels relatifs, et la taille comprend l’icône/la miniature à gauche des propriétés et l’espace entre l’icône/la miniature et le rectangle de sélection.
    -   La plupart des propriétés ont une taille d’affichage minimale. Par conséquent, ils ne s’affichent pas s’il n’y a pas suffisamment d’espace pour une taille de vue particulière. La taille minimale est généralement de 100 pixels de largeur.
    -   Chaque modèle de disposition définit le nombre de lignes et le nombre de propriétés dans chaque ligne.
3.  Choisissez les propriétés que vous souhaitez afficher dans la mise en page et la propriété que vous souhaitez afficher dans chaque emplacement. Lorsque vous choisissez la propriété à afficher à chaque position dans la disposition, tenez compte de la longueur typique de la propriété, de son importance pour l’utilisateur et de la nécessité de la supprimer lorsque la taille de la fenêtre est trop petite pour contenir toutes les propriétés.
4.  Inscrivez un modèle de disposition et une liste de propriétés pour votre type de fichier ou type d’élément en ajoutant les clés suivantes sous la clé de Registre ProgID pour le type de fichier ou l’élément (dans cet exemple, pour le type de fichier. xyz).

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Respectez les instructions de mise en forme suivantes pour l’inscription des propriétés :

    -   Chaque inscription commence par `prop:`
    -   Chaque propriété requiert le nom complet de la propriété.
    -   Les propriétés sont séparées par un point-virgule sans espace.
    -   Les propriétés sont affichées dans l’ordre défini par le modèle de disposition sélectionné.
    -   `~` indique que l’étiquette de la propriété ne doit pas être affichée.
    -   `~System.LayoutPattern.PlaceHolder` doit être utilisé si vous souhaitez laisser vide une propriété qui est spécifiée dans le modèle de disposition.

    L’exemple de clé de Registre suivant illustre ces instructions de mise en forme.

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    Les valeurs possibles pour (ContentViewModeForBrowse) sont les suivantes : prop : ~ System. ItemNameDisplay ; System. Author ; System. LayoutPattern. PlaceHolder ; System. Keywords ; System. DateModified ; ~ System. Size

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Noms de genres](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
