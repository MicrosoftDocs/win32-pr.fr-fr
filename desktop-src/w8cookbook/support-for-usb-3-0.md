---
title: Prise en charge de la norme USB 3,0
description: Prise en charge de la norme USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730757"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="b41f8-103">Prise en charge de la norme USB 3,0</span><span class="sxs-lookup"><span data-stu-id="b41f8-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="b41f8-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="b41f8-104">Platforms</span></span>

<span data-ttu-id="b41f8-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="b41f8-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="b41f8-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b41f8-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="b41f8-107">Description</span><span class="sxs-lookup"><span data-stu-id="b41f8-107">Description</span></span>

<span data-ttu-id="b41f8-108">Dans Windows 8 et Windows Server 2012, nous avons ajouté la prise en charge de la norme USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b41f8-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="b41f8-109">Pour ce faire, nous avons ajouté une nouvelle pile logicielle pour alimenter le contrôleur hôte USB 3,0, appelé contrôleur hôte eXtensible (XHC).</span><span class="sxs-lookup"><span data-stu-id="b41f8-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="b41f8-110">Nous avons conservé l’interface Parity, le niveau IRQL, le contexte de l’appelant, l’état d’erreur, la fréquence des tentatives, etc.</span><span class="sxs-lookup"><span data-stu-id="b41f8-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="b41f8-111">Il ne devrait y avoir aucune différence lors de l’interaction avec un appareil connecté via USB 2,0 et USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b41f8-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="b41f8-112">Toutefois, si vous écrivez un pilote pour un nouvel appareil USB 3,0, optez pour les nouvelles fonctionnalités USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b41f8-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b41f8-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="b41f8-113">Manifestation</span></span>

<span data-ttu-id="b41f8-114">Les transferts d’appareils sont plus rapides et moins puissantes à partir d’un PC par des périphériques USB.</span><span class="sxs-lookup"><span data-stu-id="b41f8-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="b41f8-115">Il existe un risque que les périphériques USB existants ne fonctionnent pas correctement lorsqu’ils sont connectés à un port USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="b41f8-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="b41f8-116">Cela ne devrait pas se produire et n’est pas attendu, mais, étant donné que le logiciel qui alimente USB 3,0 est nouveau, il est risqué.</span><span class="sxs-lookup"><span data-stu-id="b41f8-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




