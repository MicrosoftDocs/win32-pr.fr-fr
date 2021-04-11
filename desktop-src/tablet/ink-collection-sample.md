---
description: Cette application est basée sur l’objet InkCollector et montre la collection d’encres.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Exemple de collection Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112879"
---
# <a name="ink-collection-sample"></a><span data-ttu-id="28697-103">Exemple de collection Ink</span><span class="sxs-lookup"><span data-stu-id="28697-103">Ink Collection Sample</span></span>

<span data-ttu-id="28697-104">Cette application est basée sur l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) et montre la collection d’encres.</span><span class="sxs-lookup"><span data-stu-id="28697-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="28697-105">L’application crée une fenêtre, y attache un objet InkCollector et fournit à l’utilisateur des options de menu qui peuvent être utilisées pour modifier la couleur de l’encre, la largeur de l’encre, et activer et désactiver la collecte d’encres.</span><span class="sxs-lookup"><span data-stu-id="28697-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="28697-106">La version décrite dans cette section est Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="28697-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="28697-107">Les concepts sont les mêmes entre les différentes versions linguistiques de la bibliothèque d’exemples.</span><span class="sxs-lookup"><span data-stu-id="28697-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="28697-108">Déclaration de l’InkCollector</span><span class="sxs-lookup"><span data-stu-id="28697-108">Declaring the InkCollector</span></span>

<span data-ttu-id="28697-109">L’application importe d’abord l’espace de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28697-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="28697-110">Ensuite, l’application déclare `myInkCollector` , qui contient l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="28697-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="28697-111">Configuration des éléments</span><span class="sxs-lookup"><span data-stu-id="28697-111">Setting Things Up</span></span>

<span data-ttu-id="28697-112">La méthode du formulaire `InkCollection_Load` gère l’événement de [chargement](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="28697-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="28697-113">Elle crée un objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) affecté au formulaire modifie la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet InkCollector et active l’objet InkCollector.</span><span class="sxs-lookup"><span data-stu-id="28697-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


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



<span data-ttu-id="28697-114">Le [InkCollector](/previous-versions/ms836493(v=msdn.10)) est assigné à la fenêtre du formulaire en affectant le handle de fenêtre du formulaire à la propriété de [handle](/previous-versions/ms836504(v=msdn.10)) de l’objet InkCollector.</span><span class="sxs-lookup"><span data-stu-id="28697-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="28697-115">La collecte d’encre est activée en affectant la **valeur true** à la propriété [Enabled](/previous-versions/ms836503(v=msdn.10)) de l’objet InkCollector.</span><span class="sxs-lookup"><span data-stu-id="28697-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="28697-116">La propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) définit les attributs par défaut assignés à un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="28697-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="28697-117">Pour définir différents attributs sur un nouveau curseur, utilisez la propriété [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) de l’objet [Cursor](/previous-versions/ms839521(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28697-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="28697-118">Pour modifier les attributs de dessin d’un seul trait, utilisez la propriété [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28697-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="28697-119">Modification des propriétés</span><span class="sxs-lookup"><span data-stu-id="28697-119">Changing the Properties</span></span>

<span data-ttu-id="28697-120">Le reste de cette application simple se compose de gestionnaires pour les différentes sélections de menu que l’utilisateur peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="28697-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="28697-121">Par exemple, quand l’utilisateur choisit de changer la couleur de l’encre en rouge en sélectionnant rouge dans le menu Ink, la couleur est modifiée à l’aide de la propriété [Color](/previous-versions/ms837933(v=msdn.10)) sur la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) dans le gestionnaire d’événements du menu.</span><span class="sxs-lookup"><span data-stu-id="28697-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="28697-122">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="28697-122">Closing the Form</span></span>

<span data-ttu-id="28697-123">La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="28697-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
