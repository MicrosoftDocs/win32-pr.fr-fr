---
description: Vous pouvez inscrire une liste de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Inscrire un ensemble de propriétés et un modèle de disposition d’affichage de contenu pour un type de fichier ou un élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104321297"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="588f4-103">Comment inscrire un ensemble de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément</span><span class="sxs-lookup"><span data-stu-id="588f4-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="588f4-104">Vous pouvez inscrire une liste de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément.</span><span class="sxs-lookup"><span data-stu-id="588f4-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="588f4-105">Si votre type de fichier ou élément est également associé à un type, l’inscription de l’affichage de contenu spécifique du type de fichier ou de l’élément remplacera l’inscription de type.</span><span class="sxs-lookup"><span data-stu-id="588f4-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="588f4-106">Cela peut être utile si les propriétés les plus importantes de cet élément sont différentes de celles d’autres éléments du même type.</span><span class="sxs-lookup"><span data-stu-id="588f4-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="588f4-107">Si vous n’associez pas votre type de fichier ou élément à un type d’élément ou inscrivez directement l’affichage de contenu, le système utilise les informations d’affichage de contenu par défaut (stockées dans une clé de Registre référencée par le dernier élément dans le tableau d’association de tous les éléments, à savoir la \_ racine des classes HKEY \_ \\ \* )</span><span class="sxs-lookup"><span data-stu-id="588f4-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="588f4-108">Avant d’inscrire une liste de propriétés personnalisées pour votre type de fichier, vous devez comprendre le mode de résultat de la recherche et le mode de navigation, ainsi que les modèles de disposition qui sont à votre disposition.</span><span class="sxs-lookup"><span data-stu-id="588f4-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="588f4-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="588f4-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="588f4-110">Étape 1 : comprendre le mode de résultat de la recherche et le mode de navigation</span><span class="sxs-lookup"><span data-stu-id="588f4-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="588f4-111">L’affichage du contenu nécessite de définir un modèle de disposition et un ensemble de listes de propriétés pour un élément dans un jeu de résultats de recherche (mode de résultat de la recherche), et lorsque vous accédez à un emplacement de Shell (mode de navigation).</span><span class="sxs-lookup"><span data-stu-id="588f4-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="588f4-112">Vous pouvez utiliser les mêmes valeurs pour les résultats de recherche et parcourir, comme `Kind.Music` c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="588f4-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="588f4-113">Vous pouvez également définir une liste de propriétés et/ou un modèle de disposition différent `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="588f4-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="588f4-114">Dans le cas de `Kind.Document` , les utilisateurs recherchent souvent des mots dans le texte du document.</span><span class="sxs-lookup"><span data-stu-id="588f4-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="588f4-115">Par conséquent, l’ajout d’un plus grand nombre d’exemples de texte dans les résultats de la recherche peut être le meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="588f4-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="588f4-116">L’exemple suivant illustre l’affichage parcourir le contenu de `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="588f4-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![Parcourir l’affichage du contenu de kind.document](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="588f4-118">Étant donné que les utilisateurs recherchent rarement du texte particulier lors de la recherche de documents, l’optimisation de votre choix de propriétés et de la mise en page pour s’adapter à d’autres résultats de recherche sur l’écran peut être le meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="588f4-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="588f4-119">La capture d’écran suivante illustre l’affichage du contenu de recherche de `Kind.Document` .</span><span class="sxs-lookup"><span data-stu-id="588f4-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="588f4-120">Étape 2 : présentation des modèles de disposition</span><span class="sxs-lookup"><span data-stu-id="588f4-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="588f4-121">Il existe quatre modèles de disposition : alpha, bêta, gamma et Delta.</span><span class="sxs-lookup"><span data-stu-id="588f4-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="588f4-122">**Disposition alpha**</span><span class="sxs-lookup"><span data-stu-id="588f4-122">**Alpha layout**</span></span>

