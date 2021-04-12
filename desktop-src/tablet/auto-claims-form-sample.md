---
description: L’exemple auto claims résout un scénario hypothétique pour un évaluateur d’assurance.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Exemple de formulaire de déclaration automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319733"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="d6a56-103">Exemple de formulaire de déclaration automatique</span><span class="sxs-lookup"><span data-stu-id="d6a56-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="d6a56-104">L’exemple auto claims résout un scénario hypothétique pour un évaluateur d’assurance.</span><span class="sxs-lookup"><span data-stu-id="d6a56-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="d6a56-105">Le travail de l’évaluateur lui impose de visiter les clients de leur famille ou de leur entreprise et d’entrer leurs informations de revendication dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6a56-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="d6a56-106">Pour augmenter la productivité de l’évaluateur, son service informatique développe une application de tablette qui lui permet d’entrer rapidement et avec précision des informations de revendication à l’aide de deux contrôles Ink : les contrôles [InkEdit](/previous-versions/ms835842(v=msdn.10)) et [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d6a56-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="d6a56-107">Dans cet exemple, un contrôle [InkEdit](/previous-versions/ms835842(v=msdn.10)) est utilisé pour chaque champ d’entrée de texte.</span><span class="sxs-lookup"><span data-stu-id="d6a56-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="d6a56-108">Un utilisateur entre les informations pertinentes relatives à une stratégie d’assurance et un véhicule dans ces champs à l’aide d’un stylet.</span><span class="sxs-lookup"><span data-stu-id="d6a56-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="d6a56-109">Le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) est utilisé pour ajouter de l’encre sur une image automobile pour mettre en surbrillance les zones endommagées de l’automobile.</span><span class="sxs-lookup"><span data-stu-id="d6a56-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="d6a56-110">L’exemple de revendications automatiques est disponible pour C \# et Microsoft Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="d6a56-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="d6a56-111">Cette rubrique décrit les Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="d6a56-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="d6a56-112">La classe autorevendication est définie comme une sous-classe de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , et une classe imbriquée est définie pour créer et gérer des couches d’encre pour différents types d’endommagement.</span><span class="sxs-lookup"><span data-stu-id="d6a56-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="d6a56-113">Quatre gestionnaires d’événements sont définis pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6a56-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="d6a56-114">Initialisation du formulaire et des couches d’encre.</span><span class="sxs-lookup"><span data-stu-id="d6a56-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="d6a56-115">Redessin du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d6a56-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="d6a56-116">Sélection d’une couche d’encre dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d6a56-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="d6a56-117">Modification de la visibilité d’une couche d’encre.</span><span class="sxs-lookup"><span data-stu-id="d6a56-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="d6a56-118">Les versions de cet exemple sont disponibles en C \# et Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="d6a56-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="d6a56-119">La version décrite dans cette section est Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="d6a56-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="d6a56-120">Les concepts sont les mêmes entre les versions.</span><span class="sxs-lookup"><span data-stu-id="d6a56-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="d6a56-121">Définition du formulaire et des couches d’encre</span><span class="sxs-lookup"><span data-stu-id="d6a56-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="d6a56-122">Vous devez importer l’espace de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="d6a56-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="d6a56-123">Ensuite, dans la classe autorevendications, une classe imbriquée `InkLayer` est définie et un tableau de quatre `InkLayer` objets est déclaré.</span><span class="sxs-lookup"><span data-stu-id="d6a56-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="d6a56-124">(InkLayer contient un objet [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) pour le stockage de l’encre, et [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) et des valeurs **booléennes** pour stocker la couleur et l’état masqué de la couche.) Un cinquième objet Ink est déclaré pour gérer l’encre pour l' [InkPicture](/previous-versions/ms583740(v=vs.100)) lorsque toutes les couches d’encre sont masquées.</span><span class="sxs-lookup"><span data-stu-id="d6a56-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="d6a56-125">Chaque couche a son propre objet [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d6a56-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="d6a56-126">Le formulaire de revendication comporte quatre zones discrètes intéressantes (corps, fenêtres, pneus et phares). quatre objets InkLayer sont donc utilisés.</span><span class="sxs-lookup"><span data-stu-id="d6a56-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="d6a56-127">Un utilisateur peut afficher n’importe quelle combinaison de couches à la fois.</span><span class="sxs-lookup"><span data-stu-id="d6a56-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="d6a56-128">Initialisation du formulaire et des couches d’encre</span><span class="sxs-lookup"><span data-stu-id="d6a56-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="d6a56-129">Le `Load` Gestionnaire d’événements initialise l’objet [Ink](/previous-versions/ms583670(v=vs.100)) et les quatre `InkLayer` objets.</span><span class="sxs-lookup"><span data-stu-id="d6a56-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="d6a56-130">Ensuite, sélectionnez la première entrée (corps) dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d6a56-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="d6a56-131">Enfin, définissez la couleur d’encre du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) sur l’entrée de zone de liste actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d6a56-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="d6a56-132">Redessiner le contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="d6a56-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="d6a56-133">Dans le gestionnaire d’événements de [peinture](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) hérité du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) , les couches d’encre sont vérifiées pour déterminer celles qui sont masquées.</span><span class="sxs-lookup"><span data-stu-id="d6a56-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="d6a56-134">Si une couche n’est pas masquée, la procédure événementielle l’affiche à l’aide de la méthode [Draw](/previous-versions/ms828488(v=msdn.10)) de la propriété [Renderer](/previous-versions/ms582196(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d6a56-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="d6a56-135">Si vous regardez dans l’Explorateur d’objets, vous verrez que la propriété Microsoft. Ink. InkPicture. Renderer est définie en tant qu’objet [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="d6a56-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="d6a56-136">Sélection d’une couche d’encre dans la zone de liste</span><span class="sxs-lookup"><span data-stu-id="d6a56-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="d6a56-137">Lorsque l’utilisateur sélectionne un élément dans la zone de liste, le gestionnaire d’événements [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) vérifie d’abord que la sélection a changé et que le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) ne collecte pas d’encre pour le moment.</span><span class="sxs-lookup"><span data-stu-id="d6a56-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="d6a56-138">Il définit ensuite la couleur d’encre du contrôle InkPicture sur la couleur appropriée pour la couche d’encre sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d6a56-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="d6a56-139">En outre, il met à jour la case à cocher Masquer la couche pour refléter l’état masqué de la couche d’encre sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d6a56-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="d6a56-140">Enfin, la méthode d' [actualisation](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) héritée du contrôle InkPicture est utilisée pour afficher uniquement les couches souhaitées dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d6a56-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="d6a56-141">Modification de la visibilité d’une couche d’encre</span><span class="sxs-lookup"><span data-stu-id="d6a56-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="d6a56-142">Le `CheckedChanged` Gestionnaire d’événements vérifie d’abord que la sélection a changé et que le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) ne collecte pas d’encre pour le moment.</span><span class="sxs-lookup"><span data-stu-id="d6a56-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="d6a56-143">Il met ensuite à jour l’état masqué de la couche d’encre sélectionnée, définit le InkEnabled du contrôle InkPicture sur **false**,.</span><span class="sxs-lookup"><span data-stu-id="d6a56-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="d6a56-144">Ensuite, la propriété InkEnabled du contrôle InkPicture est définie sur **false** avant la mise à jour de sa propriété Ink.</span><span class="sxs-lookup"><span data-stu-id="d6a56-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="d6a56-145">Enfin, le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) est activé ou désactivé pour la partie de véhicule particulière selon que la case à cocher Masquer la couche est activée et que la méthode [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) du contrôle InkPicture est utilisée pour afficher uniquement les couches souhaitées dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d6a56-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="d6a56-146">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="d6a56-146">Closing the Form</span></span>

<span data-ttu-id="d6a56-147">Dans le code généré par le Concepteur Windows Form, les contrôles [InkEdit](/previous-versions/ms835842(v=msdn.10)) et [InkPicture](/previous-versions/ms583740(v=vs.100)) sont ajoutés à la liste des composants du formulaire lorsque le formulaire est initialisé.</span><span class="sxs-lookup"><span data-stu-id="d6a56-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="d6a56-148">Lorsque le formulaire se ferme, les contrôles InkEdit et InkPicture sont supprimés, ainsi que les autres composants du formulaire, par la méthode [dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6a56-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="d6a56-149">La méthode dispose du formulaire supprime également les objets [Ink](/previous-versions/ms583670(v=vs.100)) créés pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6a56-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6a56-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6a56-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d6a56-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="d6a56-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="d6a56-152">Contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="d6a56-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="d6a56-153">InkEdit, contrôle</span><span class="sxs-lookup"><span data-stu-id="d6a56-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
