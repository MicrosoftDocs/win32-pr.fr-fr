---
title: Windows Biometric Framework
description: Vous pouvez utiliser l’API Windows Biometric Framework pour créer des applications clientes qui capturent, enregistrent et comparent en toute sécurité les informations biométriques de l’utilisateur final.
ms.assetid: d9ac9ec1-bb34-402d-a590-73d5070b97ba
keywords:
- API Windows Biometric Framework API Windows Biometric Framework
- API Windows Biometric Framework API Windows Biometric Framework, page d’hébergement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4341f09f3141e1be77bcdf0987ee1273ffddcf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675161"
---
# <a name="windows-biometric-framework"></a><span data-ttu-id="a9f0d-105">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="a9f0d-105">Windows Biometric Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="a9f0d-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="a9f0d-106">Purpose</span></span>

<span data-ttu-id="a9f0d-107">Vous pouvez utiliser l’API Windows Biometric Framework pour créer des applications clientes qui capturent, enregistrent et comparent en toute sécurité les informations biométriques de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-107">You can use the Windows Biometric Framework API to create client applications that securely capture, save, and compare end-user biometric information.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a9f0d-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a9f0d-108">Developer audience</span></span>

<span data-ttu-id="a9f0d-109">Les développeurs qui utilisent cette API doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-109">Developers who use this API should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a9f0d-110">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a9f0d-110">Run-time requirements</span></span>

<span data-ttu-id="a9f0d-111">L’API Windows Biometric Framework est prise en charge à partir de Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-111">The Windows Biometric Framework API is supported beginning with Windows Server 2008 R2 and Windows 7.</span></span> <span data-ttu-id="a9f0d-112">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9f0d-113">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a9f0d-113">In this section</span></span>



| <span data-ttu-id="a9f0d-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a9f0d-114">Topic</span></span>                                                                                       | <span data-ttu-id="a9f0d-115">Description</span><span class="sxs-lookup"><span data-stu-id="a9f0d-115">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9f0d-116">Vue d’ensemble du Framework biométrique</span><span class="sxs-lookup"><span data-stu-id="a9f0d-116">Biometric Framework overview</span></span>](biometric-framework-overview.md)<br/>                 | <span data-ttu-id="a9f0d-117">Décrit la prise en charge native de la biométrie dans Windows.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-117">Describes the native support for biometrics in Windows.</span></span><br/>                                                                                       |
| [<span data-ttu-id="a9f0d-118">Création d’applications clientes</span><span class="sxs-lookup"><span data-stu-id="a9f0d-118">Creating client applications</span></span>](creating-client-applications.md)<br/>                 | <span data-ttu-id="a9f0d-119">Vous pouvez utiliser l’API cliente pour capturer et utiliser les informations biométriques dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-119">You can use the client API to capture and use biometric information in your applications.</span></span><br/>                                                     |
| [<span data-ttu-id="a9f0d-120">Création de plug-ins d’adaptateur</span><span class="sxs-lookup"><span data-stu-id="a9f0d-120">Creating Adapter Plug-ins</span></span>](creating-adapter-plug-ins.md)<br/>                       | <span data-ttu-id="a9f0d-121">Vous pouvez créer des adaptateurs de moteur, des adaptateurs de capteur et des adaptateurs de stockage à l’aide des rubriques de cette section.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-121">You can create engine adapters, sensor adapters, and storage adapters using the topics in this section.</span></span><br/>                                       |
| [<span data-ttu-id="a9f0d-122">Création d’un pool de capteurs privé</span><span class="sxs-lookup"><span data-stu-id="a9f0d-122">Creating a Private Sensor Pool</span></span>](creating-a-private-sensor-pool.md)<br/>             | <span data-ttu-id="a9f0d-123">Il existe deux types de pools de capteurs : privé et système.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-123">There are two types of sensor pools: private and system.</span></span> <span data-ttu-id="a9f0d-124">Cette section décrit chacune d’elles et explique comment créer un pool de capteurs privés.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-124">This section describes each and explains how to create a private sensor pool.</span></span> <br/>       |
| [<span data-ttu-id="a9f0d-125">Informations de référence sur l’API Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="a9f0d-125">Windows Biometric Framework API Reference</span></span>](biometric-service-api-reference.md)<br/> | <span data-ttu-id="a9f0d-126">Descriptions détaillées des fonctions, structures et autres éléments de programmation qui peuvent être utilisés pour créer des applications clientes et des plug-ins.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-126">Detailed descriptions of functions, structures, and other programming elements that can be used to create a client applications and plug-ins.</span></span><br/> |



 

 

 





