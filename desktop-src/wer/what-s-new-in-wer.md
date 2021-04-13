---
title: Nouveautés du WER
description: Cette page récapitule les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour chaque version.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Rapport d’erreurs Windows des rapports d’erreurs Windows, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314646"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="ee9fb-104">Nouveautés du WER</span><span class="sxs-lookup"><span data-stu-id="ee9fb-104">What's New in WER</span></span>

<span data-ttu-id="ee9fb-105">Cette page récapitule les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="ee9fb-106">Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee9fb-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="ee9fb-107">La liste suivante résume les nouvelles fonctionnalités WER pour Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="ee9fb-108">Ajoute la possibilité de lever une exception qui ignore tous les gestionnaires d’exceptions, mettant ainsi fin à l’application immédiatement et appelant Rapport d’erreurs Windows.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="ee9fb-109">Pour plus d’informations, consultez la fonction [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ee9fb-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="ee9fb-110">Ajoute la possibilité d’enregistrer un gestionnaire d’exceptions hors processus que le WER appelle lorsqu’un incident se produit pour collecter le nom de l’événement, les paramètres de création de rapports et les options de lancement du débogage.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="ee9fb-111">Pour plus d’informations, consultez la fonction [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .</span><span class="sxs-lookup"><span data-stu-id="ee9fb-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="ee9fb-112">Fonctions qui ont été ajoutées :</span><span class="sxs-lookup"><span data-stu-id="ee9fb-112">Functions that were added:</span></span>

-   [<span data-ttu-id="ee9fb-113">**OutOfProcessExceptionEventCallback**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="ee9fb-114">**OutOfProcessExceptionEventSignatureCallback**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="ee9fb-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="ee9fb-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee9fb-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="ee9fb-117">**WerRegisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="ee9fb-118">**WerUnregisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="ee9fb-119">Structures qui ont été ajoutées :</span><span class="sxs-lookup"><span data-stu-id="ee9fb-119">Structures that were added:</span></span>

-   [<span data-ttu-id="ee9fb-120">**\_ \_ informations sur l’exception du runtime wer \_**</span><span class="sxs-lookup"><span data-stu-id="ee9fb-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="ee9fb-121">Windows Server 2008 et Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="ee9fb-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="ee9fb-122">La liste suivante récapitule les nouvelles fonctionnalités de WER pour Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ee9fb-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="ee9fb-123">Le rapport d’erreurs Windows peut être configuré de sorte que les vidages complets en mode utilisateur soient collectés et stockés localement après un incident d’application en mode utilisateur (les applications qui effectuent leurs propres rapports d’incident personnalisés, y compris les applications .NET ne sont pas prises en charge).</span><span class="sxs-lookup"><span data-stu-id="ee9fb-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="ee9fb-124">Pour plus d’informations, consultez [collecte des vidages de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="ee9fb-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="ee9fb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee9fb-125">Windows Vista</span></span>

<span data-ttu-id="ee9fb-126">La liste suivante résume les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour Windows Vista :</span><span class="sxs-lookup"><span data-stu-id="ee9fb-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="ee9fb-127">WER a été étendu au-delà de la surveillance des incidents et des processus qui ne répondent pas.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="ee9fb-128">WER prend en charge de nombreux nouveaux types d’événements non critiques, tels que les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="ee9fb-129">Cela permet aux développeurs d’en savoir plus sur les expériences de leurs clients avec les applications qu’ils ont développées.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="ee9fb-130">De nouvelles fonctions offrent aux développeurs la flexibilité nécessaire pour créer, personnaliser et soumettre des rapports de problèmes.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="ee9fb-131">Pour plus d’informations, consultez [fonctions wer](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ee9fb-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="ee9fb-132">[Windows Quality Online Services](https://www.microsoft.com/?ref=go) amélioré offre aux développeurs un accès aux informations sur les problèmes que les clients envoient pour leurs applications et un mécanisme permettant de fournir des solutions à ces clients.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="ee9fb-133">Les fonctions introduites par la récupération de l' [application et](/windows/desktop/Recovery/application-recovery-and-restart-portal) le gestionnaire de redémarrage et de [redémarrage](/windows/desktop/RstMgr/restart-manager-portal) permettent aux applications de récupérer automatiquement les informations et de redémarrer en cas de défaillance critique.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="ee9fb-134">Les développeurs peuvent utiliser ces fonctionnalités dans leurs applications pour améliorer de manière significative leur expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="ee9fb-135">Les **rapports et solutions aux problèmes sur Windows Vista ou le centre de maintenance sur Windows 7** constituent l’emplacement central où les utilisateurs peuvent interagir avec wer.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="ee9fb-136">Les utilisateurs peuvent rechercher de nouvelles solutions, gérer leur historique de création de rapports, afficher les détails d’un rapport de problème et gérer les paramètres de création de rapports, notamment activer le rapport d’erreurs Windows pour rechercher automatiquement des solutions sans interrompre l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee9fb-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee9fb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee9fb-138">Rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="ee9fb-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 