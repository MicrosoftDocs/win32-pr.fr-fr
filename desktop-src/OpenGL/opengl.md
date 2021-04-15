---
title: Technologie
description: En tant qu’interface logicielle pour le matériel graphique, OpenGL effectue le rendu des objets multidimensionnels dans un trame.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463610"
---
# <a name="opengl"></a><span data-ttu-id="08055-103">Technologie</span><span class="sxs-lookup"><span data-stu-id="08055-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="08055-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="08055-104">Purpose</span></span>

<span data-ttu-id="08055-105">En tant qu’interface logicielle pour le matériel graphique, OpenGL effectue le rendu des objets multidimensionnels dans un trame.</span><span class="sxs-lookup"><span data-stu-id="08055-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="08055-106">L’implémentation Microsoft d’OpenGL pour le système d’exploitation Windows est un logiciel graphique standard avec lequel les programmeurs peuvent créer des images de couleur à trois dimensions toujours et animées de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="08055-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="08055-107">La version d’OpenGL décrite dans cette section est 1,1.</span><span class="sxs-lookup"><span data-stu-id="08055-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="08055-108">Pour plus d’informations sur OpenGL ES exécuté sur Windows, consultez [angle pour le Windows Store](https://github.com/microsoft/angle/wiki).</span><span class="sxs-lookup"><span data-stu-id="08055-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="08055-109">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="08055-109">Where applicable</span></span>

<span data-ttu-id="08055-110">OpenGL est conçu pour la compatibilité sur le matériel et les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="08055-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="08055-111">Cette architecture facilite le portage de programmes OpenGL d’un système vers un autre.</span><span class="sxs-lookup"><span data-stu-id="08055-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="08055-112">Même si chaque système d’exploitation a des exigences uniques, le code OpenGL dans de nombreux programmes peut être utilisé tel quel.</span><span class="sxs-lookup"><span data-stu-id="08055-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="08055-113">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="08055-113">Developer audience</span></span>

<span data-ttu-id="08055-114">Conçu pour être utilisé par les programmeurs C/C++, OpenGL requiert une connaissance de l’interface utilisateur graphique de Windows et de l’architecture pilotée par les messages.</span><span class="sxs-lookup"><span data-stu-id="08055-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="08055-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="08055-115">Run-time requirements</span></span>

<span data-ttu-id="08055-116">Pour plus d’informations sur les systèmes d’exploitation requis pour une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.</span><span class="sxs-lookup"><span data-stu-id="08055-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08055-117">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="08055-117">In this section</span></span>



| <span data-ttu-id="08055-118">Rubrique</span><span class="sxs-lookup"><span data-stu-id="08055-118">Topic</span></span>                                             | <span data-ttu-id="08055-119">Description</span><span class="sxs-lookup"><span data-stu-id="08055-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="08055-120">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="08055-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="08055-121">Informations générales sur le fonctionnement d’OpenGL.</span><span class="sxs-lookup"><span data-stu-id="08055-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="08055-122">Référence</span><span class="sxs-lookup"><span data-stu-id="08055-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="08055-123">Documentation des fonctions, structures et autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="08055-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="08055-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="08055-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="08055-125">Exemples de code OpenGL.</span><span class="sxs-lookup"><span data-stu-id="08055-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="08055-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08055-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08055-127">Graphiques et jeux DirectX</span><span class="sxs-lookup"><span data-stu-id="08055-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="08055-128">[Image toujours](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08055-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="08055-129">[Système de couleurs Windows (WCS)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08055-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08055-130">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="08055-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="08055-131">Acquisition d’image Windows</span><span class="sxs-lookup"><span data-stu-id="08055-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="08055-132">Multimédia Windows</span><span class="sxs-lookup"><span data-stu-id="08055-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="08055-133">[API Windows](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08055-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

