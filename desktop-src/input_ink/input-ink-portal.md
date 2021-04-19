---
description: En savoir plus sur les différentes API d’entrée de bureau pour les applications Windows.
ms.assetid: 0691afb1-575a-4bb7-8fa5-006b231b8f1f
title: Entrée d’encre
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ffb67d452e3bee327195f8ff920bfcab3c0232a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521280"
---
# <a name="ink-input"></a><span data-ttu-id="99af9-103">Entrée d’encre</span><span class="sxs-lookup"><span data-stu-id="99af9-103">Ink input</span></span>

<span data-ttu-id="99af9-104">En savoir plus sur les différentes API d’entrée de bureau pour les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="99af9-104">Learn about the various Desktop inking APIs for Windows apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99af9-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="99af9-105">In this section</span></span>

| <span data-ttu-id="99af9-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="99af9-106">Topic</span></span> | <span data-ttu-id="99af9-107">Description</span><span class="sxs-lookup"><span data-stu-id="99af9-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="99af9-108">Présentateur d’encre</span><span class="sxs-lookup"><span data-stu-id="99af9-108">Ink presenter</span></span>](ink-presenter.md)<br/> | <span data-ttu-id="99af9-109">Les API de présentateur d’encre permettent aux applications Microsoft Win32 de gérer l’entrée, le traitement et le rendu des entrées manuscrites (standard et modifiées) via un objet [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) inséré dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.</span><span class="sxs-lookup"><span data-stu-id="99af9-109">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/> |
| [<span data-ttu-id="99af9-110">Convertisseur d’encre</span><span class="sxs-lookup"><span data-stu-id="99af9-110">Ink renderer</span></span>](ink-renderer.md)<br/>   | <span data-ttu-id="99af9-111">Les API de [rendu d’encre](ink-renderer.md) activent le rendu des traits d’encre dans le contexte de périphérique Direct2D désigné d’une application Windows universelle, au lieu du contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) par défaut.</span><span class="sxs-lookup"><span data-stu-id="99af9-111">The [Ink renderer](ink-renderer.md) APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span><br/>                                                                        |

## <a name="related-topics"></a><span data-ttu-id="99af9-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99af9-112">Related topics</span></span>

<span data-ttu-id="99af9-113">[Interactions de stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)de stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), exemple d’écriture manuscrite [complexe](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="99af9-113">[Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
