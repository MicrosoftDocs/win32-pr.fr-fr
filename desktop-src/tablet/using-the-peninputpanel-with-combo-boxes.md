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
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Utilisation de PenInputPanel avec des zones de liste déroulante

\[L’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a été remplacé par [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]

Si vous attachez un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) à un contrôle [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , puis que vous appuyez sur le stylet de votre tablette dans la zone de liste déroulante modifier la partie de contrôle au moment de l’exécution, l’objet PenInputPanel n’apparaît pas. Toutefois, il ne s’affiche pas si vous appuyez sur la flèche déroulante. Cela est dû au fait que la fenêtre du contrôle d’édition dans la zone de liste déroulante n’est pas la fenêtre qui reçoit les messages de stylet. Les zones de liste modifiable ont une fenêtre d’édition enfant. La solution à ce problème consiste à déterminer si la fenêtre à laquelle l’objet PenInputPanel est attaché a une fenêtre enfant. Si c’est le cas, vous pouvez attacher l’objet PenInputPanel à la fenêtre enfant.

Si vous affectez à la propriété [VerticalOffset](/previous-versions/ms571983(v=vs.100)) de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) la valeur-1, le panneau s’affiche au-dessus de la zone de liste déroulante.

 

 
