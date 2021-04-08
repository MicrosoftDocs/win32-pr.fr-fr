---
title: Récupération et redémarrage d’application
description: Écrire des programmes d’installation personnalisés pour redémarrer automatiquement une application qui a été arrêtée pour terminer une mise à jour. Enregistrez les données et configurez la récupération de l’application avant de quitter les programmes.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- fiabilité
- fiabilité des logiciels
- récupération d’application
- redémarrage de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840686"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="b33fa-111">Récupération et redémarrage d’application</span><span class="sxs-lookup"><span data-stu-id="b33fa-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="b33fa-112">Objectif</span><span class="sxs-lookup"><span data-stu-id="b33fa-112">Purpose</span></span>

<span data-ttu-id="b33fa-113">Une application peut utiliser la récupération et le redémarrage de l’application (ARR) pour enregistrer les données et les informations d’État avant la fermeture de l’application en raison d’une exception non gérée ou lorsque l’application cesse de répondre.</span><span class="sxs-lookup"><span data-stu-id="b33fa-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="b33fa-114">L’application est également redémarrée, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b33fa-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="b33fa-115">Une application peut également être redémarrée si un programme d’installation met à jour un composant de l’application, ou si l’ordinateur doit redémarrer suite à une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b33fa-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="b33fa-116">Notez que pour prendre en charge le redémarrage automatique de l’application après qu’un programme d’installation a mis à jour une application, l’application et le programme d’installation doivent être correctement créés.</span><span class="sxs-lookup"><span data-stu-id="b33fa-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="b33fa-117">Pour plus d’informations, consultez [inscription au redémarrage de l’application](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="b33fa-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b33fa-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="b33fa-118">Developer audience</span></span>

<span data-ttu-id="b33fa-119">ARR est conçu pour les développeurs C et C++.</span><span class="sxs-lookup"><span data-stu-id="b33fa-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b33fa-120">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="b33fa-120">Run-time requirements</span></span>

<span data-ttu-id="b33fa-121">ARR est disponible à partir du système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b33fa-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b33fa-122">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b33fa-122">In this section</span></span>



| <span data-ttu-id="b33fa-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b33fa-123">Topic</span></span>                                                                                                   | <span data-ttu-id="b33fa-124">Description</span><span class="sxs-lookup"><span data-stu-id="b33fa-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b33fa-125">Utilisation de la récupération et du redémarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="b33fa-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="b33fa-126">Guide de procédures pour l’inscription pour la récupération et le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="b33fa-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="b33fa-127">Informations de référence sur la récupération et le redémarrage d’application</span><span class="sxs-lookup"><span data-stu-id="b33fa-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="b33fa-128">Informations de référence pour l’API ARR.</span><span class="sxs-lookup"><span data-stu-id="b33fa-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





