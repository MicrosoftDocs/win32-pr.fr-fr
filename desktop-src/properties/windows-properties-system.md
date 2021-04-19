---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Système de propriétés Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515620"
---
# <a name="windows-property-system"></a><span data-ttu-id="1bcb1-103">Système de propriétés Windows</span><span class="sxs-lookup"><span data-stu-id="1bcb1-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="1bcb1-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="1bcb1-104">Purpose</span></span>

<span data-ttu-id="1bcb1-105">Le système de propriétés Windows est un système extensible en lecture/écriture de définitions de données qui offre un moyen uniforme d’exprimer des métadonnées sur les éléments de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="1bcb1-106">Le système de propriétés Windows dans Windows Vista et les versions ultérieures vous permet de stocker et de récupérer des métadonnées pour les éléments de Shell.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="1bcb1-107">Un élément de Shell est un élément de contenu unique, tel qu’un fichier, un dossier, un message électronique ou un contact.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="1bcb1-108">Une propriété est un élément de métadonnées individuel associé à un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1bcb1-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="1bcb1-109">Developer audience</span></span>

<span data-ttu-id="1bcb1-110">Avant de commencer à lire la documentation du kit de développement logiciel (SDK) du système de propriétés Windows, vous devez avoir une connaissance fondamentale des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1bcb1-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="1bcb1-111">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="1bcb1-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="1bcb1-112">Programmation de l’espace de noms Shell</span><span class="sxs-lookup"><span data-stu-id="1bcb1-112">Shell Namespace programming</span></span>

<span data-ttu-id="1bcb1-113">Pour une introduction à COM, consultez [principes de base de com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="1bcb1-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="1bcb1-114">Pour une introduction à la programmation de l’espace de noms Shell, consultez [prise en main avec l’espace de noms Shell](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="1bcb1-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="1bcb1-115">Pour les utilisations du système de propriétés Windows, consultez [vue d’ensemble du système de propriétés : scénarios de développement](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bcb1-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1bcb1-116">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="1bcb1-116">Run-time requirements</span></span>

<span data-ttu-id="1bcb1-117">L’environnement d’exécution pris en charge pour l’utilisation du système de propriétés Windows est Windows Vista ou version ultérieure et le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1bcb1-118">Windows XP et Microsoft Windows Desktop Search (WDS) 3,0 ou version ultérieure incluent également un sous-ensemble du système de propriétés Windows.</span><span class="sxs-lookup"><span data-stu-id="1bcb1-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="1bcb1-119">Pour le téléchargement du kit de développement logiciel (SDK) Windows Vista ou mis à jour, consultez le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1bcb1-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1bcb1-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1bcb1-120">In this section</span></span>

-   <span data-ttu-id="1bcb1-121">Cliquez sur [Vue d’ensemble du système de propriétés](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bcb1-121">[Property System Overview](property-system-overview.md)</span></span>
-   [<span data-ttu-id="1bcb1-122">Guide du développeur du système de propriétés Windows</span><span class="sxs-lookup"><span data-stu-id="1bcb1-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="1bcb1-123">Référence du système de propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcb1-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="1bcb1-124">Exemples de code du système de propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcb1-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
