---
title: Contrôle de contrôle
description: Définit un contrôle défini par l’utilisateur.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menus du contrôle de contrôle et autres ressources
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940923"
---
# <a name="control-control"></a><span data-ttu-id="89428-104">Contrôle de contrôle</span><span class="sxs-lookup"><span data-stu-id="89428-104">CONTROL control</span></span>

<span data-ttu-id="89428-105">Définit un contrôle défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89428-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="89428-106"><span id="class"></span><span id="CLASS"></span>*type*</span><span class="sxs-lookup"><span data-stu-id="89428-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="89428-107">Nom redéfini, chaîne de caractères ou valeur d’entier non signé 16 bits qui définit la classe.</span><span class="sxs-lookup"><span data-stu-id="89428-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="89428-108">Il peut s’agir de l’une des classes de contrôle ; pour obtenir la liste des classes de contrôle, consultez la première liste qui suit cette description.</span><span class="sxs-lookup"><span data-stu-id="89428-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="89428-109">Si la valeur est un nom redéfini fourni par l’application, il doit s’agir d’une chaîne placée entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="89428-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="89428-110"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="89428-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="89428-111">Nom redéfini ou valeur entière qui spécifie le style du contrôle donné.</span><span class="sxs-lookup"><span data-stu-id="89428-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="89428-112">La signification exacte du *style* dépend de la valeur de la *classe* .</span><span class="sxs-lookup"><span data-stu-id="89428-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="89428-113">Les sections qui suivent cette description affichent les classes de contrôle et les styles correspondants.</span><span class="sxs-lookup"><span data-stu-id="89428-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="89428-114">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89428-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="89428-115">Notes</span><span class="sxs-lookup"><span data-stu-id="89428-115">Remarks</span></span>

<span data-ttu-id="89428-116">Les six classes de contrôle possibles sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="89428-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="89428-117">Classe de contrôle Button</span><span class="sxs-lookup"><span data-stu-id="89428-117">The Button Control Class</span></span>

<span data-ttu-id="89428-118">Un contrôle Button est une petite fenêtre enfant rectangulaire que l’utilisateur peut activer ou désactiver en cliquant dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="89428-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="89428-119">Les contrôles Button peuvent être utilisés seuls ou dans des groupes, et peuvent être étiquetés ou affichés sans texte.</span><span class="sxs-lookup"><span data-stu-id="89428-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="89428-120">En général, les contrôles de bouton changent d’apparence quand l’utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="89428-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="89428-121">Les styles de bouton sont décrits dans la rubrique suivante : [styles de bouton](../controls/button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="89428-122">Classe de contrôle de zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="89428-122">The Combo Box Control Class</span></span>

<span data-ttu-id="89428-123">Les contrôles de zone de liste déroulante se composent d’un champ de sélection semblable à un contrôle d’édition plus une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="89428-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="89428-124">La zone de liste peut être affichée en permanence ou peut être déplacée lorsque l’utilisateur sélectionne une « zone contextuelle » en regard du champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="89428-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="89428-125">Selon le style de la zone de liste déroulante, l’utilisateur peut ou ne peut pas modifier le contenu du champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="89428-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="89428-126">Si la zone de liste est visible, le fait de taper des caractères dans la zone de sélection entraîne la mise en surbrillance de la première entrée qui correspond aux caractères tapés.</span><span class="sxs-lookup"><span data-stu-id="89428-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="89428-127">À l’inverse, la sélection d’un élément dans la zone de liste affiche le texte sélectionné dans le champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="89428-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="89428-128">Les styles de contrôle de zone de liste déroulante sont décrits dans la rubrique suivante : [styles de zone de liste déroulante](../controls/combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="89428-129">Classe de contrôle d’édition</span><span class="sxs-lookup"><span data-stu-id="89428-129">The Edit Control Class</span></span>

