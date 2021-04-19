---
description: Utilisez la procédure suivante pour déboguer les experts écrits en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Débogage d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523278"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="6fac2-103">Débogage d’un expert</span><span class="sxs-lookup"><span data-stu-id="6fac2-103">Debugging an Expert</span></span>

<span data-ttu-id="6fac2-104">Utilisez la procédure suivante pour déboguer les experts écrits en Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6fac2-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="6fac2-105">**Débogage d’un expert**</span><span class="sxs-lookup"><span data-stu-id="6fac2-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="6fac2-106">Installez l’expert (fichier DLL) et le fichier de base de données du programme (. pdb) générés lorsque vous avez compilé l’expert à l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="6fac2-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="6fac2-107">Pour plus d’informations, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="6fac2-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="6fac2-108">Démarrez Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6fac2-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="6fac2-109">Dans le menu **fichier** , cliquez sur **ouvrir** , puis sélectionnez le nom de votre dll d’expert.</span><span class="sxs-lookup"><span data-stu-id="6fac2-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="6fac2-110">Après le chargement de Microsoft Visual C++, cliquez sur le menu **projet** , puis sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="6fac2-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="6fac2-111">Cliquez sur **Déboguer**.</span><span class="sxs-lookup"><span data-stu-id="6fac2-111">Click **Debug**.</span></span> <span data-ttu-id="6fac2-112">Sous **exécutable pour session de débogage**, tapez le chemin d’accès complet de Netmon.exe, par exemple :</span><span class="sxs-lookup"><span data-stu-id="6fac2-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="6fac2-113">Définissez les points d’arrêt dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6fac2-113">Set the breakpoints in your code.</span></span>

 

 



