---
description: Le transport et l’espace de noms Windows Sockets&\# 8211 ; les fournisseurs de services sont des dll avec un point d’entrée de procédure d’exportation unique pour la fonction d’initialisation du fournisseur de services WSPStartup ou NSPStartup, respectivement.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modèle d’interface de fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544659"
---
# <a name="function-interface-model"></a><span data-ttu-id="3c5ef-103">Modèle d’interface de fonction</span><span class="sxs-lookup"><span data-stu-id="3c5ef-103">Function Interface Model</span></span>

<span data-ttu-id="3c5ef-104">Espace de noms et transport Windows Sockets : les fournisseurs de services sont des dll avec un point d’entrée de procédure d’exportation unique pour la fonction d’initialisation du fournisseur de services [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) ou [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectivement.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="3c5ef-105">Toutes les autres fonctions du fournisseur de services sont rendues accessibles au \_32.dll Ws2 par le biais de la table de dispatch du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="3c5ef-106">Les DLL du fournisseur de services sont chargées en mémoire par le \_32.dll Ws2 uniquement lorsque cela est nécessaire, et sont déchargées lorsque leurs services ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="3c5ef-107">Le SPI définit également plusieurs circonstances dans lesquelles un fournisseur de services de transport appelle dans le \_32.dll (appels) Ws2 pour obtenir les services de prise en charge des dll.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="3c5ef-108">La DLL du fournisseur de services de transport reçoit la \_ table de distribution adcall de Ws232.dll via le paramètre *UpcallTable* pour [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="3c5ef-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="3c5ef-109">L’extension de nom de fichier des fournisseurs de services doit être changée de « DLL » en «». WSP "ou". NSP».</span><span class="sxs-lookup"><span data-stu-id="3c5ef-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="3c5ef-110">Cette exigence n’est pas stricte.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-110">This requirement is not strict.</span></span> <span data-ttu-id="3c5ef-111">Un fournisseur de services fonctionnera toujours avec l' \_32.dll Ws2 avec n’importe quelle extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="3c5ef-112">Le SPI Winsock utilise la Convention d’affectation de noms de préfixe de fonction suivante :</span><span class="sxs-lookup"><span data-stu-id="3c5ef-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="3c5ef-113">Préfixe</span><span class="sxs-lookup"><span data-stu-id="3c5ef-113">Prefix</span></span> | <span data-ttu-id="3c5ef-114">Signification</span><span class="sxs-lookup"><span data-stu-id="3c5ef-114">Meaning</span></span>                          | <span data-ttu-id="3c5ef-115">Description</span><span class="sxs-lookup"><span data-stu-id="3c5ef-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="3c5ef-116">WSP</span><span class="sxs-lookup"><span data-stu-id="3c5ef-116">WSP</span></span>    | <span data-ttu-id="3c5ef-117">Fournisseur de services Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="3c5ef-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="3c5ef-118">Points d’entrée du fournisseur de services de transport</span><span class="sxs-lookup"><span data-stu-id="3c5ef-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="3c5ef-119">WPU</span><span class="sxs-lookup"><span data-stu-id="3c5ef-119">WPU</span></span>    | <span data-ttu-id="3c5ef-120">Appel du fournisseur de sockets Windows</span><span class="sxs-lookup"><span data-stu-id="3c5ef-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="3c5ef-121">Ws2 \_32.dll points d’entrée pour les fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="3c5ef-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="3c5ef-122">WSC</span><span class="sxs-lookup"><span data-stu-id="3c5ef-122">WSC</span></span>    | <span data-ttu-id="3c5ef-123">Configuration de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="3c5ef-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="3c5ef-124">WS2 \_32.dll points d’entrée pour les applets d’installation</span><span class="sxs-lookup"><span data-stu-id="3c5ef-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="3c5ef-125">LECTEURS</span><span class="sxs-lookup"><span data-stu-id="3c5ef-125">NSP</span></span>    | <span data-ttu-id="3c5ef-126">Fournisseur d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c5ef-126">Namespace Provider</span></span>               | <span data-ttu-id="3c5ef-127">Points d’entrée du fournisseur d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="3c5ef-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="3c5ef-128">Comme décrit ci-dessus, ces points d’entrée ne sont pas exportés (à l’exception de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) et [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), mais ils sont accessibles via un échange de tables de dispatch.</span><span class="sxs-lookup"><span data-stu-id="3c5ef-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



