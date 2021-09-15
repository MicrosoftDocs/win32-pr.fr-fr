---
description: L’exemple auto claims résout un scénario hypothétique pour un évaluateur d’assurance.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Exemple de formulaire de déclaration automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522293"
---
# <a name="auto-claims-form-sample"></a>Exemple de formulaire de déclaration automatique

L’exemple auto claims résout un scénario hypothétique pour un évaluateur d’assurance. Le travail de l’évaluateur lui impose de visiter les clients de leur famille ou de leur entreprise et d’entrer leurs informations de revendication dans un formulaire. Pour augmenter la productivité de l’évaluateur, son service informatique développe une application de tablette qui lui permet d’entrer rapidement et avec précision des informations de revendication à l’aide de deux contrôles Ink : les contrôles [InkEdit](/previous-versions/ms835842(v=msdn.10)) et [InkPicture](/previous-versions/ms583740(v=vs.100)) .

Dans cet exemple, un contrôle [InkEdit](/previous-versions/ms835842(v=msdn.10)) est utilisé pour chaque champ d’entrée de texte. Un utilisateur entre les informations pertinentes relatives à une stratégie d’assurance et un véhicule dans ces champs à l’aide d’un stylet. Le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) est utilisé pour ajouter de l’encre sur une image automobile pour mettre en surbrillance les zones endommagées de l’automobile. l’exemple de revendications automatiques est disponible pour C \# et Microsoft Visual Basic .net. cette rubrique décrit les Visual Basic .net.

La classe autorevendication est définie en tant que sous-classe de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) et une classe imbriquée sont définis pour créer et gérer des couches d’encre pour différents types d’endommagement. Quatre gestionnaires d’événements sont définis pour effectuer les tâches suivantes :

-   Initialisation du formulaire et des couches d’encre.
-   Redessin du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) .
-   Sélection d’une couche d’encre dans la zone de liste.
-   Modification de la visibilité d’une couche d’encre.

> [!Note]  
> les Versions de cet exemple sont disponibles en C \# et Visual Basic .net. la version décrite dans cette section est Visual Basic .net. Les concepts sont les mêmes entre les versions.

 

## <a name="defining-the-form-and-ink-layers"></a>Définition du formulaire et des couches d’encre

Vous devez importer l’espace de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Ensuite, dans la classe autorevendications, une classe imbriquée `InkLayer` est définie et un tableau de quatre `InkLayer` objets est déclaré. (InkLayer contient un objet [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) pour le stockage de l’encre, et [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) et des valeurs **booléennes** pour stocker la couleur et l’état masqué de la couche.) Un cinquième objet Ink est déclaré pour gérer l’encre pour l' [InkPicture](/previous-versions/ms583740(v=vs.100)) lorsque toutes les couches d’encre sont masquées.


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



Chaque couche a son propre objet [Ink](/previous-versions/ms583670(v=vs.100)) . Le formulaire de revendication comporte quatre zones discrètes intéressantes (corps, fenêtres, pneus et phares). quatre objets InkLayer sont donc utilisés. Un utilisateur peut afficher n’importe quelle combinaison de couches à la fois.

## <a name="initializing-the-form-and-ink-layers"></a>Initialisation du formulaire et des couches d’encre

Le `Load` Gestionnaire d’événements initialise l’objet [Ink](/previous-versions/ms583670(v=vs.100)) et les quatre `InkLayer` objets.


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



Ensuite, sélectionnez la première entrée (corps) dans la zone de liste.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Enfin, définissez la couleur d’encre du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) sur l’entrée de zone de liste actuellement sélectionnée.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Redessiner le contrôle InkPicture

dans le gestionnaire d’événements [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) hérité du contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) , les couches d’encre sont vérifiées pour déterminer celles qui sont masquées. Si une couche n’est pas masquée, la procédure événementielle l’affiche à l’aide de la méthode [Draw](/previous-versions/ms828488(v=msdn.10)) de la propriété [Renderer](/previous-versions/ms582196(v=vs.100)) . Si vous regardez dans l’Explorateur d’objets, vous verrez que la propriété Microsoft. Ink. InkPicture. Renderer est définie en tant qu’objet [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Sélection d’une couche d’encre dans la zone de liste

Lorsque l’utilisateur sélectionne un élément dans la zone de liste, le gestionnaire d’événements [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) vérifie d’abord que la sélection a changé et que le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) ne collecte pas d’encre pour le moment. Il définit ensuite la couleur d’encre du contrôle InkPicture sur la couleur appropriée pour la couche d’encre sélectionnée. En outre, il met à jour la case à cocher Masquer la couche pour refléter l’état masqué de la couche d’encre sélectionnée. Enfin, la méthode d' [actualisation](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) héritée du contrôle InkPicture est utilisée pour afficher uniquement les couches souhaitées dans le contrôle.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Modification de la visibilité d’une couche d’encre

Le `CheckedChanged` Gestionnaire d’événements vérifie d’abord que la sélection a changé et que le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) ne collecte pas d’encre pour le moment. Il met ensuite à jour l’état masqué de la couche d’encre sélectionnée, définit le InkEnabled du contrôle InkPicture sur **false**,.

Ensuite, la propriété InkEnabled du contrôle InkPicture est définie sur **false** avant la mise à jour de sa propriété Ink.

Enfin, le contrôle [InkPicture](/previous-versions/ms583740(v=vs.100)) est activé ou désactivé pour la partie de véhicule particulière selon que la case à cocher Masquer la couche est activée et que la méthode [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) du contrôle InkPicture est utilisée pour afficher uniquement les couches souhaitées dans le contrôle.


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



## <a name="closing-the-form"></a>Fermeture du formulaire

dans le code généré par le concepteur de formulaires Windows, les contrôles [InkEdit](/previous-versions/ms835842(v=msdn.10)) et [InkPicture](/previous-versions/ms583740(v=vs.100)) sont ajoutés à la liste des composants du formulaire lorsque le formulaire est initialisé. Lorsque le formulaire se ferme, les contrôles InkEdit et InkPicture sont supprimés, ainsi que les autres composants du formulaire, par la méthode [dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) du formulaire. La méthode dispose du formulaire supprime également les objets [Ink](/previous-versions/ms583670(v=vs.100)) créés pour le formulaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[Contrôle InkPicture](inkpicture-control.md)
</dt> <dt>

[InkEdit, contrôle](inkedit-control.md)
</dt> </dl>

 

 