<span data-ttu-id="588f4-123">Le modèle de disposition alpha est optimisé pour les résultats de recherche de documents qui contiennent des extraits.</span><span class="sxs-lookup"><span data-stu-id="588f4-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="588f4-124">Il présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="588f4-124">It has the following specifications:</span></span>

-   <span data-ttu-id="588f4-125">Lignes : 4</span><span class="sxs-lookup"><span data-stu-id="588f4-125">Rows: 4</span></span>
-   <span data-ttu-id="588f4-126">Propriétés : 7</span><span class="sxs-lookup"><span data-stu-id="588f4-126">Properties: 7</span></span>
-   <span data-ttu-id="588f4-127">Disposition alpha lorsque l’élément a 350 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="588f4-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![modèle de disposition alpha](images/content-view/layout1.png)

-   <span data-ttu-id="588f4-129">L’illustration suivante montre la disposition alpha lorsque l’élément a 350 pixels ou plus d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramme illustrant un exemple de disposition alpha](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="588f4-131">L’illustration suivante montre la disposition alpha lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Capture d’écran montrant un exemple de disposition alpha dans Microsoft Word.](images/content-view/layout2.png)

-   <span data-ttu-id="588f4-133">L’illustration suivante montre la disposition alpha lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemple de disposition alpha](images/content-view/alphaviewless.png)

<span data-ttu-id="588f4-135">**Disposition bêta**</span><span class="sxs-lookup"><span data-stu-id="588f4-135">**Beta Layout**</span></span>

<span data-ttu-id="588f4-136">Le modèle de disposition bêta est optimisé pour les résultats de recherche de documents de courrier électronique qui contiennent des extraits.</span><span class="sxs-lookup"><span data-stu-id="588f4-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="588f4-137">Il présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="588f4-137">It has the following specifications:</span></span>

-   <span data-ttu-id="588f4-138">Lignes : 4</span><span class="sxs-lookup"><span data-stu-id="588f4-138">Rows: 4</span></span>
-   <span data-ttu-id="588f4-139">Propriétés : 5</span><span class="sxs-lookup"><span data-stu-id="588f4-139">Properties: 5</span></span>
-   <span data-ttu-id="588f4-140">Disposition bêta lorsque l’élément a 350 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="588f4-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagramme qui montre un exemple de disposition bêta.](images/content-view/layout3.png)

-   <span data-ttu-id="588f4-142">L’illustration suivante montre la disposition de la version bêta lorsque l’élément a 350 pixels ou plus d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Capture d’écran montrant un exemple de disposition bêta pour le courrier électronique.](images/content-view/betaviewmore.png)

-   <span data-ttu-id="588f4-144">L’illustration suivante montre la disposition de la version bêta lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagramme qui montre un exemple de disposition bêta avec moins de 350 pixels d’espace horizontal.](images/content-view/layout4.png)

-   <span data-ttu-id="588f4-146">L’illustration suivante montre la disposition de la version bêta lorsque l’élément a moins de 350 pixels d’espace horizontal :</span><span class="sxs-lookup"><span data-stu-id="588f4-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![exemple de disposition bêta](images/content-view/betaviewless.png)

<span data-ttu-id="588f4-148">**Disposition gamma**</span><span class="sxs-lookup"><span data-stu-id="588f4-148">**Gamma Layout**</span></span>

<span data-ttu-id="588f4-149">Le modèle de disposition gamma est semblable à alpha, mais utilise une disposition à deux lignes au lieu de quatre.</span><span class="sxs-lookup"><span data-stu-id="588f4-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="588f4-150">Cette disposition est idéale pour les scénarios dans lesquels vous souhaitez afficher un extrait de code, mais vous souhaitez afficher plus d’éléments à l’écran, ou pour les types de fichiers qui nécessitent moins d’espace pour afficher les informations les plus critiques.</span><span class="sxs-lookup"><span data-stu-id="588f4-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="588f4-151">La disposition gamma présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="588f4-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="588f4-152">Lignes : 2</span><span class="sxs-lookup"><span data-stu-id="588f4-152">Rows: 2</span></span>
-   <span data-ttu-id="588f4-153">Propriétés : 4</span><span class="sxs-lookup"><span data-stu-id="588f4-153">Properties: 4</span></span>
-   <span data-ttu-id="588f4-154">L’illustration suivante montre la disposition gamma lorsque l’élément a 350 pixels ou plus d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Diagramme qui montre un exemple de disposition gamma.](images/content-view/layout5.png)

