---
title: Le système d’exploitation contrôle désormais les lecteurs de disque optique
description: Le système d’exploitation contrôle désormais les lecteurs de disque optique
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730733"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="853ae-103">Le système d’exploitation contrôle désormais les lecteurs de disque optique</span><span class="sxs-lookup"><span data-stu-id="853ae-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="853ae-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="853ae-104">Platforms</span></span>

<span data-ttu-id="853ae-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="853ae-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="853ae-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="853ae-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="853ae-107">Description</span><span class="sxs-lookup"><span data-stu-id="853ae-107">Description</span></span>

<span data-ttu-id="853ae-108">Dans les versions précédentes de Windows, la mise sous tension du lecteur optique n’était pas gérée lorsque le lecteur optique n’était pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="853ae-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="853ae-109">Si aucun support n’est présent dans le lecteur de disque optique (impair), le système d’exploitation éteint l’alimentation du lecteur optique.</span><span class="sxs-lookup"><span data-stu-id="853ae-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="853ae-110">Cette fonctionnalité est appelée Zero Power impaire (ZPODD).</span><span class="sxs-lookup"><span data-stu-id="853ae-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="853ae-111">Cette fonctionnalité s’applique uniquement aux lecteurs optiques qui utilisent un connecteur SATA (Serial Advanced Technology Attachment).</span><span class="sxs-lookup"><span data-stu-id="853ae-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="853ae-112">Manifestation</span><span class="sxs-lookup"><span data-stu-id="853ae-112">Manifestation</span></span>

<span data-ttu-id="853ae-113">Nous n’avons pas trouvé d’impact négatif sur ce nouveau comportement ; Toutefois, vous devez en être conscient, car cela peut entraîner un comportement inattendu du logiciel d’écriture de médias.</span><span class="sxs-lookup"><span data-stu-id="853ae-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="853ae-114">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="853ae-114">Mitigation</span></span>

<span data-ttu-id="853ae-115">Pour revenir à l’État Always on, désactivez cette fonctionnalité dans le registre.</span><span class="sxs-lookup"><span data-stu-id="853ae-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="853ae-116">Le chemin d’accès absolu à la valeur de Registre est :</span><span class="sxs-lookup"><span data-stu-id="853ae-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="853ae-117">Son type est DWORD (32 bits), et si sa valeur est 0, ZPODD est désactivé. s’il s’agit d’une autre valeur, ZPODD est activé.</span><span class="sxs-lookup"><span data-stu-id="853ae-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="853ae-118">Tests</span><span class="sxs-lookup"><span data-stu-id="853ae-118">Tests</span></span>

<span data-ttu-id="853ae-119">Testez votre logiciel d’écriture multimédia pour toutes les anomalies qui se produisent en raison de cette nouvelle fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="853ae-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="853ae-120">Veuillez [informer Microsoft](mailto:OptIssue@microsoft.com) de tous les problèmes que vous rencontrez avec cette nouvelle fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="853ae-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




