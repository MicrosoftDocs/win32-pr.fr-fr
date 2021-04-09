---
title: S’assurer que les éléments d’interface utilisateur sont correctement nommés
description: Cette rubrique décrit la méthode correcte pour spécifier les noms des éléments d’interface utilisateur dans vos applications Microsoft Win32 afin que Microsoft Active Accessibility puisse exposer avec précision les noms aux applications clientes par le biais du IAccessible \ 32 ; Propriété Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941051"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="e273c-103">S’assurer que les éléments d’interface utilisateur sont correctement nommés</span><span class="sxs-lookup"><span data-stu-id="e273c-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="e273c-104">Cette rubrique décrit la méthode correcte pour spécifier les noms des éléments d’interface utilisateur dans vos applications Microsoft Win32 afin que Microsoft Active Accessibility puisse exposer avec précision les noms aux applications clientes via la [propriété de nom](name-property.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="e273c-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="e273c-105">Les informations contenues dans cette section s’appliquent uniquement à Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e273c-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="e273c-106">Elle ne s’applique pas aux applications qui utilisent Microsoft UI Automation ou à celles basées sur des langages de balisage tels que HTML, DHTML (Dynamic HTML) ou XML.</span><span class="sxs-lookup"><span data-stu-id="e273c-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="e273c-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="e273c-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="e273c-108">Comment des noms incorrects provoquent des problèmes</span><span class="sxs-lookup"><span data-stu-id="e273c-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="e273c-109">Comment MSAA obtient la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="e273c-110">Comment rechercher et corriger les problèmes de nom</span><span class="sxs-lookup"><span data-stu-id="e273c-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="e273c-111">Comment nommer correctement un TrackBar</span><span class="sxs-lookup"><span data-stu-id="e273c-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="e273c-112">Comment utiliser des étiquettes invisibles pour nommer des contrôles</span><span class="sxs-lookup"><span data-stu-id="e273c-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="e273c-113">Comment utiliser l’annotation directe pour spécifier la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="e273c-114">Étapes pour l’annotation de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="e273c-115">Exemple d’annotation de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="e273c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e273c-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e273c-117">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="e273c-117">Overview</span></span>

<span data-ttu-id="e273c-118">Dans Microsoft Active Accessibility, chaque élément d’interface utilisateur d’une application est représenté par un objet qui expose l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="e273c-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="e273c-119">Les applications clientes utilisent les propriétés et les méthodes de l’interface **IAccessible** pour interagir avec l’élément d’interface utilisateur et pour récupérer des informations à leur sujet.</span><span class="sxs-lookup"><span data-stu-id="e273c-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="e273c-120">L’une des propriétés les plus importantes exposées par l’interface **IAccessible** est la [propriété Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="e273c-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="e273c-121">Les applications clientes s’appuient sur la propriété Name pour rechercher, identifier ou annoncer un élément d’interface utilisateur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e273c-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="e273c-122">Si Microsoft Active Accessibility ne peut pas exposer correctement la propriété Name d’un élément d’interface utilisateur particulier, les applications clientes ne peuvent pas présenter cet élément d’interface utilisateur à l’utilisateur, et l’élément d’interface utilisateur est inaccessible aux utilisateurs handicapés.</span><span class="sxs-lookup"><span data-stu-id="e273c-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="e273c-123">Comment des noms incorrects provoquent des problèmes</span><span class="sxs-lookup"><span data-stu-id="e273c-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="e273c-124">Pour illustrer les problèmes causés par une dénomination incorrecte des éléments d’interface utilisateur, prenez en compte le formulaire d’entrée de nom présenté dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="e273c-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![illustration d’un formulaire simple pour entrer le prénom et le nom](images/incorrect-form.png)

<span data-ttu-id="e273c-126">Bien que les éléments de l’interface utilisateur du formulaire semblent OK, l’implémentation par programmation est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="e273c-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="e273c-127">Pour un client Microsoft Active Accessibility, tel qu’un lecteur d’écran, la [propriété Name](name-property.md) du contrôle d’édition Top est « Last Name : », et la propriété Name du contrôle d’édition Bottom est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="e273c-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="e273c-128">Le lecteur d’écran lit le contrôle d’édition du haut comme « Last Name », bien que l’utilisateur soit supposé taper dans le prénom.</span><span class="sxs-lookup"><span data-stu-id="e273c-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="e273c-129">Le lecteur d’écran lira le deuxième contrôle d’édition en tant que « no name », de sorte que l’utilisateur n’aura aucune idée de type dans le deuxième contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e273c-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="e273c-130">Le lecteur d’écran ne peut pas aider l’utilisateur à entrer des données dans ce formulaire simple.</span><span class="sxs-lookup"><span data-stu-id="e273c-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="e273c-131">Un autre problème au niveau du formulaire est qu’aucune touche de raccourci n’est assignée à l’un ou l’autre des contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="e273c-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="e273c-132">L’utilisateur est contraint d’utiliser l’onglet pour les contrôles ou d’utiliser la souris.</span><span class="sxs-lookup"><span data-stu-id="e273c-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="e273c-133">Les sections suivantes expliquent la source de ces problèmes et fournissent des instructions pour les corriger.</span><span class="sxs-lookup"><span data-stu-id="e273c-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="e273c-134">Comment MSAA obtient la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="e273c-135">Microsoft Active Accessibility obtient la chaîne de [propriété de nom](name-property.md) à partir de différents emplacements en fonction du type de l’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e273c-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="e273c-136">Pour la plupart des éléments d’interface utilisateur associés à du texte de fenêtre, Microsoft Active Accessibility utilise le texte de la fenêtre comme chaîne de propriété de nom.</span><span class="sxs-lookup"><span data-stu-id="e273c-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="e273c-137">Les contrôles tels que les boutons, les éléments de menu et les info-bulles sont des exemples de ce type d’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e273c-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="e273c-138">Pour les contrôles suivants, Microsoft Active Accessibility ignore le texte de la fenêtre et cherche à la place une étiquette de texte statique (ou une étiquette de zone de groupe) qui précède immédiatement le contrôle dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="e273c-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="e273c-139">Zones de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="e273c-139">Combo Boxes</span></span>
-   <span data-ttu-id="e273c-140">Sélecteurs de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="e273c-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="e273c-141">Contrôles Edit et Rich Edit</span><span class="sxs-lookup"><span data-stu-id="e273c-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="e273c-142">Contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e273c-142">IP Address controls</span></span>
-   <span data-ttu-id="e273c-143">Zones de liste</span><span class="sxs-lookup"><span data-stu-id="e273c-143">List Boxes</span></span>
-   <span data-ttu-id="e273c-144">Affichages de liste</span><span class="sxs-lookup"><span data-stu-id="e273c-144">List Views</span></span>
-   <span data-ttu-id="e273c-145">Barres de progression</span><span class="sxs-lookup"><span data-stu-id="e273c-145">Progress Bars</span></span>
-   <span data-ttu-id="e273c-146">Barres</span><span class="sxs-lookup"><span data-stu-id="e273c-146">Scrollbars</span></span>
-   <span data-ttu-id="e273c-147">Contrôles statiques dotés de l' \_ icône SS ou du \_ style bitmap SS</span><span class="sxs-lookup"><span data-stu-id="e273c-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="e273c-148">Trackbars</span><span class="sxs-lookup"><span data-stu-id="e273c-148">Trackbars</span></span>
-   <span data-ttu-id="e273c-149">Arborescences</span><span class="sxs-lookup"><span data-stu-id="e273c-149">Tree Views</span></span>

<span data-ttu-id="e273c-150">Si les contrôles précédents ne sont pas accompagnés d’étiquettes de texte statiques, ou si les étiquettes ne sont pas implémentées correctement, Microsoft Active Accessibility ne peut pas fournir la [propriété de nom](name-property.md) correcte aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="e273c-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="e273c-151">La plupart des contrôles précédents disposent en fait d’un texte de fenêtre associé.</span><span class="sxs-lookup"><span data-stu-id="e273c-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="e273c-152">L’éditeur de ressources génère automatiquement le texte de la fenêtre, qui se compose d’une chaîne générique telle que « Edit1 » ou « ListBox3 ».</span><span class="sxs-lookup"><span data-stu-id="e273c-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="e273c-153">Bien que les développeurs puissent remplacer le texte de fenêtre généré par du texte plus explicite, le plus jamais.</span><span class="sxs-lookup"><span data-stu-id="e273c-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="e273c-154">Étant donné que le texte de la fenêtre générée n’a aucune signification pour l’utilisateur, Microsoft Active Accessibility l’ignore et utilise à la place l’étiquette de texte statique qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="e273c-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="e273c-155">Comment rechercher et corriger les problèmes de nom</span><span class="sxs-lookup"><span data-stu-id="e273c-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="e273c-156">Dans le formulaire d’entrée de nom qui s’affiche dans la manière dont les noms incorrects provoquent des problèmes, la cause de ces problèmes est que l’ordre de tabulation des contrôles est incorrect.</span><span class="sxs-lookup"><span data-stu-id="e273c-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="e273c-157">L’examen de l’interface utilisateur avec un outil de test tel que l' [inspection](inspect-objects.md) révèle les problèmes de la hiérarchie d’objets.</span><span class="sxs-lookup"><span data-stu-id="e273c-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="e273c-158">La capture d’écran suivante montre la hiérarchie d’objets rompus du formulaire de saisie de nom tel qu’il apparaît dans inspecter.</span><span class="sxs-lookup"><span data-stu-id="e273c-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![capture d’écran de l’outil d’inspection montrant une hiérarchie d’objets incorrecte du formulaire de saisie de nom](images/incorrect-object-hierarchy.png)

<span data-ttu-id="e273c-160">Dans la capture d’écran précédente, vous remarquerez que la hiérarchie d’objets ne correspond pas à la structure des contrôles tels qu’ils apparaissent dans l’interface utilisateur du formulaire d’entrée de nom.</span><span class="sxs-lookup"><span data-stu-id="e273c-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="e273c-161">Notez également que l' [inspection](inspect-objects.md) a affecté le nom incorrect au dernier élément (il s’agit du contrôle d’édition pour entrer le prénom et doit être un nom nommé « First Name : »).</span><span class="sxs-lookup"><span data-stu-id="e273c-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="e273c-162">Enfin, Notez que l’inspection n’a pas pu trouver de nom pour le dernier élément (il s’agit du contrôle d’édition pour entrer le nom de famille et doit avoir le nom « Last Name : ».</span><span class="sxs-lookup"><span data-stu-id="e273c-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="e273c-163">L’exemple suivant montre le contenu du fichier de ressources pour le formulaire d’entrée de nom.</span><span class="sxs-lookup"><span data-stu-id="e273c-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="e273c-164">Notez que l’ordre de tabulation n’est pas cohérent avec la structure logique des contrôles tels qu’ils apparaissent dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e273c-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="e273c-165">Notez également qu’aucune touche de raccourci n’est spécifiée pour les deux contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="e273c-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="e273c-166">Pour résoudre les problèmes liés au formulaire d’entrée de nom, le fichier de ressources (. RC) doit être modifié pour spécifier des raccourcis clavier et les contrôles doivent être placés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="e273c-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="e273c-167">Étiquette de texte statique « &First Name : ».</span><span class="sxs-lookup"><span data-stu-id="e273c-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="e273c-168">Le contrôle d’édition pour l’entrée du prénom (IDC \_ Edit1).</span><span class="sxs-lookup"><span data-stu-id="e273c-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="e273c-169">Étiquette de texte statique « &nom : ».</span><span class="sxs-lookup"><span data-stu-id="e273c-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="e273c-170">Le contrôle d’édition pour la saisie du nom (IDC \_ Edit2).</span><span class="sxs-lookup"><span data-stu-id="e273c-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="e273c-171">Bouton de commande par défaut « OK ».</span><span class="sxs-lookup"><span data-stu-id="e273c-171">The "OK" default push button.</span></span>

<span data-ttu-id="e273c-172">L’exemple suivant montre le fichier de ressources corrigé pour le formulaire d’entrée de nom :</span><span class="sxs-lookup"><span data-stu-id="e273c-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="e273c-173">Pour apporter des corrections à un fichier de ressources, vous pouvez modifier directement le fichier ou utiliser l’outil d’ordre de tabulation dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e273c-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="e273c-174">Vous pouvez accéder à l’outil d’ordre de tabulation dans Visual Studio en appuyant sur CTRL + D ou en sélectionnant **ordre de tabulation** dans le menu **format** .</span><span class="sxs-lookup"><span data-stu-id="e273c-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="e273c-175">Après avoir corrigé et reconstruit l’application, l’interface utilisateur du formulaire de saisie des noms est identique à celle qui était auparavant utilisée.</span><span class="sxs-lookup"><span data-stu-id="e273c-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="e273c-176">Toutefois, Microsoft Active Accessibility fournira à présent les propriétés de nom correctes aux applications clientes et définira le focus correctement quand l’utilisateur appuie sur les raccourcis clavier ALT + F ou ALT + L.</span><span class="sxs-lookup"><span data-stu-id="e273c-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="e273c-177">En outre, l' [inspection](inspect-objects.md) affiche la hiérarchie d’objets correcte, comme le montre la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="e273c-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![capture d’écran de l’outil Explorateur accessible montrant une hiérarchie d’objets correcte du formulaire d’entrée de nom](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="e273c-179">Comment nommer correctement un TrackBar</span><span class="sxs-lookup"><span data-stu-id="e273c-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="e273c-180">Lors de la définition d’un TrackBar (ou d’un curseur), assurez-vous que l’étiquette de texte statique principale pour la barre de défilement s’affiche avant le TrackBar et que les étiquettes de texte statique pour les plages minimale et maximale apparaissent après le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e273c-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="e273c-181">N’oubliez pas que Microsoft Active Accessibility utilise l’étiquette de texte statique qui précède immédiatement un contrôle comme [propriété de nom](name-property.md) pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e273c-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="e273c-182">Le fait de placer l’étiquette de texte statique principale juste avant le TrackBar, et les autres étiquettes ultérieures, garantit que Microsoft Active Accessibility fournit la propriété de nom correcte à un client.</span><span class="sxs-lookup"><span data-stu-id="e273c-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="e273c-183">L’illustration suivante montre un TrackBar typique avec une étiquette de texte statique principale appelée « Speed » et des étiquettes de texte statiques pour les plages minimum (« min ») et maximum (« max »).</span><span class="sxs-lookup"><span data-stu-id="e273c-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![illustration d’un contrôle TrackBar qui a une étiquette principale et des étiquettes pour les plages minimale et maximale](images/speed-trackbar.png)

<span data-ttu-id="e273c-185">L’exemple suivant illustre la façon correcte de définir un TrackBar et ses étiquettes de texte statiques dans le fichier de ressources :</span><span class="sxs-lookup"><span data-stu-id="e273c-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="e273c-186">Comment utiliser des étiquettes invisibles pour nommer des contrôles</span><span class="sxs-lookup"><span data-stu-id="e273c-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="e273c-187">Il n’est pas toujours possible ou souhaitable d’avoir une étiquette visible pour chaque contrôle.</span><span class="sxs-lookup"><span data-stu-id="e273c-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="e273c-188">Par exemple, l’ajout d’étiquettes peut parfois entraîner des modifications indésirables dans l’apparence de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e273c-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="e273c-189">Dans ce cas, vous pouvez utiliser des étiquettes invisibles.</span><span class="sxs-lookup"><span data-stu-id="e273c-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="e273c-190">Microsoft Active Accessibility récupère toujours le texte associé à une étiquette invisible, mais l’étiquette n’apparaît pas dans l’interface utilisateur visuel ou en interfère avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e273c-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="e273c-191">Comme avec les étiquettes visibles, une étiquette invisible doit immédiatement précéder le contrôle dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="e273c-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="e273c-192">Pour rendre une étiquette invisible dans un fichier de ressources (. RC), ajoutez `NOT WS_VISIBLE` ou `|~WS_VISIBLE` à la partie de style du contrôle de texte statique.</span><span class="sxs-lookup"><span data-stu-id="e273c-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="e273c-193">Si vous utilisez l’éditeur de ressources dans Visual Studio, vous pouvez définir la propriété visible sur false.</span><span class="sxs-lookup"><span data-stu-id="e273c-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="e273c-194">Comment utiliser l’annotation directe pour spécifier la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="e273c-195">Les proxys par défaut inclus dans le composant d’exécution Microsoft Active Accessibility, Oleacc.dll fournissent automatiquement un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour tous les contrôles Windows standard.</span><span class="sxs-lookup"><span data-stu-id="e273c-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="e273c-196">Si vous personnalisez un contrôle Windows standard, les proxies par défaut font de leur mieux pour fournir avec précision toutes les propriétés **IAccessible** pour votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e273c-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="e273c-197">Vous devez tester minutieusement un contrôle personnalisé pour vous assurer que les proxies par défaut fournissent des valeurs de propriété précises et complètes.</span><span class="sxs-lookup"><span data-stu-id="e273c-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="e273c-198">Si le test révèle des valeurs de propriété inexactes ou incomplètes, vous pourrez peut-être utiliser la technique d’annotation dynamique appelée annotation directe pour fournir des valeurs de propriété correctes et ajouter celles qui sont manquantes.</span><span class="sxs-lookup"><span data-stu-id="e273c-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="e273c-199">Notez que l’annotation dynamique n’est pas seulement pour les contrôles pris en charge par les proxies Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e273c-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="e273c-200">Vous pouvez également l’utiliser pour modifier ou fournir des propriétés pour tout contrôle qui fournit sa propre implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="e273c-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="e273c-201">Cette section se concentre sur l’utilisation de l’annotation directe pour fournir une valeur correcte pour la [propriété Name](name-property.md) de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="e273c-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="e273c-202">Vous pouvez utiliser l’annotation directe pour fournir également d’autres valeurs de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e273c-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="e273c-203">En outre, d’autres techniques d’annotation dynamique à côté des annotations directes sont disponibles, et les fonctionnalités et fonctionnalités de l’API d’annotation dynamique s’étendent bien au-delà de ce qui est décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e273c-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="e273c-204">Pour plus d’informations sur les annotations dynamiques, consultez [API d’annotation dynamique](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="e273c-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="e273c-205">Étapes pour l’annotation de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="e273c-206">L’utilisation de l’annotation directe pour modifier la [propriété Name](name-property.md) d’un contrôle implique les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e273c-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="e273c-207">Incluez les fichiers d’en-tête suivants :</span><span class="sxs-lookup"><span data-stu-id="e273c-207">Include the following header files:</span></span>
    -   <span data-ttu-id="e273c-208">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="e273c-208">Initguid.h</span></span>
    -   <span data-ttu-id="e273c-209">Oleacc. h</span><span class="sxs-lookup"><span data-stu-id="e273c-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="e273c-210">Pour définir des GUID, vous devez inclure Initguid. h avant oleacc. h dans le même fichier.</span><span class="sxs-lookup"><span data-stu-id="e273c-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="e273c-211">Initialisez la bibliothèque COM (Component Object Model) en appelant la fonction [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , en général pendant le processus d’initialisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="e273c-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="e273c-212">Peu après la création du contrôle cible (en général, pendant le message [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) ), créez une instance du gestionnaire d’annotations et obtenez un pointeur vers son pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="e273c-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="e273c-213">Annotez la [propriété Name](name-property.md) du contrôle cible à l’aide de la méthode [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .</span><span class="sxs-lookup"><span data-stu-id="e273c-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="e273c-214">Libère le pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="e273c-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="e273c-215">Avant de détruire le contrôle cible (en général, lors de la gestion du message [WM \_ Destroy](../winmsg/wm-destroy.md) ), créez une instance du gestionnaire d’annotations et obtenez un pointeur vers son interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="e273c-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="e273c-216">Utilisez la méthode [**IAccPropServices :: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) pour effacer les annotations de [propriété de nom](name-property.md) du contrôle cible.</span><span class="sxs-lookup"><span data-stu-id="e273c-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="e273c-217">Libère le pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="e273c-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="e273c-218">Avant de quitter votre application (en général, lors du traitement du message [WM \_ Destroy](../winmsg/wm-destroy.md) ), libérez la bibliothèque com en appelant la fonction [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="e273c-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="e273c-219">La fonction [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) accepte cinq paramètres.</span><span class="sxs-lookup"><span data-stu-id="e273c-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="e273c-220">Les trois premiers,*HWND*, *idObject* et *idChild*, s’associent pour identifier le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e273c-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="e273c-221">Le quatrième paramètre, *idProp*, spécifie l’identificateur de la propriété à modifier.</span><span class="sxs-lookup"><span data-stu-id="e273c-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="e273c-222">Pour modifier la [propriété Name](name-property.md), définissez *idProp* sur **propid \_ ACC \_ nom**.</span><span class="sxs-lookup"><span data-stu-id="e273c-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="e273c-223">(Pour obtenir la liste des autres propriétés que vous pouvez définir via l’annotation directe, consultez [utilisation de l’annotation directe](using-direct-annotation.md).) Le dernier paramètre de **SetHwndPropStr**, *Str*, est la nouvelle chaîne à utiliser comme propriété Name.</span><span class="sxs-lookup"><span data-stu-id="e273c-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="e273c-224">Exemple d’annotation de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="e273c-225">L’exemple de code suivant montre comment utiliser l’annotation directe pour modifier la [propriété Name](name-property.md) de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="e273c-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="e273c-226">Pour simplifier les choses, l’exemple utilise une chaîne codée en dur (« New Control Name ») pour définir la propriété Name.</span><span class="sxs-lookup"><span data-stu-id="e273c-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="e273c-227">Les chaînes codées en dur ne doivent pas être utilisées dans la version finale de votre application, car elles ne peuvent pas être localisées.</span><span class="sxs-lookup"><span data-stu-id="e273c-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="e273c-228">Au lieu de cela, chargez toujours des chaînes à partir de votre fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="e273c-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="e273c-229">En outre, l’exemple n’affiche pas les appels aux fonctions [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="e273c-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e273c-230">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e273c-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e273c-231">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e273c-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e273c-232">API d’annotation dynamique</span><span class="sxs-lookup"><span data-stu-id="e273c-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="e273c-233">Fourniture de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="e273c-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="e273c-234">Outils de test</span><span class="sxs-lookup"><span data-stu-id="e273c-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 