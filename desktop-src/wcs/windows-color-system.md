---
title: Système de couleurs Windows
description: Les schémas de gestion des couleurs sont mis en œuvre dans les systèmes d’exploitation Microsoft Windows pour améliorer le rendu du contenu en couleurs dans toutes les formes de communication numérique. Le schéma de gestion des couleurs utilisé à partir de Windows 2000, Windows XP et Windows Server 2003 est appelé gestion des couleurs d’image (ICM) 2,0. Le modèle de gestion des couleurs utilisé à partir de Windows Vista est appelé Windows Color System (WCS) 1,0. Le schéma de gestion des couleurs WCS 1,0 est un sur-ensemble d’API et de fonctionnalités ICM 2,0.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522897"
---
# <a name="windows-color-system"></a><span data-ttu-id="27a23-105">Système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="27a23-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="27a23-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="27a23-106">Purpose</span></span>

<span data-ttu-id="27a23-107">Les schémas de gestion des couleurs sont mis en œuvre dans les systèmes d’exploitation Microsoft Windows pour améliorer le rendu du contenu en couleurs dans toutes les formes de communication numérique.</span><span class="sxs-lookup"><span data-stu-id="27a23-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="27a23-108">Le schéma de gestion des couleurs utilisé à partir de Windows 2000, Windows XP et Windows Server 2003 est appelé gestion des couleurs d’image (ICM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="27a23-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="27a23-109">Le modèle de gestion des couleurs utilisé à partir de Windows Vista est appelé Windows Color System (WCS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="27a23-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="27a23-110">Le schéma de gestion des couleurs WCS 1,0 est un sur-ensemble d’API et de fonctionnalités ICM 2,0.</span><span class="sxs-lookup"><span data-stu-id="27a23-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="27a23-111">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="27a23-111">Where applicable</span></span>

<span data-ttu-id="27a23-112">ICM peut être utilisé dans toutes les applications sur les systèmes d’exploitation Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="27a23-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="27a23-113">WCS peut être utilisé dans toutes les applications sur Windows Vista et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="27a23-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="27a23-114">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="27a23-114">Developer audience</span></span>

<span data-ttu-id="27a23-115">L’API WCS est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="27a23-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="27a23-116">Vous devez vous familiariser avec l’interface utilisateur graphique de Windows, l’architecture pilotée par les messages et des connaissances pratiques sur les concepts de gestion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="27a23-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="27a23-117">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="27a23-117">Run-time requirements</span></span>

<span data-ttu-id="27a23-118">Les applications qui utilisent l’API ICM requièrent Windows 2000 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27a23-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="27a23-119">Les applications qui utilisent l’API WCS requièrent Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27a23-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="27a23-120">Pour obtenir des informations spécifiques au moment de l’exécution sur une fonction, consultez la section Configuration requise de la page de référence pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="27a23-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="27a23-121">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="27a23-121">In this section</span></span>

-   [<span data-ttu-id="27a23-122">Considérations relatives à la sécurité : système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="27a23-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="27a23-123">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="27a23-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="27a23-124">Schémas et algorithmes du système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="27a23-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="27a23-125">À propos de Windows Color System version 1.0</span><span class="sxs-lookup"><span data-stu-id="27a23-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="27a23-126">Utilisation de WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="27a23-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="27a23-127">Référence</span><span class="sxs-lookup"><span data-stu-id="27a23-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="27a23-128">Glossaire WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="27a23-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="27a23-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27a23-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27a23-130">Technologie</span><span class="sxs-lookup"><span data-stu-id="27a23-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="27a23-131">Multimédia Windows</span><span class="sxs-lookup"><span data-stu-id="27a23-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="27a23-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="27a23-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 