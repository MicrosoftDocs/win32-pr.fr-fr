---
description: Vsdiagview et Vssagent sont des outils que vous pouvez utiliser pour dépanner des applications VSS. Notez que ces outils sont inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Utilisation des diagnostics VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514185"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="778d4-103">Utilisation des diagnostics VSS</span><span class="sxs-lookup"><span data-stu-id="778d4-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="778d4-104">Vsdiagview et Vssagent sont des outils que vous pouvez utiliser pour dépanner des applications VSS.</span><span class="sxs-lookup"><span data-stu-id="778d4-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="778d4-105">Ces outils sont inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="778d4-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="778d4-106">Vous pouvez télécharger le SDK Windows à partir de [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="778d4-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="778d4-107">Dans l’installation SDK Windows, ces outils se trouvent dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour Windows 32 bits).</span><span class="sxs-lookup"><span data-stu-id="778d4-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="778d4-108">Collecte de données</span><span class="sxs-lookup"><span data-stu-id="778d4-108">Gathering Data</span></span>

<span data-ttu-id="778d4-109">Vous pouvez collecter des données à l’aide de la commande Vssagent.</span><span class="sxs-lookup"><span data-stu-id="778d4-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="778d4-110">**Pour collecter des données à l’aide de Vssagent**</span><span class="sxs-lookup"><span data-stu-id="778d4-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="778d4-111">Pour collecter des données à partir de la ligne de commande, utilisez la commande Vssagent comme suit :</span><span class="sxs-lookup"><span data-stu-id="778d4-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="778d4-112">**vssagent-rassembler** *xmlFileName \* \* *. xml**</span><span class="sxs-lookup"><span data-stu-id="778d4-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="778d4-113">Pour afficher le fichier de sortie, consultez la section Affichage des données suivante.</span><span class="sxs-lookup"><span data-stu-id="778d4-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="778d4-114">Affichage des données</span><span class="sxs-lookup"><span data-stu-id="778d4-114">Viewing Data</span></span>

<span data-ttu-id="778d4-115">L’application Vsdiagview peut être utilisée pour afficher les données qui ont été collectées à l’aide de la commande Vssagent.</span><span class="sxs-lookup"><span data-stu-id="778d4-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="778d4-116">Vsdiagview affiche les informations suivantes sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="778d4-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="778d4-117">Informations sur l’ordinateur, telles que la version du système d’exploitation, la mémoire totale disponible et la vitesse du processeur</span><span class="sxs-lookup"><span data-stu-id="778d4-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="778d4-118">Noms et numéros de version des fichiers binaires VSS</span><span class="sxs-lookup"><span data-stu-id="778d4-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="778d4-119">Les noms et les propriétés des périphériques de disque et de volume</span><span class="sxs-lookup"><span data-stu-id="778d4-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="778d4-120">Noms et propriétés de toutes les applications COM+</span><span class="sxs-lookup"><span data-stu-id="778d4-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="778d4-121">Noms des journaux des événements qui peuvent être utilisés pour diagnostiquer les problèmes VSS</span><span class="sxs-lookup"><span data-stu-id="778d4-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="778d4-122">Les noms de tous les enregistreurs VSS et les événements qu’ils gèrent</span><span class="sxs-lookup"><span data-stu-id="778d4-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="778d4-123">Informations sur les autres fichiers de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="778d4-123">Information about other operating system files</span></span>

<span data-ttu-id="778d4-124">**Pour afficher les données à l’aide de Vsdiagview**</span><span class="sxs-lookup"><span data-stu-id="778d4-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="778d4-125">Dans le menu fichier, choisissez **ouvrir** pour rechercher un fichier.</span><span class="sxs-lookup"><span data-stu-id="778d4-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="778d4-126">(L’emplacement par défaut est C : \\ vssdiag.)</span><span class="sxs-lookup"><span data-stu-id="778d4-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="778d4-127">Cliquez sur **ouvrir** pour afficher les données.</span><span class="sxs-lookup"><span data-stu-id="778d4-127">Click **Open** to view the data.</span></span>

 

 



