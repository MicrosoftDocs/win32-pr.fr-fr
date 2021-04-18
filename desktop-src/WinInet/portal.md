---
title: Windows Internet
description: L’interface de programmation d’applications (API) Microsoft Windows Internet (WinINet) permet aux applications d’accéder aux protocoles Internet standard, tels que FTP et HTTP. Pour faciliter l’utilisation, WinINet fait abstraction de ces protocoles dans une interface de haut niveau.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- WinINet Windows Internet
- Wininet wininet, portail
- Windows Internet WinINet, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463511"
---
# <a name="windows-internet"></a><span data-ttu-id="69bbd-107">Windows Internet</span><span class="sxs-lookup"><span data-stu-id="69bbd-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="69bbd-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="69bbd-108">Purpose</span></span>

<span data-ttu-id="69bbd-109">L’interface de programmation d’applications (API) Microsoft Windows Internet (WinINet) permet aux applications d’accéder aux protocoles Internet standard, tels que FTP et HTTP.</span><span class="sxs-lookup"><span data-stu-id="69bbd-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="69bbd-110">Pour faciliter l’utilisation, WinINet fait abstraction de ces protocoles dans une interface de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="69bbd-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="69bbd-111">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="69bbd-111">Where applicable</span></span>

<span data-ttu-id="69bbd-112">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="69bbd-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="69bbd-113">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="69bbd-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="69bbd-114">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="69bbd-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="69bbd-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="69bbd-115">Developer audience</span></span>

<span data-ttu-id="69bbd-116">WinINet est conçu pour être utilisé par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="69bbd-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="69bbd-117">Elle nécessite une compréhension de base des protocoles FTP et HTTP.</span><span class="sxs-lookup"><span data-stu-id="69bbd-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="69bbd-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="69bbd-118">Run-time requirements</span></span>

<span data-ttu-id="69bbd-119">Les applications qui utilisent l’API WinINet nécessitent Windows NT 4,0 ou une version ultérieure, ou Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="69bbd-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="69bbd-120">Pour plus d’informations sur les systèmes d’exploitation ou les composants requis pour utiliser un élément de programmation particulier, consultez la section Configuration requise de la documentation.</span><span class="sxs-lookup"><span data-stu-id="69bbd-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69bbd-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="69bbd-121">In this section</span></span>



| <span data-ttu-id="69bbd-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="69bbd-122">Topic</span></span>                                                          | <span data-ttu-id="69bbd-123">Description</span><span class="sxs-lookup"><span data-stu-id="69bbd-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="69bbd-124">À propos de Windows Internet</span><span class="sxs-lookup"><span data-stu-id="69bbd-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="69bbd-125">Informations générales sur l’API Internet Windows.</span><span class="sxs-lookup"><span data-stu-id="69bbd-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="69bbd-126">Utilisation de Windows Internet</span><span class="sxs-lookup"><span data-stu-id="69bbd-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="69bbd-127">Guide de programmation de l’API Internet Windows.</span><span class="sxs-lookup"><span data-stu-id="69bbd-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="69bbd-128">Informations de référence sur Internet Windows</span><span class="sxs-lookup"><span data-stu-id="69bbd-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="69bbd-129">Documentation de référence pour l’API Internet Windows.</span><span class="sxs-lookup"><span data-stu-id="69bbd-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="69bbd-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69bbd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69bbd-131">Services HTTP Microsoft Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="69bbd-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

