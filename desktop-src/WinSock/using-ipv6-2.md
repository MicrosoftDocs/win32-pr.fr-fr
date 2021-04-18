---
description: Sur Windows XP plus tard, un nouvel outil de ligne de commande est fourni pour la configuration et la gestion d’IPv4. Cet outil utilise la \# commande &0034 ; netsh interface ip&\# 0034 ; pour la configuration et la gestion d’IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Utilisation d'une adresse IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533679"
---
# <a name="using-ipv6"></a><span data-ttu-id="a2057-104">Utilisation d'une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="a2057-104">Using IPv6</span></span>

<span data-ttu-id="a2057-105">Sur Windows XP plus tard, un nouvel outil de ligne de commande est fourni pour la configuration et la gestion d’IPv4.</span><span class="sxs-lookup"><span data-stu-id="a2057-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="a2057-106">Cet outil utilise la commande « netsh interface IP » pour la configuration et la gestion d’IPv4.</span><span class="sxs-lookup"><span data-stu-id="a2057-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="a2057-107">Sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures, ce nouvel outil en ligne de commande a été amélioré pour prendre en charge la configuration et la gestion d’IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2057-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="a2057-108">Cet outil amélioré est la commande « netsh interface IPv6 ».</span><span class="sxs-lookup"><span data-stu-id="a2057-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="a2057-109">Les modifications de configuration effectuées à l’aide des commandes Netsh.exe sont permanentes et ne sont pas perdues lors du redémarrage de l’ordinateur ou du protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2057-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="a2057-110">La commande suivante est disponible sur Windows XP avec SP1 et versions ultérieures pour interroger et configurer IPv6 sur un ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="a2057-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="a2057-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="a2057-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="a2057-112">Avant Windows XP avec Service Pack 1 (SP1), la configuration et la gestion IPv6 utilisaient plusieurs anciens outils en ligne de commande pour configurer et gérer IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2057-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="a2057-113">À l’aide de ces outils plus anciens, les modifications IPv6 ne sont pas permanentes et sont perdues lorsque l’ordinateur ou le protocole IPv6 a été redémarré.</span><span class="sxs-lookup"><span data-stu-id="a2057-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="a2057-114">Les commandes plus anciennes suivantes sont disponibles sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2057-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="a2057-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="a2057-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="a2057-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="a2057-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="a2057-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="a2057-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="a2057-118">Ces anciens outils étaient également fournis dans la version préliminaire de la technologie IPv6 pour Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a2057-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="a2057-119">Les modifications de configuration effectuées à l’aide de ces anciens outils peuvent être conservées en les plaçant sous forme de lignes de commande dans un fichier de script de commande (. cmd) qui est exécuté après le redémarrage de l’ordinateur ou du protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2057-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="a2057-120">Pour rétablir automatiquement les modifications de configuration après le redémarrage, il est possible d’utiliser les tâches planifiées de Windows pour exécuter le fichier. cmd au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a2057-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="a2057-121">Ces outils plus anciens ne sont pas fournis sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a2057-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="a2057-122">L’outil « netsh interface IPv6 » est fourni pour la configuration et la gestion D’ipv6 à partir de la ligne de commande sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a2057-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2057-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2057-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2057-124">Protocole Internet version 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="a2057-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="a2057-125">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a2057-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="a2057-126">Version préliminaire de la technologie IPv6 pour Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a2057-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



