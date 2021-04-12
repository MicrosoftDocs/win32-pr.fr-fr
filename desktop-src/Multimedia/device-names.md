---
title: Noms des appareils
description: Noms des appareils
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462470"
---
# <a name="device-names"></a><span data-ttu-id="1393d-103">Noms des appareils</span><span class="sxs-lookup"><span data-stu-id="1393d-103">Device Names</span></span>

<span data-ttu-id="1393d-104">Pour chaque type d’appareil, il peut y avoir plusieurs pilotes MCI qui partagent le jeu de commandes, mais qui opèrent sur des formats de données différents.</span><span class="sxs-lookup"><span data-stu-id="1393d-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="1393d-105">Pour identifier un pilote MCI de manière unique, MCI utilise des *noms d’appareils*.</span><span class="sxs-lookup"><span data-stu-id="1393d-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="1393d-106">Les noms des appareils sont identifiés dans \[ la \] section MCI du fichier SYSTEM.INI ou dans la partie appropriée du Registre.</span><span class="sxs-lookup"><span data-stu-id="1393d-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="1393d-107">Ces informations identifient tous les pilotes MCI sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1393d-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="1393d-108">Les entrées de la \[ \] section MCI utilisent la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="1393d-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="1393d-109">*\_ nom du périphérique* nom  =  *\_ du pilote. extension*</span><span class="sxs-lookup"><span data-stu-id="1393d-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="1393d-110">L’exemple suivant montre une \[ section MCI classique \] de SYSTEM.INI :</span><span class="sxs-lookup"><span data-stu-id="1393d-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="1393d-111">Si un pilote MCI est installé à l’aide d’un nom d’appareil qui existe déjà dans SYSTEM.INI ou dans le registre, le système ajoute un entier au nom du périphérique du nouveau pilote, en créant un nom d’appareil unique.</span><span class="sxs-lookup"><span data-stu-id="1393d-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="1393d-112">Dans l’exemple précédent, un pilote supplémentaire installé à l’aide du nom de l’appareil « cdaudio » se voit attribuer le nom de l’appareil « cdaudio1 ».</span><span class="sxs-lookup"><span data-stu-id="1393d-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




