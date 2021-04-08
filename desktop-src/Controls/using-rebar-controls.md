---
title: Utilisation des contrôles Rebar
description: Cette section contient des rubriques qui montrent comment créer et utiliser des contrôles Rebar.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730508"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="b952b-103">Utilisation des contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="b952b-103">Using Rebar Controls</span></span>

<span data-ttu-id="b952b-104">Cette section contient des rubriques qui montrent comment créer et utiliser des contrôles Rebar.</span><span class="sxs-lookup"><span data-stu-id="b952b-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b952b-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b952b-105">In this section</span></span>



| <span data-ttu-id="b952b-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b952b-106">Topic</span></span>                                                                | <span data-ttu-id="b952b-107">Description</span><span class="sxs-lookup"><span data-stu-id="b952b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b952b-108">Comment créer des contrôles Rebar</span><span class="sxs-lookup"><span data-stu-id="b952b-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="b952b-109">Une application crée un contrôle rebar en appelant la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant [**REBARCLASSNAME**](common-control-window-classes.md) comme classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b952b-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="b952b-110">L’application doit tout d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant le \_ bit des classes cool ICC \_ dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="b952b-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

