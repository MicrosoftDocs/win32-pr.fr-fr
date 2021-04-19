---
description: Les API de rendu d’encre activent le rendu des traits d’encre dans le contexte de périphérique Direct2D désigné d’une application Windows universelle, au lieu du contrôle InkCanvas par défaut.
ms.assetid: 8E532066-19EB-4FA6-823D-21823591742F
title: Convertisseur d’encre
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f9e1e654859dd8d777855bc2bffaf953feb8ba8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525011"
---
# <a name="ink-renderer"></a><span data-ttu-id="b8088-103">Convertisseur d’encre</span><span class="sxs-lookup"><span data-stu-id="b8088-103">Ink renderer</span></span>

<span data-ttu-id="b8088-104">Les API de rendu d’encre activent le rendu des traits d’encre dans le contexte de périphérique Direct2D désigné d’une application Windows universelle, au lieu du contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8088-104">The Ink renderer APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

<span data-ttu-id="b8088-105">Le convertisseur d’encre est conçu pour être utilisé par les développeurs d’applications Windows universelles qui souhaitent personnaliser la manière dont les traits d’encre sont rendus « secs » et de qualité identique au contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) .</span><span class="sxs-lookup"><span data-stu-id="b8088-105">Ink renderer is designed for use by Universal Windows app developers interested in customizing how ink strokes are rendered "dry", and of identical quality to the [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b8088-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b8088-106">In this section</span></span>

| <span data-ttu-id="b8088-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b8088-107">Topic</span></span>                                                             | <span data-ttu-id="b8088-108">Description</span><span class="sxs-lookup"><span data-stu-id="b8088-108">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8088-109">Classes de convertisseur d’encre</span><span class="sxs-lookup"><span data-stu-id="b8088-109">Ink renderer classes</span></span>](ink-renderer-classes.md)<br/>       | <span data-ttu-id="b8088-110">Les rubriques contenues dans cette section fournissent les spécifications de référence pour les classes de convertisseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="b8088-110">The topics contained in this section provide the reference specifications for Ink renderer classes.</span></span> <br/>    |
| [<span data-ttu-id="b8088-111">Interfaces de convertisseur d’encre</span><span class="sxs-lookup"><span data-stu-id="b8088-111">Ink renderer interfaces</span></span>](ink-renderer-interfaces.md)<br/> | <span data-ttu-id="b8088-112">Les rubriques contenues dans cette section fournissent les spécifications de référence pour les interfaces de convertisseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="b8088-112">The topics contained in this section provide the reference specifications for Ink renderer interfaces.</span></span> <br/> |

## <a name="related-topics"></a><span data-ttu-id="b8088-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8088-113">Related topics</span></span>

<span data-ttu-id="b8088-114">[Entrée manuscrite](input-ink-portal.md), [interactions de stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)de stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe</span><span class="sxs-lookup"><span data-stu-id="b8088-114">[Ink input](input-ink-portal.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
