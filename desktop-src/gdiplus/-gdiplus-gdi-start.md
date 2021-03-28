---
description: Windows GDI+ est une API basée sur une classe pour les programmeurs C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112951"
---
# <a name="gdi"></a><span data-ttu-id="885f3-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="885f3-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="885f3-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="885f3-104">Purpose</span></span>

<span data-ttu-id="885f3-105">Windows GDI+ est une API basée sur une classe pour les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="885f3-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="885f3-106">Elle permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois sur l’écran vidéo et sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="885f3-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="885f3-107">Les applications basées sur l'API Microsoft Win32 n'accèdent pas directement au matériel graphique.</span><span class="sxs-lookup"><span data-stu-id="885f3-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="885f3-108">À la place, GDI+ interagit avec les pilotes de périphérique pour le compte des applications.</span><span class="sxs-lookup"><span data-stu-id="885f3-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="885f3-109">GDI+ est également pris en charge par Microsoft Win64.</span><span class="sxs-lookup"><span data-stu-id="885f3-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="885f3-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="885f3-110">Where applicable</span></span>

<span data-ttu-id="885f3-111">Les fonctions et les classes GDI+ ne sont pas prises en charge pour une utilisation dans un service Windows.</span><span class="sxs-lookup"><span data-stu-id="885f3-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="885f3-112">Toute tentative d’utilisation de ces fonctions et classes à partir d’un service Windows peut entraîner des problèmes inattendus, tels que des performances de service réduites et des exceptions ou des erreurs d’exécution.</span><span class="sxs-lookup"><span data-stu-id="885f3-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="885f3-113">Lorsque vous utilisez l’API GDI+, vous ne devez jamais autoriser votre application à télécharger des polices arbitraires à partir de sources non approuvées.</span><span class="sxs-lookup"><span data-stu-id="885f3-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="885f3-114">Le système d’exploitation requiert des privilèges élevés pour s’assurer que toutes les polices installées sont approuvées.</span><span class="sxs-lookup"><span data-stu-id="885f3-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="885f3-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="885f3-115">Developer audience</span></span>

<span data-ttu-id="885f3-116">L’interface basée sur la classe C++ GDI+ est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="885f3-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="885f3-117">Vous devez vous familiariser avec l’interface utilisateur graphique de Windows et l’architecture pilotée par les messages.</span><span class="sxs-lookup"><span data-stu-id="885f3-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="885f3-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="885f3-118">Run-time requirements</span></span>

<span data-ttu-id="885f3-119">GDI+ peut être utilisé dans toutes les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="885f3-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="885f3-120">GDI+ a été introduit dans Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="885f3-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="885f3-121">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une classe ou une méthode particulière, consultez la section plus d’informations de la documentation relative à la classe ou à la méthode.</span><span class="sxs-lookup"><span data-stu-id="885f3-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="885f3-122">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="885f3-122">In this section</span></span>

| <span data-ttu-id="885f3-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="885f3-123">Topic</span></span>                                                    | <span data-ttu-id="885f3-124">Description</span><span class="sxs-lookup"><span data-stu-id="885f3-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="885f3-125">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="885f3-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="885f3-126">Informations générales sur GDI+.</span><span class="sxs-lookup"><span data-stu-id="885f3-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="885f3-127">À</span><span class="sxs-lookup"><span data-stu-id="885f3-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="885f3-128">Tâches et exemples utilisant GDI+.</span><span class="sxs-lookup"><span data-stu-id="885f3-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="885f3-129">Référence</span><span class="sxs-lookup"><span data-stu-id="885f3-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="885f3-130">Documentation de l’API basée sur la classe C++ GDI+.</span><span class="sxs-lookup"><span data-stu-id="885f3-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="885f3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="885f3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885f3-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="885f3-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="885f3-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="885f3-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="885f3-134">Acquisition d’image Windows</span><span class="sxs-lookup"><span data-stu-id="885f3-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="885f3-135">Technologie</span><span class="sxs-lookup"><span data-stu-id="885f3-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="885f3-136">Multimédia Windows</span><span class="sxs-lookup"><span data-stu-id="885f3-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
