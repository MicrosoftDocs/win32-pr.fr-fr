---
description: Ce didacticiel met en évidence les différents aspects auxquels les développeurs Web doivent se soucier lors de la conception de pages pour le workflow d’autorisation Web pour Windows 8. Cette section illustre un workflow d’autorisation à deux pages.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Didacticiel sur l’authentification des pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545013"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="198bf-104">Didacticiel sur l’authentification des pages Web</span><span class="sxs-lookup"><span data-stu-id="198bf-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="198bf-105">Ce didacticiel met en évidence les différents aspects auxquels les développeurs Web doivent se soucier lors de la conception de pages pour le workflow d’autorisation Web pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="198bf-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="198bf-106">Cette section illustre un workflow d’autorisation à deux pages.</span><span class="sxs-lookup"><span data-stu-id="198bf-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="198bf-107">**Objectif :** L’objectif de l’exemple ne doit pas être normatif à propos de la disposition ou de la conception visuelle que chaque fournisseur aura certainement un point de vue unique sur, mais pour faire appel à quelques domaines intéressant d’investir dans pour bénéficier d’une expérience de style de conception Microsoft de première classe pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="198bf-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="198bf-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="198bf-108">Prerequisites</span></span>

<span data-ttu-id="198bf-109">Pour pouvoir utiliser les API du Service Broker d’authentification Web, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="198bf-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="198bf-110">Windows 8 (x86 ou amd64 uniquement)</span><span class="sxs-lookup"><span data-stu-id="198bf-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="198bf-111">Microsoft Internet Information Services (IIS) doit être installé à partir du panneau de configuration sous « programmes et fonctionnalités » et à l’aide de l’option « Activer ou désactiver des fonctionnalités Windows ».</span><span class="sxs-lookup"><span data-stu-id="198bf-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="198bf-112">**Durée totale :** 2 minutes.</span><span class="sxs-lookup"><span data-stu-id="198bf-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="198bf-113">Où aller à partir d’ici</span><span class="sxs-lookup"><span data-stu-id="198bf-113">Where to go from here</span></span>

<span data-ttu-id="198bf-114">Prochaine [authentification pour les pages Web](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="198bf-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="198bf-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="198bf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="198bf-116">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="198bf-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="198bf-117">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="198bf-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="198bf-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="198bf-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
