---
description: Cette application est basée sur l’objet InkCollector et montre la collection d’encres.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Exemple de collection Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718258"
---
# <a name="ink-collection-sample"></a>Exemple de collection Ink

Cette application est basée sur l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) et montre la collection d’encres. L’application crée une fenêtre, y attache un objet InkCollector et fournit à l’utilisateur des options de menu qui peuvent être utilisées pour modifier la couleur de l’encre, la largeur de l’encre, et activer et désactiver la collecte d’encres.

> [!Note]  
> la version décrite dans cette section est Visual Basic .net. Les concepts sont les mêmes entre les différentes versions linguistiques de la bibliothèque d’exemples.

 

## <a name="declaring-the-inkcollector"></a>Déclaration de l’InkCollector

L’application importe d’abord l’espace de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) . Ensuite, l’application déclare `myInkCollector` , qui contient l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) pour le formulaire.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Configuration des éléments

La méthode du formulaire `InkCollection_Load` gère l’événement de [chargement](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire. Elle crée un objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) affecté au formulaire modifie la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet InkCollector et active l’objet InkCollector.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



Le [InkCollector](/previous-versions/ms836493(v=msdn.10)) est assigné à la fenêtre du formulaire en affectant le handle de fenêtre du formulaire à la propriété de [handle](/previous-versions/ms836504(v=msdn.10)) de l’objet InkCollector. La collecte d’encre est activée en affectant la **valeur true** à la propriété [Enabled](/previous-versions/ms836503(v=msdn.10)) de l’objet InkCollector.

La propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) définit les attributs par défaut assignés à un nouveau curseur. Pour définir différents attributs sur un nouveau curseur, utilisez la propriété [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) de l’objet [Cursor](/previous-versions/ms839521(v=msdn.10)) . Pour modifier les attributs de dessin d’un seul trait, utilisez la propriété [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) .

## <a name="changing-the-properties"></a>Modification des propriétés

Le reste de cette application simple se compose de gestionnaires pour les différentes sélections de menu que l’utilisateur peut effectuer. Par exemple, quand l’utilisateur choisit de changer la couleur de l’encre en rouge en sélectionnant rouge dans le menu Ink, la couleur est modifiée à l’aide de la propriété [Color](/previous-versions/ms837933(v=msdn.10)) sur la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) dans le gestionnaire d’événements du menu.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
