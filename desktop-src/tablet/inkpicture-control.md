---
description: Rubrique de référence sur le contrôle InkPicture pour Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Contrôle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521349"
---
# <a name="inkpicture-control"></a><span data-ttu-id="c35e2-103">Contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="c35e2-103">InkPicture Control</span></span>

<span data-ttu-id="c35e2-104">Le contrôle [InkPicture](inkpicture-control-reference.md) vous permet de placer une image (format. jpg,. bmp,. png ou. gif) dans une application à laquelle les utilisateurs peuvent ajouter de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c35e2-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="c35e2-105">Il est destiné aux scénarios dans lesquels l’encre n’a pas besoin d’être reconnue en tant que texte, mais est stockée en tant qu’encre.</span><span class="sxs-lookup"><span data-stu-id="c35e2-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="c35e2-106">Les utilisateurs ajoutent de l’encre à une couche transparente à l’aide d’un stylet.</span><span class="sxs-lookup"><span data-stu-id="c35e2-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="c35e2-107">Les utilisateurs peuvent redimensionner une fenêtre [InkPicture](inkpicture-control-reference.md) sans perdre d’informations manuscrites, même si l’encre est rognée lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="c35e2-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="c35e2-108">Le contrôle [InkPicture](inkpicture-control-reference.md) comprend la prise en charge de l’impression de base. Toutefois, il vous revient de mettre en œuvre l’aperçu avant impression ou d’autres fonctionnalités d’impression avancées.</span><span class="sxs-lookup"><span data-stu-id="c35e2-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="c35e2-109">L’implémentation managée (.NET Framework) de [InkPicture](/previous-versions/ms583740(v=vs.100)) hérite de la classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="c35e2-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="c35e2-110">Par défaut, l’encre est colorée en noir si elle n’est pas en mode de contraste élevé ; dans le cas contraire, elle est définie sur la valeur actuelle du paramètre de couleur système (COLOR \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="c35e2-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="c35e2-111">En outre, par défaut, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="c35e2-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="c35e2-112">Dans le contrôle [InkPicture](inkpicture-control-reference.md) , utilisez l’objet [**Ink**](inkdisp-class.md) pour charger et enregistrer l’encre.</span><span class="sxs-lookup"><span data-stu-id="c35e2-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="c35e2-113">Lorsque vous affectez à [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) la valeur **Delete** ou **Select**, d’autres événements (tels que l’événement [**Stroke**](inkpicture-stroke.md) ) sont déclenchés.</span><span class="sxs-lookup"><span data-stu-id="c35e2-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="c35e2-114">Ces événements sont utiles si vous souhaitez implémenter vos propres modes de suppression ou de sélection.</span><span class="sxs-lookup"><span data-stu-id="c35e2-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="c35e2-115">Pour obtenir des informations de référence détaillées sur le contrôle [InkPicture](inkpicture-control-reference.md) , consultez InkPicture.</span><span class="sxs-lookup"><span data-stu-id="c35e2-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="c35e2-116">Les sections suivantes détaillent l’utilisation du contrôle [InkPicture](inkpicture-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="c35e2-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="c35e2-117">Utilisation des images</span><span class="sxs-lookup"><span data-stu-id="c35e2-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="c35e2-118">Utilisation d’InkPicture sur des versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="c35e2-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
