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
# <a name="working-with-pictures"></a>Utilisation des images

Cette rubrique explique comment ajuster des images à l’aide de la propriété [System. Windows. Forms. PictureBox. ModeAffichage](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) et comment afficher des images dans Microsoft Visual Studio .net.

## <a name="the-sizemode-property"></a>La propriété ModeAffichage

Vous pouvez spécifier la façon dont une image s’ajuste au contrôle avec la propriété [ModeAffichage](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) . La propriété ModeAffichage est disponible à la fois dans la bibliothèque managée et dans la bibliothèque Automation. Avec la fonction ModeAffichage, vous pouvez :

-   Redimensionnez les bordures du contrôle pour ajuster une image.
-   Étirez une image pour l’ajuster aux bordures du contrôle.
-   Centrer une image à l’intérieur des bordures de contrôle.
-   Ancrez une image dans la zone supérieure gauche du contrôle sans redimensionner l’image ou le contrôle (une partie de l’image risque de ne pas être visible si vous ne redimensionnez pas l’image ou le contrôle).

## <a name="working-with-pictures-in-visual-studio-net"></a>Utilisation d’images dans Visual Studio .NET

Pour afficher une image au moment du design dans Visual Studio .NET :

1.  Faites glisser un contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) sur un formulaire ou double-cliquez sur le contrôle InkPicture dans la boîte à outils.
2.  Dans la fenêtre **Propriétés** , sélectionnez la propriété **image** , puis cliquez sur le bouton de sélection pour ouvrir la boîte de dialogue **ouvrir** .
3.  Si vous recherchez un type de fichier spécifique (par exemple, fichiers. jpg), sélectionnez-le dans la zone **types de fichiers** .
4.  Sélectionnez le fichier que vous souhaitez afficher.

Pour effacer l’image au moment de la conception :

1.  Dans la fenêtre **Propriétés** , sélectionnez la propriété **image** et cliquez avec le bouton droit sur l’image miniature.
2.  Cliquez sur **Réinitialiser**.

Le contrôle [InkPicture](/previous-versions/aa514604(v=msdn.10)) est affiché par défaut sans bordure. Vous pouvez fournir une bordure standard ou à trois dimensions à l’aide de la propriété [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) pour distinguer la zone InkPicture du reste du formulaire, même si elle ne contient pas d’image.

Vous pouvez afficher une image au moment de l’exécution avec la méthode [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) de l’objet [System. Drawing. image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



Vous pouvez également inclure une image d’arrière-plan avec la propriété [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) de l’objet [image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) hérité. Toutefois, cette image ne peut pas être redimensionnée.

 

 
