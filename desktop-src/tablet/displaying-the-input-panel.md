---
description: Vue d’ensemble de l’affichage du panneau de saisie.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Affichage du panneau de saisie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535640"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="bbf5b-103">Affichage du panneau de saisie</span><span class="sxs-lookup"><span data-stu-id="bbf5b-103">Displaying the Input Panel</span></span>

<span data-ttu-id="bbf5b-104">\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) pour le code managé).</span><span class="sxs-lookup"><span data-stu-id="bbf5b-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="bbf5b-105">Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="bbf5b-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="bbf5b-106">L’ordre des différents événements de focus pour un contrôle se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="bbf5b-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="bbf5b-107">Control. Enter</span><span class="sxs-lookup"><span data-stu-id="bbf5b-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="bbf5b-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="bbf5b-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="bbf5b-109">Control. Leave</span><span class="sxs-lookup"><span data-stu-id="bbf5b-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="bbf5b-110">Contrôle. validation</span><span class="sxs-lookup"><span data-stu-id="bbf5b-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="bbf5b-111">Control. Validated</span><span class="sxs-lookup"><span data-stu-id="bbf5b-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="bbf5b-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="bbf5b-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="bbf5b-113">Il n’y a aucune garantie que le contrôle a réellement le focus au moment où la propriété [Control. visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) est écrite lorsqu’elle est définie dans le gestionnaire d’événements [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="bbf5b-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="bbf5b-114">L’événement Control. Enter est le meilleur emplacement pour attacher l’objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) à un contrôle, mais l’événement [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) est le meilleur emplacement pour modifier la propriété [PenInputPanel. visible](/previous-versions/ms571984(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bbf5b-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
