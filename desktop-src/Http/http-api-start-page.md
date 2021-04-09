---
title: API de serveur HTTP
description: L’API du serveur HTTP permet aux applications de communiquer sur HTTP sans utiliser Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API de serveur HTTP
- API serveur HTTP, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101624"
---
# <a name="http-server-api"></a><span data-ttu-id="2a6a6-105">API de serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6a6-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="2a6a6-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="2a6a6-106">Purpose</span></span>

<span data-ttu-id="2a6a6-107">L’API du serveur HTTP permet aux applications de communiquer sur HTTP sans utiliser Microsoft Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="2a6a6-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="2a6a6-108">Les applications peuvent s’inscrire pour recevoir des requêtes HTTP pour des URL particulières, recevoir des requêtes HTTP et envoyer des réponses HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="2a6a6-109">L’API du serveur HTTP comprend la prise en charge SSL afin que les applications puissent échanger des données via des connexions HTTP sécurisées sans IIS.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="2a6a6-110">Il est également conçu pour fonctionner avec des ports de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2a6a6-111">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="2a6a6-111">Developer audience</span></span>

<span data-ttu-id="2a6a6-112">Cette API est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2a6a6-113">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="2a6a6-113">Run-time requirements</span></span>

<span data-ttu-id="2a6a6-114">L’API du serveur HTTP est prise en charge sur les systèmes d’exploitation Windows Server 2003 et Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="2a6a6-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="2a6a6-115">Sachez que Microsoft IIS 5 s’exécutant sur Windows XP avec SP2 ne peut pas partager le port 80 avec d’autres applications HTTP exécutées simultanément.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2a6a6-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="2a6a6-116">In this section</span></span>



| <span data-ttu-id="2a6a6-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2a6a6-117">Topic</span></span>                                                                           | <span data-ttu-id="2a6a6-118">Description</span><span class="sxs-lookup"><span data-stu-id="2a6a6-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a6a6-119">À propos de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6a6-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="2a6a6-120">Informations générales sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="2a6a6-121">Utilisation de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6a6-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="2a6a6-122">Guide de procédures pour l’utilisation de HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="2a6a6-123">Référence de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6a6-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="2a6a6-124">Documentation des fonctions, structures et types d’énumération spécifiques disponibles dans HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="2a6a6-125">Exemple d’application de serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6a6-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="2a6a6-126">Exemple d’application qui montre comment utiliser l’API du serveur HTTP pour effectuer des tâches côté serveur.</span><span class="sxs-lookup"><span data-stu-id="2a6a6-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2a6a6-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a6a6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a6a6-128">Services HTTP Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="2a6a6-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

