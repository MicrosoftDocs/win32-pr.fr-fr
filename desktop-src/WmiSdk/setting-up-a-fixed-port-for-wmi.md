---
description: WMI s’exécute dans le cadre d’un hôte de service partagé avec les ports attribués par le biais de DCOM par défaut. Toutefois, vous pouvez configurer le service WMI pour qu’il s’exécute en tant que seul processus dans un hôte distinct et spécifier un port fixe.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configuration d’un port fixe pour WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532159"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="90497-104">Configuration d’un port fixe pour WMI</span><span class="sxs-lookup"><span data-stu-id="90497-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="90497-105">WMI s’exécute dans le cadre d’un hôte de service partagé avec les ports attribués par le biais de DCOM par défaut.</span><span class="sxs-lookup"><span data-stu-id="90497-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="90497-106">Toutefois, vous pouvez configurer le service WMI pour qu’il s’exécute en tant que seul processus dans un hôte distinct et spécifier un port fixe.</span><span class="sxs-lookup"><span data-stu-id="90497-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="90497-107">La procédure suivante est une installation automatisée pour permettre à WMI d’avoir un port fixe.</span><span class="sxs-lookup"><span data-stu-id="90497-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="90497-108">La procédure utilise l’outil en ligne de commande [**winmgmt**](winmgmt.md) .</span><span class="sxs-lookup"><span data-stu-id="90497-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="90497-109">**Pour configurer un port fixe pour WMI**</span><span class="sxs-lookup"><span data-stu-id="90497-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="90497-110">À l’invite de commandes, tapez **winmgmt-standalonehost**</span><span class="sxs-lookup"><span data-stu-id="90497-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="90497-111">Arrêtez le service WMI en tapant la commande **net stop « Windows Management Instrumentation »**, ou utilisez le nom abrégé **net stop winmgmt**</span><span class="sxs-lookup"><span data-stu-id="90497-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="90497-112">Redémarrez le service WMI dans un nouvel hôte de service en tapant **net start « Windows Management Instrumentation »** ou **net start winmgmt**</span><span class="sxs-lookup"><span data-stu-id="90497-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="90497-113">Établissez un nouveau numéro de port pour le service WMI en tapant **netsh firewall Add ouverture TCP 24158 WMIFixedPort**</span><span class="sxs-lookup"><span data-stu-id="90497-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="90497-114">Pour annuler les modifications apportées à WMI, tapez **winmgmt/sharedhost**, puis arrêtez et redémarrez le service WinMgmt.</span><span class="sxs-lookup"><span data-stu-id="90497-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="90497-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="90497-115">Examples</span></span>

<span data-ttu-id="90497-116">Pour obtenir un script qui configure un port fixe pour WMI, consultez l' [exemple de code](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )de la Galerie de scripts suivant.</span><span class="sxs-lookup"><span data-stu-id="90497-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="90497-117">ou un exemple de code PowerShell qui active ou désactive les paramètres de port WMI, reportez-vous à l’exemple [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) sur la Galerie technet.</span><span class="sxs-lookup"><span data-stu-id="90497-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90497-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90497-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90497-119">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="90497-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="90497-120">Résolution des problèmes de connexions WMI distantes</span><span class="sxs-lookup"><span data-stu-id="90497-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="90497-121">Hébergement et sécurité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="90497-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



