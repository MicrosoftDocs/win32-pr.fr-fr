---
title: Outils du journal des événements Windows
description: Le journal des événements Windows fournit les outils suivants que vous utilisez pour créer votre fournisseur.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104381734"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="7cb42-103">Outils du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="7cb42-103">Windows Event Log Tools</span></span>

<span data-ttu-id="7cb42-104">Le journal des événements Windows fournit les outils suivants que vous utilisez pour créer votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7cb42-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="7cb42-105">Outil</span><span class="sxs-lookup"><span data-stu-id="7cb42-105">Tool</span></span>                                                           | <span data-ttu-id="7cb42-106">Description</span><span class="sxs-lookup"><span data-stu-id="7cb42-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cb42-107">**Message Compiler (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="7cb42-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="7cb42-108">Utilitaire en ligne de commande utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message.</span><span class="sxs-lookup"><span data-stu-id="7cb42-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="7cb42-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="7cb42-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="7cb42-110">Utilitaire de ligne de commande principalement utilisé pour inscrire votre fournisseur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cb42-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="7cb42-111">Vous pouvez également l’utiliser pour obtenir des informations de métadonnées sur le fournisseur, ses événements et les canaux dans lesquels il journalise des événements, ainsi que pour interroger des événements à partir d’un canal ou d’un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7cb42-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="7cb42-112">L’outil WevtUtil.exe est inclus dans% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="7cb42-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="7cb42-113">Pour obtenir des informations sur l’utilisation, entrez « wevtutil/ ? »</span><span class="sxs-lookup"><span data-stu-id="7cb42-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="7cb42-114">à une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7cb42-114">at a command prompt.</span></span><br/> <span data-ttu-id="7cb42-115">Cette commande est limitée aux membres du groupe administrateurs et doit être exécutée avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="7cb42-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
