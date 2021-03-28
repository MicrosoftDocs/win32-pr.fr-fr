---
title: Informations sur le pilote de périphérique
description: Les pilotes de périphérique et les modules sont similaires en ce sens qu’ils sont tous deux basés sur des fichiers PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028834"
---
# <a name="device-driver-information"></a><span data-ttu-id="fa1c2-103">Informations sur le pilote de périphérique</span><span class="sxs-lookup"><span data-stu-id="fa1c2-103">Device Driver Information</span></span>

<span data-ttu-id="fa1c2-104">Les pilotes de périphérique et les modules sont similaires en ce sens qu’ils sont tous deux basés sur des fichiers PE.</span><span class="sxs-lookup"><span data-stu-id="fa1c2-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="fa1c2-105">Toutefois, bien que chaque processus possède sa propre liste privée de modules chargés, les pilotes de périphérique ont des modules qui sont globaux pour le système.</span><span class="sxs-lookup"><span data-stu-id="fa1c2-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="fa1c2-106">Par conséquent, PSAPI possède des fonctions spécifiques pour obtenir la liste des pilotes de périphériques et leurs noms.</span><span class="sxs-lookup"><span data-stu-id="fa1c2-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="fa1c2-107">Vous pouvez récupérer l’adresse de chargement de chaque pilote de périphérique en appelant la fonction [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) .</span><span class="sxs-lookup"><span data-stu-id="fa1c2-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="fa1c2-108">Cette fonction remplit un tableau de valeurs **LPVOID** avec les adresses de chargement de tous les pilotes de périphérique dans le système.</span><span class="sxs-lookup"><span data-stu-id="fa1c2-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="fa1c2-109">La fonction [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) prend une adresse de chargement de pilote comme entrée et remplit une mémoire tampon avec le nom de base du pilote (par exemple, Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="fa1c2-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="fa1c2-110">Une fonction associée, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), accepte les mêmes paramètres et retourne le chemin d’accès au pilote de périphérique (par exemple, C : \\ Windows \\ system32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="fa1c2-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




