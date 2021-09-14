---
description: Décrit comment créer un objet PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Création d’un objet PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294658"
---
# <a name="creating-a-peninputpanel-object"></a>Création d’un objet PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) et [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)). Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]

Les constructeurs de code managé offrent un moyen pratique de créer un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) et de l’attacher à un contrôle en une seule étape. Cet \# exemple C crée un objet PenInputPanel et l’attache à un contrôle [InkEdit](/previous-versions/ms835842(v=msdn.10)) existant, `InkEdit1` , avec une ligne de code.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



le même exemple dans Visual Basic .net se présente comme suit :


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Cette technique est utile dans les cas où un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) est associé à un seul contrôle tout au long de sa durée de vie. Dans les cas où vous souhaitez utiliser un objet PenInputPanel et l’associer à plusieurs contrôles, comme illustré dans l' [exemple PenInputPanel](peninputpanel-sample.md), utilisez la propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) pour modifier le contrôle auquel l’objet PenInputPanel est associé.

Pour attacher un objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) à un contrôle sans utiliser de constructeur, utilisez la propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) . Utilisez cette technique pour les langages qui ne prennent pas en charge les constructeurs managés, tels que C++.

 

 