<span data-ttu-id="89428-130">Un contrôle d’édition est une fenêtre enfant rectangulaire dans laquelle l’utilisateur peut entrer du texte à partir du clavier.</span><span class="sxs-lookup"><span data-stu-id="89428-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="89428-131">L’utilisateur sélectionne le contrôle et lui donne le focus d’entrée, en cliquant sur la souris à l’intérieur ou en appuyant sur la touche TAB.</span><span class="sxs-lookup"><span data-stu-id="89428-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="89428-132">L’utilisateur peut entrer du texte lorsque le contrôle affiche un point d’insertion clignotant.</span><span class="sxs-lookup"><span data-stu-id="89428-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="89428-133">La souris peut être utilisée pour déplacer le curseur et sélectionner les caractères à remplacer, ou pour positionner le curseur en insérant des caractères.</span><span class="sxs-lookup"><span data-stu-id="89428-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="89428-134">La touche Retour arrière peut être utilisée pour supprimer des caractères.</span><span class="sxs-lookup"><span data-stu-id="89428-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="89428-135">Les contrôles d’édition utilisent la police à espacement fixe et les caractères Unicode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="89428-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="89428-136">Elles développent les caractères de tabulation dans autant de caractères d’espace que nécessaire pour déplacer le curseur vers le taquet de tabulation suivant.</span><span class="sxs-lookup"><span data-stu-id="89428-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="89428-137">Les taquets de tabulation sont supposés être à chaque huitième caractère.</span><span class="sxs-lookup"><span data-stu-id="89428-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="89428-138">Les styles de contrôle d’édition sont décrits dans la rubrique suivante : [modifier les styles de contrôle](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="89428-139">Classe de contrôle de zone de liste</span><span class="sxs-lookup"><span data-stu-id="89428-139">The List Box Control Class</span></span>

<span data-ttu-id="89428-140">Les contrôles de zone de liste sont constitués d’une liste de chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="89428-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="89428-141">Le contrôle est utilisé chaque fois qu’une application doit présenter une liste de noms, tels que des noms de fichiers, que l’utilisateur peut afficher et sélectionner.</span><span class="sxs-lookup"><span data-stu-id="89428-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="89428-142">L’utilisateur peut sélectionner une chaîne en pointant sur la chaîne à l’aide de la souris et en cliquant sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="89428-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="89428-143">Lorsqu’une chaîne est sélectionnée, elle est mise en surbrillance et un message de notification est transmis à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="89428-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="89428-144">Une barre de défilement peut être utilisée avec un contrôle de zone de liste pour faire défiler des listes qui sont trop longues ou trop larges pour la fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="89428-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="89428-145">Les styles de contrôle de zone de liste sont décrits dans la rubrique suivante : [styles de zone de liste](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="89428-146">Classe de contrôle Scroll-Bar</span><span class="sxs-lookup"><span data-stu-id="89428-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="89428-147">Un contrôle de barre de défilement est un rectangle qui contient un curseur de défilement et qui a des flèches de direction aux deux extrémités.</span><span class="sxs-lookup"><span data-stu-id="89428-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="89428-148">La barre de défilement envoie un message de notification à son parent chaque fois que l’utilisateur clique sur la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="89428-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="89428-149">Le parent est responsable de la mise à jour de la position du curseur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="89428-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="89428-150">Les contrôles de barre de défilement ont la même apparence et la même fonction que les barres de défilement utilisées dans les fenêtres ordinaires.</span><span class="sxs-lookup"><span data-stu-id="89428-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="89428-151">Toutefois, contrairement aux barres de défilement, les contrôles de barre de défilement peuvent être positionnés n’importe où dans une fenêtre et utilisés chaque fois que nécessaire pour fournir une entrée de défilement pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="89428-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="89428-152">Les styles de barre de défilement sont décrits dans la rubrique suivante : [styles de contrôle de barre de défilement](../controls/scroll-bar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="89428-153">Classe de contrôle statique</span><span class="sxs-lookup"><span data-stu-id="89428-153">The Static Control Class</span></span>

<span data-ttu-id="89428-154">Les contrôles statiques sont des champs de texte, des zones et des rectangles simples qui peuvent être utilisés pour étiqueter, Box ou séparer d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="89428-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="89428-155">Les contrôles statiques ne prennent aucune entrée et ne fournissent aucune sortie.</span><span class="sxs-lookup"><span data-stu-id="89428-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="89428-156">Les styles de contrôle statiques sont décrits dans la rubrique suivante : [styles de contrôle statiques](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="89428-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 