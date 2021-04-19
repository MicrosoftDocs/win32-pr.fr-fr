---
description: Cette rubrique explique comment ajuster des images à l’aide de la propriété System. Windows. Forms. PictureBox. ModeAffichage et comment afficher des images dans Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Utilisation des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518541"
---
# <a name="working-with-pictures"></a><span data-ttu-id="fefbc-103">Utilisation des images</span><span class="sxs-lookup"><span data-stu-id="fefbc-103">Working with Pictures</span></span>

<span data-ttu-id="fefbc-104">Cette rubrique explique comment ajuster des images à l’aide de la propriété [System. Windows. Forms. PictureBox. ModeAffichage](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) et comment afficher des images dans Microsoft Visual Studio .net.</span><span class="sxs-lookup"><span data-stu-id="fefbc-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="fefbc-105">La propriété ModeAffichage</span><span class="sxs-lookup"><span data-stu-id="fefbc-105">The SizeMode Property</span></span>

<span data-ttu-id="fefbc-106">Vous pouvez spécifier la façon dont une image s’ajuste au contrôle avec la propriété [ModeAffichage](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="fefbc-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="fefbc-107">La propriété ModeAffichage est disponible à la fois dans la bibliothèque managée et dans la bibliothèque Automation.</span><span class="sxs-lookup"><span data-stu-id="fefbc-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="fefbc-108">Avec la fonction ModeAffichage, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="fefbc-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="fefbc-109">Redimensionnez les bordures du contrôle pour ajuster une image.</span><span class="sxs-lookup"><span data-stu-id="fefbc-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="fefbc-110">Étirez une image pour l’ajuster aux bordures du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fefbc-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="fefbc-111">Centrer une image à l’intérieur des bordures de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fefbc-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="fefbc-112">Ancrez une image dans la zone supérieure gauche du contrôle sans redimensionner l’image ou le contrôle (une partie de l’image risque de ne pas être visible si vous ne redimensionnez pas l’image ou le contrôle).</span><span class="sxs-lookup"><span data-stu-id="fefbc-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="fefbc-113">Utilisation d’images dans Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="fefbc-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="fefbc-114">Pour afficher une image au moment du design dans Visual Studio .NET :</span><span class="sxs-lookup"><span data-stu-id="fefbc-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="fefbc-115">Faites glisser un contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) sur un formulaire ou double-cliquez sur le contrôle InkPicture dans la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="fefbc-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="fefbc-116">Dans la fenêtre **Propriétés** , sélectionnez la propriété **image** , puis cliquez sur le bouton de sélection pour ouvrir la boîte de dialogue **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="fefbc-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="fefbc-117">Si vous recherchez un type de fichier spécifique (par exemple, fichiers. jpg), sélectionnez-le dans la zone **types de fichiers** .</span><span class="sxs-lookup"><span data-stu-id="fefbc-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="fefbc-118">Sélectionnez le fichier que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="fefbc-118">Select the file you want to display.</span></span>

<span data-ttu-id="fefbc-119">Pour effacer l’image au moment de la conception :</span><span class="sxs-lookup"><span data-stu-id="fefbc-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="fefbc-120">Dans la fenêtre **Propriétés** , sélectionnez la propriété **image** et cliquez avec le bouton droit sur l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="fefbc-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="fefbc-121">Cliquez sur **Réinitialiser**.</span><span class="sxs-lookup"><span data-stu-id="fefbc-121">Click **Reset**.</span></span>

<span data-ttu-id="fefbc-122">Le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) est affiché par défaut sans bordure.</span><span class="sxs-lookup"><span data-stu-id="fefbc-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="fefbc-123">Vous pouvez fournir une bordure standard ou à trois dimensions à l’aide de la propriété [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) pour distinguer la zone InkPicture du reste du formulaire, même si elle ne contient pas d’image.</span><span class="sxs-lookup"><span data-stu-id="fefbc-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="fefbc-124">Vous pouvez afficher une image au moment de l’exécution avec la méthode [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) de l’objet [System. Drawing. image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :</span><span class="sxs-lookup"><span data-stu-id="fefbc-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="fefbc-125">Vous pouvez également inclure une image d’arrière-plan avec la propriété [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) de l’objet [image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) hérité. Toutefois, cette image ne peut pas être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="fefbc-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
