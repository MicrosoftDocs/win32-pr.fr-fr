---
description: La rubrique suivante décrit le fonctionnement de l’API de plateforme d’évaluation Windows As a service (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: À propos de la plateforme d’évaluation WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544903"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="7fa30-103">À propos de la plateforme d’évaluation WaaS</span><span class="sxs-lookup"><span data-stu-id="7fa30-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="7fa30-104">La rubrique suivante décrit le fonctionnement de l’API de plateforme d’évaluation Windows As a service (WaaS).</span><span class="sxs-lookup"><span data-stu-id="7fa30-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="7fa30-105">L’API d’évaluation de WaaS offre à l’appelant les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7fa30-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="7fa30-106">Si un appareil se trouve sur les dernières mises à jour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7fa30-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="7fa30-107">Si l’appareil a atteint la fin du support.</span><span class="sxs-lookup"><span data-stu-id="7fa30-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="7fa30-108">Heures de publication des dernières mises à jour applicables pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7fa30-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="7fa30-109">Évaluation de la raison pour laquelle un appareil n’est pas à jour et l’impact potentiel qu’il peut avoir sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7fa30-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="7fa30-110">La plateforme d’évaluation WaaS utilise le modèle d’API COM et s’exécute automatiquement au moins une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="7fa30-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="7fa30-111">Ce cycle intercepte les informations de version applicables.</span><span class="sxs-lookup"><span data-stu-id="7fa30-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="7fa30-112">Pendant la période mise en cache, les évaluations sont effectuées par rapport aux informations de version mises en cache.</span><span class="sxs-lookup"><span data-stu-id="7fa30-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="7fa30-113">Si un appel est effectué en dehors de la fenêtre d’expiration du cache, un nouvel appel et une nouvelle évaluation sont effectués, mis en cache et retournés.</span><span class="sxs-lookup"><span data-stu-id="7fa30-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="7fa30-114">Lorsqu’un appel est effectué, le client d’évaluation de WaaS contacte le service d’évaluation WaaS avec les attributs de l’appareil et reçoit un dossier d’informations qui s’applique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7fa30-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="7fa30-115">Le client utilise ensuite ces informations par rapport aux informations recueillies sur l’appareil pour effectuer l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="7fa30-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="7fa30-116">Votre code doit disposer de privilèges d’administrateur pour appeler l’API d’évaluation WAAS.</span><span class="sxs-lookup"><span data-stu-id="7fa30-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="7fa30-117">Pour plus d’informations sur le développement d’applications qui requièrent des privilèges d’administrateur, consultez [cet article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="7fa30-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
