---
description: Dans cet \# exemple C, un formulaire papier a été analysé en tant que fichier png (Portable Network Graphics) et spécifié comme image d’arrière-plan au moment de l’exécution pour un contrôle InkPicture. L’exemple utilise une boîte de message pour afficher les résultats de la reconnaissance de l’écriture manuscrite.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Exemple de formulaire papier numérisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525289"
---
# <a name="scanned-paper-form-sample"></a>Exemple de formulaire papier numérisé

Dans cet \# exemple C, un formulaire papier a été analysé en tant que fichier png (Portable Network Graphics) et spécifié comme image d’arrière-plan au moment de l’exécution pour un contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) . L’exemple utilise une boîte de message pour afficher les résultats de la reconnaissance de l’écriture manuscrite.

L’exemple comprend un fichier Extensible Markup Language (XML), Formdata.xml. Le fichier XML contient le nom du fichier PNG. Il contient également `FieldInfo` des éléments qui définissent des zones rectangulaires sur le formulaire où un utilisateur peut entrer de l’encre. Les informations contenues dans l' `FieldInfo` élément sont affichées dans l’exemple suivant :


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Les éléments gauche, supérieur, droit et bas sont des définitions de coordonnées en pixels pour chaque champ.

L’exemple Initialise un nouveau [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) avec les données contenues dans Formdata.xml :


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



L’image de formulaire spécifiée dans Formdata.xml est chargée comme arrière-plan du contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



La collecte d’encre est ensuite activée pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Gestionnaires d’événements de menu

L’application comprend des gestionnaires d’événements Click pour tous les menus affichés en haut du formulaire.

### <a name="recognize-menu-item"></a>Recognize (élément de menu)

Le gestionnaire d’événements de clic de menu Recognize désactive la collecte d’encre pour le contrôle et recherche un module de reconnaissance de l’écriture manuscrite. Si aucun module de reconnaissance n’est installé, une boîte de dialogue s’affiche. Un utilisateur doit ensuite cliquer sur l’option de menu encre ou stylet pour réactiver le contrôle pour l’entrée d’encre.

Si un module de reconnaissance est installé, la `Recognize` fonction récupère les données XML qui spécifient des coordonnées en pixels pour chaque champ de formulaire. Les coordonnées sont converties en coordonnées d’espace d’encre et un rectangle est défini pour chaque champ de formulaire. Une fois les rectangles définis, la fonction recherche les traits qui se croisent et se trouvent dans chaque rectangle. Enfin, il effectue la reconnaissance de l’encre et affiche les résultats dans une boîte de message.

### <a name="ink-menu-item"></a>Élément de menu encre

Le gestionnaire d’événements de clic de menu Ink active le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) .

### <a name="pen-menu-item"></a>Élément de menu PEN

Le gestionnaire d’événements Click du menu PEN effectue les tâches suivantes :

-   Désactive la collecte d’encres pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) (ce qui est nécessaire avant de modifier la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) ).
-   Définit la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) pour collecter l’encre.
-   Réactive la collection d’encres pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) et bascule les menus stylet, sélectionner et gomme pour indiquer le mode actif.

### <a name="edit-menu-item"></a>Modifier l’élément de menu

Le gestionnaire d’événements de clic du menu Edition est semblable au gestionnaire d’événements du menu de stylet. Il effectue les tâches suivantes :

-   Désactive la collecte d’encres.
-   Définit la propriété [EditingMode](/previous-versions/ms582189(v=vs.100)) sur **Select**, ce qui permet à l’utilisateur d’effectuer une sélection d’entrée manuscrite.
-   Réactive la collecte d’encre et active les menus stylet, modifier et gomme pour indiquer le mode actif.

### <a name="eraser-menu-item"></a>Élément de menu de la gomme

Le gestionnaire d’événements de clic du menu gomme définit le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) sur **Delete**, ce qui permet à un utilisateur d’effacer l’encre. Il bascule également les éléments de menu stylet, modifier et gomme.

### <a name="clear-menu-item"></a>Effacer l’élément de menu

Le gestionnaire d’événements de clic de menu effacer supprime la collection de [traits](/previous-versions/ms552701(v=vs.100)) active pour le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) , effaçant ainsi toute l’encre du formulaire.

## <a name="closing-the-form"></a>Fermeture du formulaire

dans le code généré par le concepteur de formulaires Windows, le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) est ajouté à la liste des composants du formulaire lorsque le formulaire est initialisé. Lorsque le formulaire se ferme, le contrôle InkPicture est supprimé, ainsi que les autres composants du formulaire, par la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[InkEdit, contrôle](inkedit-control.md)
</dt> <dt>

[Contrôle InkPicture](inkpicture-control.md)
</dt> </dl>

 

 
