---
description: La procédure suivante montre comment déboguer une analyse.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Débogage d’une analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529019"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="5b031-103">Débogage d’une analyse</span><span class="sxs-lookup"><span data-stu-id="5b031-103">Debugging a Monitor</span></span>

<span data-ttu-id="5b031-104">La procédure suivante montre comment déboguer une analyse.</span><span class="sxs-lookup"><span data-stu-id="5b031-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="5b031-105">**Pour déboguer une analyse**</span><span class="sxs-lookup"><span data-stu-id="5b031-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="5b031-106">Installez la DLL du moniteur et le fichier de base de données du programme (. pdb) généré lorsque vous avez compilé le moniteur à l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="5b031-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="5b031-107">Pour plus d’informations, consultez [installation d’une analyse pour moniteur réseau](installing-a-monitor-to-network-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="5b031-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="5b031-108">Vérifiez que le service de contrôle de l’analyse est configuré en tant que serveur au lieu d’un service en sélectionnant Panneau de configuration, services.</span><span class="sxs-lookup"><span data-stu-id="5b031-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="5b031-109">Ouvrez une invite de commandes et accédez au répertoire Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="5b031-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="5b031-110">Tapez :</span><span class="sxs-lookup"><span data-stu-id="5b031-110">Type:</span></span>

    <span data-ttu-id="5b031-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="5b031-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="5b031-112">Une fois la session de débogage de l’analyse terminée, vous pouvez rétablir la valeur par défaut de MCSVC en tapant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5b031-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="5b031-113">**Mcsvc.exe/service**</span><span class="sxs-lookup"><span data-stu-id="5b031-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="5b031-114">Dans Microsoft Visual Studio, lancez Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="5b031-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="5b031-115">Dans l’option de menu **fichier**, **ouvrir** , sélectionnez le nom de votre dll d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5b031-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="5b031-116">Après le chargement de Microsoft Visual C++, cliquez sur **projet**, **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="5b031-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="5b031-117">Cliquez sur l’onglet **Déboguer** sous **exécutable** pour session de débogage et tapez le chemin d’accès complet de Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="5b031-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="5b031-118">Par exemple, C : \\ Program Files \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="5b031-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="5b031-119">Définissez les points d’arrêt dans le code.</span><span class="sxs-lookup"><span data-stu-id="5b031-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="5b031-120">N’utilisez pas de boîte de message pour surveiller le débogage.</span><span class="sxs-lookup"><span data-stu-id="5b031-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="5b031-121">Si le MCSVC s’exécute en tant que service, vous ne verrez pas la fenêtre contextuelle et MCSVC semblera bloqué.</span><span class="sxs-lookup"><span data-stu-id="5b031-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



