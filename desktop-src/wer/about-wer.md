---
title: À propos de WER
description: Rapport d’erreurs Windows (WER) est une infrastructure de commentaires flexible basée sur les événements, conçue pour collecter des informations sur les problèmes matériels et logiciels que Windows peut détecter, signaler les informations à Microsoft et fournir aux utilisateurs toutes les solutions disponibles. Pour plus d’informations sur les améliorations apportées à WER, consultez What’s New in WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Rapport d’erreurs Windows Rapport d’erreurs Windows, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310493"
---
# <a name="about-wer"></a><span data-ttu-id="7f182-105">À propos de WER</span><span class="sxs-lookup"><span data-stu-id="7f182-105">About WER</span></span>

<span data-ttu-id="7f182-106">Rapport d’erreurs Windows (WER) est une infrastructure de commentaires flexible basée sur les événements, conçue pour collecter des informations sur les problèmes matériels et logiciels que Windows peut détecter, signaler les informations à Microsoft et fournir aux utilisateurs toutes les solutions disponibles.</span><span class="sxs-lookup"><span data-stu-id="7f182-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="7f182-107">Pour plus d’informations sur les améliorations apportées à WER, consultez [What’s New in wer](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="7f182-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="7f182-108">À compter de Windows Vista, Windows fournit par défaut des erreurs de blocage, de réponse et de défaillance du noyau, sans nécessiter de modifications de votre application.</span><span class="sxs-lookup"><span data-stu-id="7f182-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="7f182-109">Les applications utilisent à la place l’API WER pour générer des rapports d’erreurs pour les problèmes spécifiques à l’application qui ne sont pas liés aux incidents, aux non-réponses ou aux erreurs de noyau.</span><span class="sxs-lookup"><span data-stu-id="7f182-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="7f182-110">Pour générer des rapports d’erreurs pour les problèmes spécifiques à l’application, l’application doit créer une brève description du problème à l’aide de quelques informations de base appelées *paramètres de rapport*.</span><span class="sxs-lookup"><span data-stu-id="7f182-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="7f182-111">Les paramètres de rapport comprennent des informations telles que le nom de l’application, la version de l’application, le nom du module, la version du module et le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f182-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="7f182-112">La combinaison de ces paramètres de rapport décrit un problème unique.</span><span class="sxs-lookup"><span data-stu-id="7f182-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="7f182-113">Lorsque WER recherche une solution, il communique avec le serveur WER à Microsoft en lui demandant d’abord si le problème est déjà connu.</span><span class="sxs-lookup"><span data-stu-id="7f182-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="7f182-114">Le serveur répond de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f182-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="7f182-115">Si le problème est connu et qu’il existe une solution, le serveur envoie la solution à l’ordinateur client et WER affiche ces informations à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f182-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="7f182-116">Si le problème est étudié, le serveur peut envoyer une réponse qui indique l’État.</span><span class="sxs-lookup"><span data-stu-id="7f182-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="7f182-117">Si le développeur a besoin d’informations supplémentaires pour résoudre le problème, le serveur demande des informations supplémentaires dans WER et WER demande à l’utilisateur l’autorisation d’envoyer ces informations.</span><span class="sxs-lookup"><span data-stu-id="7f182-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="7f182-118">Si le problème n’est pas connu, le serveur crée un problème pour qu’un développeur examine et envoie une réponse WER qui indique l’État.</span><span class="sxs-lookup"><span data-stu-id="7f182-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="7f182-119">À l’aide de ce processus, WER rassemble plus d’informations si nécessaire, ou envoie une solution à l’utilisateur lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="7f182-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="7f182-120">Sur Windows Vista, l’utilisateur peut accéder aux **rapports et solutions aux problèmes** à tout moment pour afficher les solutions disponibles, vérifier si de nouvelles solutions sont disponibles ou gérer les autres rapports et paramètres wer.</span><span class="sxs-lookup"><span data-stu-id="7f182-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="7f182-121">Sur Windows 7, les **rapports et solutions aux problèmes** sont désormais appelés **Centre de maintenance**.</span><span class="sxs-lookup"><span data-stu-id="7f182-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="7f182-122">Cliquez sur **Démarrer** et entrez « afficher » dans **Rechercher les programmes et fichiers** , puis sélectionnez **Afficher tous les rapports de problèmes**, **afficher l’historique de fiabilité** ou afficher les **solutions aux problèmes**.</span><span class="sxs-lookup"><span data-stu-id="7f182-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f182-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f182-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f182-124">Rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="7f182-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




