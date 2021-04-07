---
title: Infrastructure de diagnostics réseau
description: Network Diagnostics Framework (NDF) permet aux développeurs de composants et d’applications de simplifier la résolution des problèmes réseau pour les utilisateurs.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028917"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="1b0c5-103">Infrastructure de diagnostics réseau</span><span class="sxs-lookup"><span data-stu-id="1b0c5-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="1b0c5-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="1b0c5-104">Purpose</span></span>

<span data-ttu-id="1b0c5-105">Network Diagnostics Framework (NDF) permet aux développeurs de composants et d’applications de simplifier la résolution des problèmes réseau pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="1b0c5-106">Les utilisateurs peuvent tenter de diagnostiquer et de réparer un problème réseau à l’aide d’un seul outil de dépannage.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="1b0c5-107">Microsoft fournit des classes d’assistance NDF, dont certaines sont extensibles afin que les développeurs puissent créer des unités de dépannage appelées extensions de classe d’assistance pour fournir des diagnostics plus détaillés spécifiques à des composants logiciels ou matériels particuliers.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1b0c5-108">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="1b0c5-108">Where applicable</span></span>

<span data-ttu-id="1b0c5-109">NDF peut être utilisé par les logiciels des fournisseurs qui s’appuient sur la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1b0c5-110">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="1b0c5-110">Developer audience</span></span>

<span data-ttu-id="1b0c5-111">L’API NDF est conçue pour les développeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1b0c5-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="1b0c5-112">Run-time requirements</span></span>

<span data-ttu-id="1b0c5-113">NDF est disponible pour les ordinateurs exécutant Windows Vista, Windows Server 2008 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b0c5-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1b0c5-114">In this section</span></span>



| <span data-ttu-id="1b0c5-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1b0c5-115">Topic</span></span>                                                                       | <span data-ttu-id="1b0c5-116">Description</span><span class="sxs-lookup"><span data-stu-id="1b0c5-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b0c5-117">À propos de NDF</span><span class="sxs-lookup"><span data-stu-id="1b0c5-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="1b0c5-118">Fournit une synthèse générale de la technologie NDF.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="1b0c5-119">Utilisation d’NDF</span><span class="sxs-lookup"><span data-stu-id="1b0c5-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="1b0c5-120">Fournit des informations et des exemples sur l’utilisation des fonctionnalités NDF, ainsi que sur la façon d’étendre cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="1b0c5-121">Référence NDF</span><span class="sxs-lookup"><span data-stu-id="1b0c5-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="1b0c5-122">Fournit des informations sur les énumérations, les fonctions, les interfaces et les structures qui prennent en charge l’utilisation d’NDF, ainsi que des informations sur les classes d’assistance extensible fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="1b0c5-123">Traçage réseau dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="1b0c5-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="1b0c5-124">Décrit le traçage réseau et les outils à utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="1b0c5-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 





