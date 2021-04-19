---
title: StorAHCI remplace MSAHCI
description: StorAHCI remplace MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106510913"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="7a3ca-103">StorAHCI remplace MSAHCI</span><span class="sxs-lookup"><span data-stu-id="7a3ca-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="7a3ca-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="7a3ca-104">Platforms</span></span>

<span data-ttu-id="7a3ca-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a3ca-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="7a3ca-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a3ca-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="7a3ca-107">Description</span><span class="sxs-lookup"><span data-stu-id="7a3ca-107">Description</span></span>

<span data-ttu-id="7a3ca-108">StorAHCI, un miniport Storport, prend en charge les contrôleurs d’interface de contrôleur d’hôte (AHCI) avancés SATA dans Windows et remplace MSAHCI, un miniport ATAport.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7a3ca-109">Manifestation</span><span class="sxs-lookup"><span data-stu-id="7a3ca-109">Manifestation</span></span>

<span data-ttu-id="7a3ca-110">Il ne doit y avoir aucune modification de la fonctionnalité ou des performances. ce pilote prend en charge tous les appareils pris en charge par MSAHCI.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="7a3ca-111">Cette modification est transparente pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7a3ca-112">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="7a3ca-112">Mitigation</span></span>

<span data-ttu-id="7a3ca-113">Mettez à jour tous les utilitaires et scripts qui reposent sur des liaisons ATAport.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="7a3ca-114">Ne vous fiez pas au nom du lecteur.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-114">Do not rely on the drive name.</span></span> <span data-ttu-id="7a3ca-115">Utilisez plutôt la détection de disque standard.</span><span class="sxs-lookup"><span data-stu-id="7a3ca-115">Instead use standard disk detection.</span></span>

 

 




