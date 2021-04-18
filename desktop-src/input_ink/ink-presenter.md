---
description: Les API d’affichage d’entrées manuscrites permettent aux applications Win32 de gérer les entrées, le traitement et le rendu des entrées manuscrites (standard ou personnalisées), par le biais d’un objet InkPresenter inséré dans l’arborescence virtuelle DirectComposition de l’application.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Présentateur d’encre
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203876"
---
# <a name="ink-presenter"></a><span data-ttu-id="c0171-103">Présentateur d’encre</span><span class="sxs-lookup"><span data-stu-id="c0171-103">Ink presenter</span></span>

<span data-ttu-id="c0171-104">Les API de présentateur d’encre permettent aux applications Microsoft Win32 de gérer l’entrée, le traitement et le rendu des entrées manuscrites (standard et modifiées) via un objet [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inséré dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.</span><span class="sxs-lookup"><span data-stu-id="c0171-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="c0171-105">L’entrée d’encre standard (info-bulle ou bouton de gomme) n’est pas modifiée à l’aide d’une offre secondaire, telle qu’un bouton de stylet, un bouton droit de la souris ou similaire.</span><span class="sxs-lookup"><span data-stu-id="c0171-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="c0171-106">Les applications plateforme Windows universelle (UWP) utilisant Extensible Application Markup Language (XAML) fournissent cette fonctionnalité via un contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) avec un objet [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) qui se connecte à l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) XAML.</span><span class="sxs-lookup"><span data-stu-id="c0171-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="c0171-107">Pour plus d’informations, consultez [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet.</span><span class="sxs-lookup"><span data-stu-id="c0171-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="c0171-108">Le [convertisseur d’encre](ink-renderer.md) est conçu pour être utilisé par les développeurs d’applications Windows universelles qui souhaitent fournir des fonctionnalités d’InkPresenter [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)basés sur XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) dans les applications Win32 natives.</span><span class="sxs-lookup"><span data-stu-id="c0171-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c0171-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c0171-109">In this section</span></span>



| <span data-ttu-id="c0171-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c0171-110">Topic</span></span>                                                               | <span data-ttu-id="c0171-111">Description</span><span class="sxs-lookup"><span data-stu-id="c0171-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0171-112">Classes de présentateur d’encre</span><span class="sxs-lookup"><span data-stu-id="c0171-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="c0171-113">Les rubriques contenues dans cette section fournissent les spécifications de référence pour les classes de présentateur d’encre.</span><span class="sxs-lookup"><span data-stu-id="c0171-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="c0171-114">Interfaces de présentateur d’encre</span><span class="sxs-lookup"><span data-stu-id="c0171-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="c0171-115">Les rubriques contenues dans cette section fournissent les spécifications de référence pour les interfaces de présentateur d’encre.</span><span class="sxs-lookup"><span data-stu-id="c0171-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c0171-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0171-116">Related topics</span></span>

<span data-ttu-id="c0171-117">[Présentation](ink-presenter.md)de l’encre, [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe</span><span class="sxs-lookup"><span data-stu-id="c0171-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
