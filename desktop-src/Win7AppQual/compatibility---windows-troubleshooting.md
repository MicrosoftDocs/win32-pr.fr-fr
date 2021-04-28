---
description: Résolution des problèmes Windows
ms.assetid: fb2c487a-d395-45eb-9010-936a61a414d0
title: Résolution des problèmes Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff332afe1b586b05866d78b49013a264e815f3eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088557"
---
# <a name="windows-troubleshooting"></a><span data-ttu-id="b9b5b-103">Résolution des problèmes Windows</span><span class="sxs-lookup"><span data-stu-id="b9b5b-103">Windows Troubleshooting</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b9b5b-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="b9b5b-104">Affected Platforms</span></span>

<span data-ttu-id="b9b5b-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9b5b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b9b5b-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9b5b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="description"></a><span data-ttu-id="b9b5b-107">Description</span><span class="sxs-lookup"><span data-stu-id="b9b5b-107">Description</span></span>

<span data-ttu-id="b9b5b-108">Une nouvelle fonctionnalité du centre de maintenance Windows 7 (anciennement appelée « Centre de solutions »), résolution des problèmes Windows, offre une expérience de dépannage systématique à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-108">A new Windows 7 Action Center (formerly known as Solutions Center) feature, Windows Troubleshooting, delivers a systematic troubleshooting experience for the user.</span></span> <span data-ttu-id="b9b5b-109">Le centre de maintenance est l’une des cinq icônes épinglées dans l’systray.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-109">The Action Center is one of the five icons pinned in the systray.</span></span> <span data-ttu-id="b9b5b-110">La résolution des problèmes Windows vous permet de parcourir ou de rechercher des packs de résolution des problèmes et des packs de résolution des problèmes qui sont stockés sur un serveur Microsoft sur Internet. c’est une meilleure approche en cas de connexion (BWC).</span><span class="sxs-lookup"><span data-stu-id="b9b5b-110">Windows Troubleshooting allows you to browse or search for in-box troubleshooting packs and for troubleshooting packs that are stored on a Microsoft server on the Internet – a Better When Connected (BWC) experience.</span></span> <span data-ttu-id="b9b5b-111">Vous pouvez sélectionner et exécuter un pack de résolution des problèmes pour tenter de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-111">You can select and run a troubleshooting pack to attempt to resolve their problem.</span></span> <span data-ttu-id="b9b5b-112">Si vous ne parvenez pas à identifier la résolution du problème, vous avez la possibilité de rechercher de l’aide, du contenu de la communauté et des Articles de support, ou d’autres packs de résolution des problèmes pour obtenir le contenu associé pertinent.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-112">If you cannot identify a resolution to the problem, you have the option of searching help, community content, and support articles, or other troubleshooting packs for relevant related content.</span></span> <span data-ttu-id="b9b5b-113">Si vous ne fournissez pas de réponse au problème, vous pouvez restaurer le PC à une heure avant le moment où le problème s’est produit ou obtenir de l’aide via l’assistance à distance.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-113">Should that not provide an answer to the problem, you can restore the PC to a time prior to when the problem occurred or get help through remote assistance.</span></span> <span data-ttu-id="b9b5b-114">L’objectif est de vous permettre de trouver facilement et rapidement une solution au problème.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-114">The intent is to allow you to find a solution to the problem easily and quickly.</span></span>

## <a name="usage"></a><span data-ttu-id="b9b5b-115">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b9b5b-115">Usage</span></span>

<span data-ttu-id="b9b5b-116">Le centre de maintenance est clairement visible et disponible à partir de plusieurs emplacements.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-116">The Action Center is clearly visible and available from several locations.</span></span> <span data-ttu-id="b9b5b-117">Vous pouvez le lancer à partir du menu contextuel du centre de maintenance dans l’systray, à partir du panneau de configuration en tant que lien de raccourci sous système et maintenance, à partir de la page principale du centre de maintenance et à partir du contenu d’aide.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-117">You can launch it from the context menu of the Action Center in the systray, from the control panel as a shortcut link under system and maintenance, from the main page of the Action Center, and from Help content.</span></span>

<span data-ttu-id="b9b5b-118">Les packs de résolution des problèmes sont basés sur des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-118">Troubleshooting packs are based upon powershell scripts.</span></span> <span data-ttu-id="b9b5b-119">Le processus de création et de publication d’un pack de résolution des problèmes sera rendu public pour permettre aux OEM, aux IHV, aux éditeurs de logiciels indépendants et aux professionnels de l’informatique de développer et d’envoyer leur propre contenu de dépannage.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-119">The process of authoring and publishing a troubleshooting pack will be made public to allow OEMs, IHVs, ISVs, and IT Professionals to develop and ship their own troubleshooting content.</span></span>

<span data-ttu-id="b9b5b-120">Pour une expérience utilisateur cohérente, veillez à suivre les meilleures pratiques et les instructions décrites dans la boîte à outils de dépannage de Windows lors de la conception de vos propres packs de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b9b5b-120">For a consistent user experience, be sure to follow the best practices and guidelines described in the Windows troubleshooting toolkit when designing your own troubleshooting packs.</span></span>

 

 



