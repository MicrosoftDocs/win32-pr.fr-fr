---
description: Dans cet \# exemple C, un formulaire papier a été analysé en tant que fichier png (Portable Network Graphics) et spécifié comme image d’arrière-plan au moment de l’exécution pour un contrôle InkPicture. L’exemple utilise une boîte de message pour afficher les résultats de la reconnaissance de l’écriture manuscrite.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Exemple de formulaire papier numérisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530626"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="13be3-104">Exemple de formulaire papier numérisé</span><span class="sxs-lookup"><span data-stu-id="13be3-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="13be3-105">Dans cet \# exemple C, un formulaire papier a été analysé en tant que fichier png (Portable Network Graphics) et spécifié comme image d’arrière-plan au moment de l’exécution pour un contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="13be3-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="13be3-106">L’exemple utilise une boîte de message pour afficher les résultats de la reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="13be3-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="13be3-107">L’exemple comprend un fichier Extensible Markup Language (XML), Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="13be3-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="13be3-108">Le fichier XML contient le nom du fichier PNG.</span><span class="sxs-lookup"><span data-stu-id="13be3-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="13be3-109">Il contient également `FieldInfo` des éléments qui définissent des zones rectangulaires sur le formulaire où un utilisateur peut entrer de l’encre.</span><span class="sxs-lookup"><span data-stu-id="13be3-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="13be3-110">Les informations contenues dans l' `FieldInfo` élément sont affichées dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="13be3-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="13be3-111">Les éléments gauche, supérieur, droit et bas sont des définitions de coordonnées en pixels pour chaque champ.</span><span class="sxs-lookup"><span data-stu-id="13be3-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="13be3-112">L’exemple Initialise un nouveau [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) avec les données contenues dans Formdata.xml :</span><span class="sxs-lookup"><span data-stu-id="13be3-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="13be3-113">L’image de formulaire spécifiée dans Formdata.xml est chargée comme arrière-plan du contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="13be3-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="13be3-114">La collecte d’encre est ensuite activée pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="13be3-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="13be3-115">Gestionnaires d’événements de menu</span><span class="sxs-lookup"><span data-stu-id="13be3-115">Menu Event Handlers</span></span>

<span data-ttu-id="13be3-116">L’application comprend des gestionnaires d’événements Click pour tous les menus affichés en haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="13be3-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="13be3-117">Recognize (élément de menu)</span><span class="sxs-lookup"><span data-stu-id="13be3-117">Recognize Menu Item</span></span>

<span data-ttu-id="13be3-118">Le gestionnaire d’événements de clic de menu Recognize désactive la collecte d’encre pour le contrôle et recherche un module de reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="13be3-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="13be3-119">Si aucun module de reconnaissance n’est installé, une boîte de dialogue s’affiche.</span><span class="sxs-lookup"><span data-stu-id="13be3-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="13be3-120">Un utilisateur doit ensuite cliquer sur l’option de menu encre ou stylet pour réactiver le contrôle pour l’entrée d’encre.</span><span class="sxs-lookup"><span data-stu-id="13be3-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="13be3-121">Si un module de reconnaissance est installé, la `Recognize` fonction récupère les données XML qui spécifient des coordonnées en pixels pour chaque champ de formulaire.</span><span class="sxs-lookup"><span data-stu-id="13be3-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="13be3-122">Les coordonnées sont converties en coordonnées d’espace d’encre et un rectangle est défini pour chaque champ de formulaire.</span><span class="sxs-lookup"><span data-stu-id="13be3-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="13be3-123">Une fois les rectangles définis, la fonction recherche les traits qui se croisent et se trouvent dans chaque rectangle.</span><span class="sxs-lookup"><span data-stu-id="13be3-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="13be3-124">Enfin, il effectue la reconnaissance de l’encre et affiche les résultats dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="13be3-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="13be3-125">Élément de menu encre</span><span class="sxs-lookup"><span data-stu-id="13be3-125">Ink Menu Item</span></span>

<span data-ttu-id="13be3-126">Le gestionnaire d’événements de clic de menu Ink active le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="13be3-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="13be3-127">Élément de menu PEN</span><span class="sxs-lookup"><span data-stu-id="13be3-127">Pen Menu Item</span></span>

<span data-ttu-id="13be3-128">Le gestionnaire d’événements Click du menu PEN effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="13be3-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="13be3-129">Désactive la collecte d’encres pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) (ce qui est nécessaire avant de modifier la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="13be3-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="13be3-130">Définit la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) pour collecter l’encre.</span><span class="sxs-lookup"><span data-stu-id="13be3-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="13be3-131">Réactive la collection d’encres pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) et bascule les menus stylet, sélectionner et gomme pour indiquer le mode actif.</span><span class="sxs-lookup"><span data-stu-id="13be3-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="13be3-132">Modifier l’élément de menu</span><span class="sxs-lookup"><span data-stu-id="13be3-132">Edit Menu Item</span></span>

<span data-ttu-id="13be3-133">Le gestionnaire d’événements de clic du menu Edition est semblable au gestionnaire d’événements du menu de stylet.</span><span class="sxs-lookup"><span data-stu-id="13be3-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="13be3-134">Il effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="13be3-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="13be3-135">Désactive la collecte d’encres.</span><span class="sxs-lookup"><span data-stu-id="13be3-135">Disables ink collection.</span></span>
-   <span data-ttu-id="13be3-136">Définit la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) sur **Select**, ce qui permet à l’utilisateur d’effectuer une sélection d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="13be3-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="13be3-137">Réactive la collecte d’encre et active les menus stylet, modifier et gomme pour indiquer le mode actif.</span><span class="sxs-lookup"><span data-stu-id="13be3-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="13be3-138">Élément de menu de la gomme</span><span class="sxs-lookup"><span data-stu-id="13be3-138">Eraser Menu Item</span></span>

<span data-ttu-id="13be3-139">Le gestionnaire d’événements de clic du menu gomme définit le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) sur **Delete**, ce qui permet à un utilisateur d’effacer l’encre.</span><span class="sxs-lookup"><span data-stu-id="13be3-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="13be3-140">Il bascule également les éléments de menu stylet, modifier et gomme.</span><span class="sxs-lookup"><span data-stu-id="13be3-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="13be3-141">Effacer l’élément de menu</span><span class="sxs-lookup"><span data-stu-id="13be3-141">Clear Menu Item</span></span>

<span data-ttu-id="13be3-142">Le gestionnaire d’événements de clic de menu effacer supprime la collection de [traits](/previous-versions/ms552701(v=vs.100)) active pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) , effaçant ainsi toute l’encre du formulaire.</span><span class="sxs-lookup"><span data-stu-id="13be3-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="13be3-143">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="13be3-143">Closing the Form</span></span>

<span data-ttu-id="13be3-144">Dans le code généré par le Concepteur Windows Form, le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) est ajouté à la liste des composants du formulaire lorsque le formulaire est initialisé.</span><span class="sxs-lookup"><span data-stu-id="13be3-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="13be3-145">Lorsque le formulaire se ferme, le contrôle InkPicture est supprimé, ainsi que les autres composants du formulaire, par la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="13be3-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13be3-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13be3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13be3-147">InkEdit, contrôle</span><span class="sxs-lookup"><span data-stu-id="13be3-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="13be3-148">Contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="13be3-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
