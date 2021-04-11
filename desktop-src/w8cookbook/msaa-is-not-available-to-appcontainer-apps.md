---
title: MSAA n’est pas disponible pour les applications du Windows Store
description: MSAA n’est pas disponible pour les applications du Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031993"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="4002a-103">MSAA n’est pas disponible pour les applications du Windows Store</span><span class="sxs-lookup"><span data-stu-id="4002a-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="4002a-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="4002a-104">Platform</span></span>

<span data-ttu-id="4002a-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="4002a-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="4002a-106">Description</span><span class="sxs-lookup"><span data-stu-id="4002a-106">Description</span></span>

<span data-ttu-id="4002a-107">Windows 8 ne prend pas en charge MSAA (Microsoft Active Accessibility) pour lire ou automatiser des données accessibles à partir d’applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002a-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="4002a-108">L’API UI Automation (UIA), disponible depuis Windows 7, doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="4002a-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="4002a-109">Étant donné qu’il n’existe pas de fonctionnalités d’application Windows Store existantes, aucune implémentation existante n’est affectée par cette modification.</span><span class="sxs-lookup"><span data-stu-id="4002a-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="4002a-110">Cela affecte uniquement les nouvelles applications et fonctionnalités écrites pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4002a-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="4002a-111">Les développeurs peuvent toujours utiliser MSAA pour exposer leurs données d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="4002a-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="4002a-112">Si les données MSAA sont fournies par le fournisseur d’applications du Windows Store, les clients UIA pourront toujours lire et automatiser les données.</span><span class="sxs-lookup"><span data-stu-id="4002a-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="4002a-113">Pour simplifier l’API pour les applications du Windows Store 8Windows, nous avons décidé de prendre en charge uniquement UI Automation en tant que client pour ces applications.</span><span class="sxs-lookup"><span data-stu-id="4002a-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="4002a-114">Les clients UIA peuvent lire les fournisseurs UIA en mode natif, sans aucune traduction.</span><span class="sxs-lookup"><span data-stu-id="4002a-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="4002a-115">Les clients UIA peuvent lire les fournisseurs MSAA tels qu’ils sont traduits par le proxy UIA-à-MSAA.</span><span class="sxs-lookup"><span data-stu-id="4002a-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="4002a-116">Cela réduira la charge de test pour les développeurs d’applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002a-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="4002a-117">L’élimination de la prise en charge des fournisseurs MSAA réduirait davantage la matrice de test, mais il existe des applications majeures qui sont toujours basées sur MSAA et que nous ne souhaitons pas rendre inaccessibles.</span><span class="sxs-lookup"><span data-stu-id="4002a-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4002a-118">Manifestation</span><span class="sxs-lookup"><span data-stu-id="4002a-118">Manifestation</span></span>

<span data-ttu-id="4002a-119">Les développeurs d’applications du Windows Store ne seront pas en mesure d’accéder aux détails de MSAA dans le modèle d’application.</span><span class="sxs-lookup"><span data-stu-id="4002a-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="4002a-120">Solution</span><span class="sxs-lookup"><span data-stu-id="4002a-120">Solution</span></span>

<span data-ttu-id="4002a-121">Aucun nouveau cas automatisé ne doit être créé dans MSAA pour les fonctionnalités des applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002a-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="4002a-122">Basculez tous les outils intégrés existants qui utilisent MSAA vers UIA s’ils ont besoin d’interagir avec les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002a-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="4002a-123">Les développeurs d’applications du Windows Store doivent utiliser l’API UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4002a-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="4002a-124">Ressources</span><span class="sxs-lookup"><span data-stu-id="4002a-124">Resources</span></span>

-   [<span data-ttu-id="4002a-125">Notions de base d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="4002a-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 