---
description: Vue d’ensemble des contrôles manuscrits pour Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Contrôles Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525966"
---
# <a name="ink-controls"></a><span data-ttu-id="3623b-103">Contrôles Ink</span><span class="sxs-lookup"><span data-stu-id="3623b-103">Ink Controls</span></span>

<span data-ttu-id="3623b-104">La plateforme Tablet PC fournit deux contrôles, [InkEdit](inkedit-control.md) et [InkPicture](inkpicture-control.md), qui vous permettent d’ajouter facilement la reconnaissance de l’écriture manuscrite et de l’écriture manuscrite aux applications Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3623b-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="3623b-105">Le contrôle InkEdit a des versions [managées](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) et Win32, tandis que InkPicture n’a que les versions d' [InkPicture](/previous-versions/ms583740(v=vs.100)) et [ActiveX](inkpicture-control-reference.md) gérées.</span><span class="sxs-lookup"><span data-stu-id="3623b-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="3623b-106">La principale différence entre les contrôles réside dans la façon dont les données sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="3623b-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="3623b-107">Le contrôle [InkEdit](inkedit-control.md) enregistre l’encre sous forme de texte par défaut, tandis que [InkPicture](inkpicture-control.md) enregistre l’encre sous forme d’encre.</span><span class="sxs-lookup"><span data-stu-id="3623b-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="3623b-108">Le contrôle [InkEdit](inkedit-control.md) est destiné à l’entrée de texte via la reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="3623b-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="3623b-109">[InkPicture](inkpicture-control.md) est destiné à l’annotation (par exemple, en marquant une diapositive de présentation ou une autre image).</span><span class="sxs-lookup"><span data-stu-id="3623b-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="3623b-110">Dans le code managé, créez des contrôles Ink dans le même thread que le thread principal pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3623b-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="3623b-111">Si un contrôle [InkEdit](inkedit-control.md) ou [InkPicture](inkpicture-control.md) est créé dans un thread différent, il se peut que votre application ne réponde pas correctement.</span><span class="sxs-lookup"><span data-stu-id="3623b-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="3623b-112">Vous devez définir explicitement le modèle de thread sur STA (single-thread Apartment) avant de créer un contrôle Ink.</span><span class="sxs-lookup"><span data-stu-id="3623b-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="3623b-113">Le contrôle est alors créé sur le thread principal.</span><span class="sxs-lookup"><span data-stu-id="3623b-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="3623b-114">Vous pouvez utiliser le code C++ managé suivant pour définir explicitement le modèle de thread.</span><span class="sxs-lookup"><span data-stu-id="3623b-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="3623b-115">Vous pouvez utiliser le code suivant pour effectuer la même opération en C \# .</span><span class="sxs-lookup"><span data-stu-id="3623b-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="3623b-116">Dans le code managé, pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que le contrôle ne soit hors de portée.</span><span class="sxs-lookup"><span data-stu-id="3623b-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="3623b-117">Les sections suivantes décrivent les contrôles Ink et l’utilisation des contrôles Ink dans les applications :</span><span class="sxs-lookup"><span data-stu-id="3623b-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="3623b-118">Ajout de contrôles Ink à un projet</span><span class="sxs-lookup"><span data-stu-id="3623b-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="3623b-119">InkEdit, contrôle</span><span class="sxs-lookup"><span data-stu-id="3623b-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="3623b-120">Contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="3623b-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
