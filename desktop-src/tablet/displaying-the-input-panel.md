---
description: Vue d’ensemble de l’affichage du panneau de saisie.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Affichage du panneau de saisie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940789"
---
# <a name="displaying-the-input-panel"></a>Affichage du panneau de saisie

\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) pour le code managé). Reportez-vous à la [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]

L’ordre des différents événements de focus pour un contrôle se présente comme suit :

-   [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Contrôle. validation](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control. Validated](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Il n’y a aucune garantie que le contrôle a réellement le focus au moment où la propriété [Control. visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) est écrite lorsqu’elle est définie dans le gestionnaire d’événements [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) . L’événement Control. Enter est le meilleur emplacement pour attacher l’objet [PenInputPanel](/previous-versions/ms583923(v=vs.100)) à un contrôle, mais l’événement [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) est le meilleur emplacement pour modifier la propriété [PenInputPanel. visible](/previous-versions/ms571984(v=vs.100)) .

 

 
