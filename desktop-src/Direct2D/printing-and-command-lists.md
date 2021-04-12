---
title: Impression et listes de commandes
description: Le contrôle d’impression Direct2D \ 32 ; est un nouveau composant du module Direct2D dans Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382079"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="3823c-103">Impression et listes de commandes</span><span class="sxs-lookup"><span data-stu-id="3823c-103">Printing and command lists</span></span>

<span data-ttu-id="3823c-104">Le [](./direct2d-portal.md) [**contrôle d’impression**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D est un nouveau composant du module Direct2D dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3823c-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="3823c-105">Ce composant permet aux applications Direct2D de réutiliser leurs appels de dessin Direct2D (en termes de modifications d’État et de primitives rendu) pour fournir des résultats d’impression similaires à ceux que vous voyez à l’écran.</span><span class="sxs-lookup"><span data-stu-id="3823c-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="3823c-106">L’interface [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) représente un travail d’impression virtuel : vous pouvez créer un contrôle d’impression [Direct2D](./direct2d-portal.md) pour lancer un nouveau travail d’impression, passer le contenu Direct2D pour chaque page que vous souhaitez imprimer, puis fermer le contrôle d’impression pour terminer un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="3823c-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="3823c-107">Un contrôle d’impression est mappé à un et un seul travail d’impression, et vous ne pouvez pas le réutiliser.</span><span class="sxs-lookup"><span data-stu-id="3823c-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="3823c-108">Le contrôle d’impression [Direct2D](./direct2d-portal.md) convertit et optimise le contenu de Direct2D passé pour le sous-système d’impression, qui fonctionne avec les véritables imprimantes pour remettre l’impression réelle.</span><span class="sxs-lookup"><span data-stu-id="3823c-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="3823c-109">Tous les détails spécifiques à l’impression sont masqués dans les applications Direct2D, ce qui signifie que les applications Direct2D peuvent imprimer sans savoir quels appareils ils dessinent, ou comment les dessins sont convertis en impression.</span><span class="sxs-lookup"><span data-stu-id="3823c-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="3823c-110">Pour imprimer avec [Direct2D](./direct2d-portal.md), vous devez préparer une liste de commandes Direct2D pour chaque page que vous souhaitez imprimer, puis passer cette liste de commandes au contrôle d’impression Direct2D.</span><span class="sxs-lookup"><span data-stu-id="3823c-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="3823c-111">Pour préparer cette liste de commandes Direct2D, vous devez simplement créer et définir une liste de commandes comme cible de dessin du contexte de périphérique actuel, puis dessiner sur ce contexte de périphérique, exactement comme si vous dessiniez dans une cible bitmap pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="3823c-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="3823c-112">Pour plus d’informations sur les appareils et les cibles, consultez [contextes de périphériques et](devices-and-device-contexts.md) de périphériques.</span><span class="sxs-lookup"><span data-stu-id="3823c-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="3823c-113">Le diagramme ici illustre l’interaction entre l’application, le contexte de périphérique, la cible bitmap, la cible de la liste de commandes et le contrôle d’impression.</span><span class="sxs-lookup"><span data-stu-id="3823c-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="3823c-114">Les Sub-System d’impression Windows et les composants d’imprimante sont grisés, car ils sont complètement masqués dans les applications [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3823c-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![diagramme qui montre comment le commandlist et l’impression interagissent avec une application et Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="3823c-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="3823c-116">Example</span></span>

<span data-ttu-id="3823c-117">Le processus complet d’impression du contenu Direct2D comprend les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3823c-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="3823c-118">Créez un contrôle d’impression pour lancer un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="3823c-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="3823c-119">Ajoutez une page au contrôle d’impression en passant dans une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="3823c-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="3823c-120">Répétez l’étape 2 pour chaque page du reste du document</span><span class="sxs-lookup"><span data-stu-id="3823c-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="3823c-121">Fermez le contrôle d’impression pour terminer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="3823c-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="3823c-122">Voici un exemple de code qui illustre le processus.</span><span class="sxs-lookup"><span data-stu-id="3823c-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="3823c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3823c-123">Related topics</span></span>

[<span data-ttu-id="3823c-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="3823c-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="3823c-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="3823c-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="3823c-126">Amélioration des performances des applications Direct2D et de l’impression</span><span class="sxs-lookup"><span data-stu-id="3823c-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)