---
description: Décrit comment créer un objet PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Création d’un objet PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513954"
---
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="6ddb7-103">Création d’un objet PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="6ddb7-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="6ddb7-104">\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) et [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="6ddb7-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="6ddb7-105">Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="6ddb7-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="6ddb7-106">Les constructeurs de code managé offrent un moyen pratique de créer un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) et de l’attacher à un contrôle en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="6ddb7-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="6ddb7-107">Cet \# exemple C crée un objet PenInputPanel et l’attache à un contrôle [InkEdit](/previous-versions/ms835842(v=msdn.10)) existant, `InkEdit1` , avec une ligne de code.</span><span class="sxs-lookup"><span data-stu-id="6ddb7-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="6ddb7-108">Le même exemple dans Visual Basic .NET se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="6ddb7-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="6ddb7-109">Cette technique est utile dans les cas où un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) est associé à un seul contrôle tout au long de sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="6ddb7-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="6ddb7-110">Dans les cas où vous souhaitez utiliser un objet PenInputPanel et l’associer à plusieurs contrôles, comme illustré dans l' [exemple PenInputPanel](peninputpanel-sample.md), utilisez la propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) pour modifier le contrôle auquel l’objet PenInputPanel est associé.</span><span class="sxs-lookup"><span data-stu-id="6ddb7-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="6ddb7-111">Pour attacher un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) à un contrôle sans utiliser de constructeur, utilisez la propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="6ddb7-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="6ddb7-112">Utilisez cette technique pour les langages qui ne prennent pas en charge les constructeurs managés, tels que C++.</span><span class="sxs-lookup"><span data-stu-id="6ddb7-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 