-   <span data-ttu-id="588f4-156">L’illustration suivante montre la disposition gamma lorsque l’élément a 350 pixels ou plus d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![Capture d’écran montrant un exemple de disposition gamma pour un élément de liste de vérification.](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="588f4-158">L’illustration suivante montre la disposition gamma lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Diagramme qui montre un exemple de disposition gamma avec moins de 350 pixels d’espace horizontal.](images/content-view/layout6.png)

-   <span data-ttu-id="588f4-160">Exemple de disposition gamma lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemple de disposition gamma](images/content-view/gammaviewless.png)

<span data-ttu-id="588f4-162">**Disposition Delta**</span><span class="sxs-lookup"><span data-stu-id="588f4-162">**Delta Layout**</span></span>

<span data-ttu-id="588f4-163">Le modèle de disposition Delta est optimisé pour afficher de nombreuses propriétés plus courtes, telles que pour la musique et les images.</span><span class="sxs-lookup"><span data-stu-id="588f4-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="588f4-164">Il présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="588f4-164">It has the following specifications:</span></span>

-   <span data-ttu-id="588f4-165">Lignes : 2</span><span class="sxs-lookup"><span data-stu-id="588f4-165">Rows: 2</span></span>
-   <span data-ttu-id="588f4-166">Propriétés : 6</span><span class="sxs-lookup"><span data-stu-id="588f4-166">Properties: 6</span></span>
-   <span data-ttu-id="588f4-167">Disposition Delta lorsque l’élément a 700 pixels ou plus d’espace horizontal, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="588f4-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Diagramme qui montre un exemple de disposition Delta.](images/content-view/layout7.png)

