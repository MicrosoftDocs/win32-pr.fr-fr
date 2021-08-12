---
description: Rubrique de référence sur le contrôle InkPicture pour Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Contrôle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451098"
---
# <a name="inkpicture-control"></a>Contrôle InkPicture

Le contrôle [InkPicture](inkpicture-control-reference.md) vous permet de placer une image (format .jpg, .bmp, .png ou .gif) dans une application à laquelle les utilisateurs peuvent ajouter de l’encre. Il est destiné aux scénarios dans lesquels l’encre n’a pas besoin d’être reconnue en tant que texte, mais est stockée en tant qu’encre.

Les utilisateurs ajoutent de l’encre à une couche transparente à l’aide d’un stylet. Les utilisateurs peuvent redimensionner une fenêtre [InkPicture](inkpicture-control-reference.md) sans perdre d’informations manuscrites, même si l’encre est rognée lors du redimensionnement.

Le contrôle [InkPicture](inkpicture-control-reference.md) comprend la prise en charge de l’impression de base. Toutefois, il vous revient de mettre en œuvre l’aperçu avant impression ou d’autres fonctionnalités d’impression avancées.

l’implémentation managée (.NET Framework) de [InkPicture](/previous-versions/ms583740(v=vs.100)) hérite de la classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .

Par défaut, l’encre est colorée en noir si elle n’est pas en mode de contraste élevé ; dans le cas contraire, elle est définie sur la valeur actuelle du paramètre de couleur système (COLOR \_ WINDOWTEXT). En outre, par défaut, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) a la **valeur false**.

Dans le contrôle [InkPicture](inkpicture-control-reference.md) , utilisez l’objet [**Ink**](inkdisp-class.md) pour charger et enregistrer l’encre.

> [!Note]  
> Lorsque vous affectez à [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) la valeur **Delete** ou **Select**, d’autres événements (tels que l’événement [**Stroke**](inkpicture-stroke.md) ) sont déclenchés. Ces événements sont utiles si vous souhaitez implémenter vos propres modes de suppression ou de sélection.

 

Pour obtenir des informations de référence détaillées sur le contrôle [InkPicture](inkpicture-control-reference.md) , consultez InkPicture.

Les sections suivantes détaillent l’utilisation du contrôle [InkPicture](inkpicture-control-reference.md) :

-   [Utilisation des images](working-with-pictures.md)
-   [Utilisation d’InkPicture sur des versions antérieures de Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
