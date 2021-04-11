---
title: Fichier d' Module-Definition du lecteur d’installation
description: Fichier d' Module-Definition du lecteur d’installation
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- pilotes installables, fichiers de définition de module
- pilotes installables, fichiers DEF
- pilotes nstallable, fonction DriverProc
- DriverProc fonction)
- fichiers de définition de module
- fichiers DEF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031129"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="2852e-109">Fichier d' Module-Definition du lecteur d’installation</span><span class="sxs-lookup"><span data-stu-id="2852e-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="2852e-110">La définition de module (. DEF) d’un pilote installable nomme le pilote, exporte la fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) et définit une description du pilote.</span><span class="sxs-lookup"><span data-stu-id="2852e-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="2852e-111">L’exemple suivant montre un fichier de définition de module standard pour un pilote installable :</span><span class="sxs-lookup"><span data-stu-id="2852e-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="2852e-112">Certaines applications d’installation peuvent ouvrir le pilote et récupérer la ligne de description à utiliser lors de l’installation du pilote.</span><span class="sxs-lookup"><span data-stu-id="2852e-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="2852e-113">Pour rester compatible avec ces applications d’installation, la ligne de description doit avoir la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="2852e-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="2852e-114">  *Alias* \[ de description,*alias* \] ... **:\* \* * texte*</span><span class="sxs-lookup"><span data-stu-id="2852e-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="2852e-115">L' *alias* spécifie un nom unique pour le pilote que les applications peuvent utiliser pour ouvrir le pilote.</span><span class="sxs-lookup"><span data-stu-id="2852e-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="2852e-116">L’alias sert également de nom de valeur associé au pilote dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2852e-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="2852e-117">Les alias multiples sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="2852e-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="2852e-118">Le *texte* décrit l’objectif du pilote.</span><span class="sxs-lookup"><span data-stu-id="2852e-118">The *text* describes the purpose of the driver.</span></span>

 

 