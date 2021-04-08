---
description: Décrit l’utilisation de l’objet PenInputPanel avec des zones de liste déroulante.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Utilisation de PenInputPanel avec des zones de liste déroulante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751261"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="fda6c-103">Utilisation de PenInputPanel avec des zones de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="fda6c-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="fda6c-104">\[L’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a été remplacé par [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="fda6c-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="fda6c-105">Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="fda6c-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="fda6c-106">Si vous attachez un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) à un contrôle [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , puis que vous appuyez sur le stylet de votre tablette dans la zone de liste déroulante modifier la partie de contrôle au moment de l’exécution, l’objet PenInputPanel n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="fda6c-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="fda6c-107">Toutefois, il ne s’affiche pas si vous appuyez sur la flèche déroulante.</span><span class="sxs-lookup"><span data-stu-id="fda6c-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="fda6c-108">Cela est dû au fait que la fenêtre du contrôle d’édition dans la zone de liste déroulante n’est pas la fenêtre qui reçoit les messages de stylet.</span><span class="sxs-lookup"><span data-stu-id="fda6c-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="fda6c-109">Les zones de liste modifiable ont une fenêtre d’édition enfant.</span><span class="sxs-lookup"><span data-stu-id="fda6c-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="fda6c-110">La solution à ce problème consiste à déterminer si la fenêtre à laquelle l’objet PenInputPanel est attaché a une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="fda6c-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="fda6c-111">Si c’est le cas, vous pouvez attacher l’objet PenInputPanel à la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="fda6c-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="fda6c-112">Si vous affectez à la propriété [VerticalOffset](/previous-versions/ms571983(v=vs.100)) de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) la valeur-1, le panneau s’affiche au-dessus de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="fda6c-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 
