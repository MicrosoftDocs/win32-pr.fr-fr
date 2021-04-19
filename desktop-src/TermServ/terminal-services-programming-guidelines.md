---
title: Instructions de programmation Services Bureau à distance
description: Rubriques qui fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, instructions de programmation
- instructions de programmation Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536889"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="b4011-105">Instructions de programmation Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b4011-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="b4011-106">La plupart des applications Windows 32 bits ou 64 bits existantes s’exécutent « en l’environnement » dans une Services Bureau à distance (anciennement « services Terminal Server »).</span><span class="sxs-lookup"><span data-stu-id="b4011-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="b4011-107">Toutefois, certaines applications fonctionnent correctement et fonctionnent bien dans un environnement Services Bureau à distance, contrairement à d’autres.</span><span class="sxs-lookup"><span data-stu-id="b4011-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="b4011-108">Les rubriques suivantes fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4011-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4011-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b4011-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b4011-110">Instructions pour plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b4011-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="b4011-111">Instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4011-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b4011-112">Instructions relatives aux performances</span><span class="sxs-lookup"><span data-stu-id="b4011-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="b4011-113">Instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4011-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b4011-114">Instructions de programmation générales</span><span class="sxs-lookup"><span data-stu-id="b4011-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="b4011-115">Instructions pour le développement d’applications dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4011-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="b4011-116">La plupart de ces instructions sont de bonnes pratiques en matière de programmation qui tireront parti des applications qui s’exécutent dans n’importe quel environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="b4011-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="b4011-117">Toutefois, certaines optimisations recommandées, telles que la limitation des effets graphiques, sont des optimisations que vous souhaiteriez uniquement lorsque votre application s’exécute sous Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4011-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="b4011-118">Pour obtenir un exemple de code qui montre comment détecter un environnement de Services Bureau à distance, consultez [détection de l’environnement services Bureau à distance](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b4011-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4011-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4011-119">Related topics</span></span>

<dl> <span data-ttu-id="b4011-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b4011-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b4011-121">Les services Terminal Server sont désormais Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b4011-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="b4011-122">Format du fichier de modèle d’administration</span><span class="sxs-lookup"><span data-stu-id="b4011-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="b4011-123">Sécurité de la clé de Registre et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="b4011-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="b4011-124">Ruches du Registre</span><span class="sxs-lookup"><span data-stu-id="b4011-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="b4011-125">Descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="b4011-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="b4011-126">Droits d’accès standard</span><span class="sxs-lookup"><span data-stu-id="b4011-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="b4011-127">Modèle de Access Control</span><span class="sxs-lookup"><span data-stu-id="b4011-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 