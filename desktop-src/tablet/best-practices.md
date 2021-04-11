---
description: Vue d’ensemble des meilleures pratiques lors de l’utilisation de l’objet panneau de saisie Pen.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Meilleures pratiques (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210828"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="c35c9-103">Meilleures pratiques (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="c35c9-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="c35c9-104">Voici quelques recommandations à prendre en compte lors de l’utilisation de l’objet [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c35c9-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="c35c9-105">Préférer le contrôle InkEdit</span><span class="sxs-lookup"><span data-stu-id="c35c9-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="c35c9-106">Désactiver le mode Ink sur les contrôles InkEdit</span><span class="sxs-lookup"><span data-stu-id="c35c9-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="c35c9-107">Utilisation des contrôles sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="c35c9-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="c35c9-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c35c9-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="c35c9-109">Préférer le contrôle InkEdit</span><span class="sxs-lookup"><span data-stu-id="c35c9-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="c35c9-110">[InkEdit](inkedit-control-reference.md) est le contrôle par défaut auquel attacher l’objet [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c35c9-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="c35c9-111">Le contrôle InkEdit fournit la prise en charge de [Text Services Framework (TSF)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="c35c9-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="c35c9-112">Désactiver le mode Ink sur les contrôles InkEdit</span><span class="sxs-lookup"><span data-stu-id="c35c9-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="c35c9-113">Lorsqu’il est attaché à un contrôle [InkEdit](inkedit-control-reference.md) , affectez à la propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) du contrôle InkEdit la valeur [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) .</span><span class="sxs-lookup"><span data-stu-id="c35c9-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="c35c9-114">Si la propriété **InkMode** n’est pas définie sur la valeur **InkMode** , le contrôle InkEdit interprète le premier TAP comme un trait, le transmet au module de reconnaissance et insère le texte dans le contrôle InkEdit.</span><span class="sxs-lookup"><span data-stu-id="c35c9-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="c35c9-115">Étant donné que vous avez déjà un objet [**PenInputPanel**](peninputpanel-class.md) joint pour accepter l’entrée manuscrite, il n’est pas nécessaire que le contrôle InkEdit soit également activé pour l’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="c35c9-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="c35c9-116">Utilisation des contrôles sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="c35c9-116">Using Windowless Controls</span></span>

<span data-ttu-id="c35c9-117">Lorsqu’un objet [**PenInputPanel**](peninputpanel-class.md) est attaché à une fenêtre parente qui contient plus d’un contrôle sans fenêtre, l’objet **PenInputPanel** ne sait pas comment suivre le signe insertion lorsque le focus se déplace entre des enfants sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c35c9-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="c35c9-118">Une entrée d’écriture manuscrite peut être envoyée à un enfant incorrect lorsque le focus passe d’un contrôle sans fenêtre à un autre alors que l’entrée est en attente.</span><span class="sxs-lookup"><span data-stu-id="c35c9-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="c35c9-119">Pour utiliser l’objet [**PenInputPanel**](peninputpanel-class.md) dans un environnement sans fenêtre, vous pouvez utiliser la technique suivante :</span><span class="sxs-lookup"><span data-stu-id="c35c9-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="c35c9-120">Instanciez un contrôle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) et positionnez-le sur le contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c35c9-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="c35c9-121">Attachez l’objet [**PenInputPanel**](peninputpanel-class.md) au nouveau contrôle zone de texte.</span><span class="sxs-lookup"><span data-stu-id="c35c9-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="c35c9-122">Laissez le contrôle de zone de texte collecter le texte reconnu à partir de l’objet [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c35c9-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="c35c9-123">Lorsque le focus est modifié en dehors du contrôle Text Box, appelez la méthode [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) de l’objet [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c35c9-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="c35c9-124">Copiez le texte reconnu à partir du contrôle zone de texte dans l’enfant sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c35c9-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="c35c9-125">Détachez l’objet [**PenInputPanel**](peninputpanel-class.md) en affectant à sa propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (code managé uniquement) ou à la propriété [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c35c9-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="c35c9-126">Détruisez le contrôle Text Box.</span><span class="sxs-lookup"><span data-stu-id="c35c9-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c35c9-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c35c9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c35c9-128">**PenInputPanel, classe**</span><span class="sxs-lookup"><span data-stu-id="c35c9-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="c35c9-129">[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c35c9-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="c35c9-130">Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="c35c9-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
