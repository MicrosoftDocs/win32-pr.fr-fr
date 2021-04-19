---
description: Vue d’ensemble de l’infrastructure de services de texte pour Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Text Services Framework (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523677"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="4993f-103">Text Services Framework (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="4993f-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="4993f-104">Lorsque [Text Services Framework (TSF)](../tsf/text-services-framework.md) est activé sur un contrôle avec un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) joint, l’objet PenInputPanel peut insérer du texte directement.</span><span class="sxs-lookup"><span data-stu-id="4993f-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="4993f-105">Si le contrôle ne prend pas en charge Text Services Framework (TSF), l’objet PenInputPanel doit recourir à l’utilisation de la [fonction SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) pour insérer du texte.</span><span class="sxs-lookup"><span data-stu-id="4993f-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="4993f-106">La possibilité d’insérer directement du texte devient très importante pour les caractères d’Extrême-Orient, où l’utilisation de la [fonction SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) peut produire des caractères incorrects.</span><span class="sxs-lookup"><span data-stu-id="4993f-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="4993f-107">TSF fournit une interface permettant de corriger les erreurs de reconnaissance, ce qui permet à l’utilisateur final de corriger, de réécrire ou même de dicter le texte approprié.</span><span class="sxs-lookup"><span data-stu-id="4993f-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="4993f-108">TSF est activé en appelant la méthode [EnableTsf](/previous-versions/ms569656(v=vs.100)) avec le paramètre *Enable* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="4993f-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="4993f-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="4993f-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="4993f-110">Un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) attaché à un contrôle [InkEdit](/previous-versions/ms552265(v=vs.100)) offre une expérience utilisateur robuste, car INKEDIT prend en charge TSF.</span><span class="sxs-lookup"><span data-stu-id="4993f-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="4993f-111">Toutefois, veillez à définir la propriété [InkMode](/previous-versions/ms835850(v=msdn.10)) sur [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) sur le contrôle InkEdit comme indiqué dans la rubrique [meilleures pratiques](best-practices.md) .</span><span class="sxs-lookup"><span data-stu-id="4993f-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="4993f-112">L' [exemple PenInputPanel](peninputpanel-sample.md) fournit un exemple d’activation de TSF.</span><span class="sxs-lookup"><span data-stu-id="4993f-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4993f-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4993f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4993f-114">Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="4993f-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