-   <span data-ttu-id="588f4-169">Exemple de disposition Delta lorsque l’élément a 700 pixels ou plus d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![Capture d’écran montrant un exemple de disposition Delta pour un fichier musical.](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="588f4-171">Disposition Delta lorsque l’élément a entre 350 et 700 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![Diagramme qui montre un exemple de disposition Delta qui a entre 350 et 700 pixels d’espace horizontal.](images/content-view/layout8.png)

-   <span data-ttu-id="588f4-173">Exemple de disposition Delta lorsque l’élément a entre 350 et 700 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![exemple de disposition Delta](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="588f4-175">Disposition Delta lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![exemple de disposition](images/content-view/layout9.png)

-   <span data-ttu-id="588f4-177">Exemple de disposition Delta lorsque l’élément a moins de 350 pixels d’espace horizontal.</span><span class="sxs-lookup"><span data-stu-id="588f4-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Capture d’écran montrant un exemple de disposition Delta pour un fichier musical contenant moins de 350 pixels d’espace horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="588f4-179">Étape 3 : enregistrement des propriétés personnalisées et de la disposition pour votre type de fichier</span><span class="sxs-lookup"><span data-stu-id="588f4-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="588f4-180">Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier.</span><span class="sxs-lookup"><span data-stu-id="588f4-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="588f4-181">**Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier.**</span><span class="sxs-lookup"><span data-stu-id="588f4-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="588f4-182">Choisissez parmi les quatre modèles de disposition : alpha, bêta, gamma ou Delta.</span><span class="sxs-lookup"><span data-stu-id="588f4-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="588f4-183">Tenez compte des règles de mise en forme suivantes, qui s’appliquent également aux quatre modèles de disposition :</span><span class="sxs-lookup"><span data-stu-id="588f4-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="588f4-184">La propriété 1 est toujours affichée dans une plus grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="588f4-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="588f4-185">Taille de police importante généralement utilisée pour le nom de l’élément, mais peut également être utilisée pour la propriété d’ancrage ou d’autre élément.</span><span class="sxs-lookup"><span data-stu-id="588f4-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="588f4-186">La propriété 4 est destinée aux extraits des modèles de disposition alpha, bêta et gamma.</span><span class="sxs-lookup"><span data-stu-id="588f4-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="588f4-187">Cette propriété est allouée en plus de l’espace dans ces modèles et s’affiche dans une couleur de police grise, par opposition aux autres propriétés, afin de les aider à se mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="588f4-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="588f4-188">Les mesures en pixels ci-dessous se trouvent en pixels relatifs, et la taille comprend l’icône/la miniature à gauche des propriétés et l’espace entre l’icône/la miniature et le rectangle de sélection.</span><span class="sxs-lookup"><span data-stu-id="588f4-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="588f4-189">La plupart des propriétés ont une taille d’affichage minimale.</span><span class="sxs-lookup"><span data-stu-id="588f4-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="588f4-190">Par conséquent, ils ne s’affichent pas s’il n’y a pas suffisamment d’espace pour une taille de vue particulière.</span><span class="sxs-lookup"><span data-stu-id="588f4-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="588f4-191">La taille minimale est généralement de 100 pixels de largeur.</span><span class="sxs-lookup"><span data-stu-id="588f4-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="588f4-192">Chaque modèle de disposition définit le nombre de lignes et le nombre de propriétés dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="588f4-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="588f4-193">Choisissez les propriétés que vous souhaitez afficher dans la mise en page et la propriété que vous souhaitez afficher dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="588f4-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="588f4-194">Lorsque vous choisissez la propriété à afficher à chaque position dans la disposition, tenez compte de la longueur typique de la propriété, de son importance pour l’utilisateur et de la nécessité de la supprimer lorsque la taille de la fenêtre est trop petite pour contenir toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="588f4-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="588f4-195">Inscrivez un modèle de disposition et une liste de propriétés pour votre type de fichier ou type d’élément en ajoutant les clés suivantes sous la clé de Registre ProgID pour le type de fichier ou l’élément (dans cet exemple, pour le type de fichier. xyz).</span><span class="sxs-lookup"><span data-stu-id="588f4-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="588f4-196">Respectez les instructions de mise en forme suivantes pour l’inscription des propriétés :</span><span class="sxs-lookup"><span data-stu-id="588f4-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="588f4-197">Chaque inscription commence par `prop:`</span><span class="sxs-lookup"><span data-stu-id="588f4-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="588f4-198">Chaque propriété requiert le nom complet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="588f4-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="588f4-199">Les propriétés sont séparées par un point-virgule sans espace.</span><span class="sxs-lookup"><span data-stu-id="588f4-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="588f4-200">Les propriétés sont affichées dans l’ordre défini par le modèle de disposition sélectionné.</span><span class="sxs-lookup"><span data-stu-id="588f4-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="588f4-201">`~` indique que l’étiquette de la propriété ne doit pas être affichée.</span><span class="sxs-lookup"><span data-stu-id="588f4-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="588f4-202">`~System.LayoutPattern.PlaceHolder` doit être utilisé si vous souhaitez laisser vide une propriété qui est spécifiée dans le modèle de disposition.</span><span class="sxs-lookup"><span data-stu-id="588f4-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="588f4-203">L’exemple de clé de Registre suivant illustre ces instructions de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="588f4-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="588f4-204">Les valeurs possibles pour (ContentViewModeForBrowse) sont les suivantes : prop : ~ System. ItemNameDisplay ; System. Author ; System. LayoutPattern. PlaceHolder ; System. Keywords ; System. DateModified ; ~ System. Size</span><span class="sxs-lookup"><span data-stu-id="588f4-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="588f4-205">Notes</span><span class="sxs-lookup"><span data-stu-id="588f4-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="588f4-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="588f4-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="588f4-207">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="588f4-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="588f4-208">Noms de genres</span><span class="sxs-lookup"><span data-stu-id="588f4-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="588f4-209">System. PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="588f4-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="588f4-210">System. PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="588f4-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
