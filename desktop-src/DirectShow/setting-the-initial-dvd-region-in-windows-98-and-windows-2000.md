---
description: Définition de la région du DVD initial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Définition de la région du DVD initial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520388"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="4a4f9-103">Définition de la région du DVD initial</span><span class="sxs-lookup"><span data-stu-id="4a4f9-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="4a4f9-104">Il incombe au fabricant du système de sélectionner une région de DVD initiale pour le lecteur de DVD dans leurs PC.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="4a4f9-105">Seuls les disques chiffrés peuvent être utilisés pour définir la région.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="4a4f9-106">Windows 2000 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="4a4f9-106">Windows 2000 and Later</span></span>

<span data-ttu-id="4a4f9-107">À partir de Windows 2000, la région DVD par défaut est sélectionnée en fonction des paramètres régionaux pour lesquels la machine est configurée.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="4a4f9-108">Windows 2000 définit toujours la région initiale pour un lecteur de DVD à l’aide de cette région par défaut, ainsi que de la région du disque, si un disque se trouve dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="4a4f9-109">Le fabricant du système n’a rien à faire pour définir la région initiale pour les lecteurs de DVD Windows 2000 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="4a4f9-110">Pour les lecteurs RPC1, s’il n’y a pas de disque dans le lecteur lors du démarrage, la région par défaut est définie uniquement en fonction des paramètres régionaux de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="4a4f9-111">S’il y a un disque DVD dans le lecteur lors du démarrage, la région par défaut est sélectionnée pour être la région du lecteur, à condition qu’elle corresponde à une région du disque. dans le cas contraire, la région la plus basse sur le disque est choisie comme région initiale du lecteur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="4a4f9-112">L’utilisateur (ou le fabricant du système) a une modification restante autorisée, si la valeur par défaut n’était pas correcte.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="4a4f9-113">Pour les lecteurs RPC2, si au cours du processus d’installation, Windows 2000 constate que le lecteur n’a pas de région définie, il tente de sélectionner une région comme indiqué ci-dessus, mais uniquement s’il y a un disque dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="4a4f9-114">(Les lecteurs RPC1 choisissent la région sans disque dans le lecteur).</span><span class="sxs-lookup"><span data-stu-id="4a4f9-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="4a4f9-115">Une fois qu’une région est définie pour les lecteurs RPC2, elle n’est pas modifiée automatiquement par une réinstallation ou une nouvelle installation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="4a4f9-116">L’OEM peut définir une clé de registre contenant la région du DVD par défaut pour le système.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="4a4f9-117">Au premier démarrage, la région du lecteur sera définie sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="4a4f9-118">La clé de Registre sur Windows 2000 et versions ultérieures est HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).</span><span class="sxs-lookup"><span data-stu-id="4a4f9-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a4f9-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a4f9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a4f9-120">Prise en charge des modifications de région de DVD dans Windows</span><span class="sxs-lookup"><span data-stu-id="4a4f9-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



