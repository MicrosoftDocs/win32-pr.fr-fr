---
title: Modifications apportées à la prise en charge matérielle héritée virtuel DX9
description: Modifications apportées à la prise en charge matérielle héritée virtuel DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106511910"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="0ff1a-103">Modifications apportées à la prise en charge matérielle héritée virtuel DX9</span><span class="sxs-lookup"><span data-stu-id="0ff1a-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="0ff1a-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="0ff1a-104">Platform</span></span>

<span data-ttu-id="0ff1a-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ff1a-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="0ff1a-106">Description</span><span class="sxs-lookup"><span data-stu-id="0ff1a-106">Description</span></span>

<span data-ttu-id="0ff1a-107">Intel et AMD/ATI ne prennent plus en charge leurs composants graphiques virtuel DX9 et ne mettent pas à jour les pilotes de ces appareils pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="0ff1a-108">En outre, ces appareils ne sont pas couverts pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="0ff1a-109">Les derniers pilotes de ces périphériques sont ceux disponibles sur WU et sur les sites Web OEM/IHV. à partir de Vista, beaucoup de ces pilotes de version finale présentent des problèmes sur Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="0ff1a-110">En outre, nVidia a récemment indiqué qu’ils ne prendront pas en charge leurs composants de portable (Vista et plus anciens) mobiles pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="0ff1a-111">Ils continuent à prendre en charge leurs composants Desktop virtuel DX9.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="0ff1a-112">Toutes ces combinaisons de pilotes/parties se trouvent dans la liste de secours des logiciels d’Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="0ff1a-113">Cela signifie que, pour des raisons de performances ou de stabilité, Internet Explorer 9 utilise le rendu logiciel sur ces périphériques.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="0ff1a-114">C’est une bonne indication que l’expérience avec les applications du Windows Store n’est pas satisfaisante sur ces pilotes et parties.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0ff1a-115">Manifestation</span><span class="sxs-lookup"><span data-stu-id="0ff1a-115">Manifestation</span></span>

<span data-ttu-id="0ff1a-116">Comme il n’existe pas de prise en charge intégrée pour ces appareils, de nombreux utilisateurs disposant de ces éléments s’exécutent sur le pilote d’affichage de base de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="0ff1a-117">Il s’agit d’un GPU de logiciel WDDM 1,2 basé sur la distorsion, qui est en fait plus rapide que certains des composants de cette classe, par exemple, la série Intel GMA500.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="0ff1a-118">Il prend en charge Aero-Glass et DWM, et peut exécuter des applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="0ff1a-119">Toutefois, il présente des limitations importantes :</span><span class="sxs-lookup"><span data-stu-id="0ff1a-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="0ff1a-120">Il ne prend pas en charge plusieurs moniteurs ou projection</span><span class="sxs-lookup"><span data-stu-id="0ff1a-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="0ff1a-121">Il ne prend pas en charge le mode veille, bien qu’il prenne en charge la mise en veille prolongée</span><span class="sxs-lookup"><span data-stu-id="0ff1a-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="0ff1a-122">Il n’autorise généralement pas la modification de la résolution d’écran</span><span class="sxs-lookup"><span data-stu-id="0ff1a-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="0ff1a-123">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="0ff1a-123">Mitigation</span></span>

<span data-ttu-id="0ff1a-124">Si, après le test, vous constatez que l’expérience utilisateur n’est pas acceptable, vous pouvez choisir de définir la configuration matérielle requise pour les produits qui excluent ces anciens composants Intel et AMD virtuel DX9.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="0ff1a-125">Vous pouvez également choisir d’alerter vos clients qu’ils peuvent avoir une expérience inacceptable sur ces parties.</span><span class="sxs-lookup"><span data-stu-id="0ff1a-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="0ff1a-126">Tests</span><span class="sxs-lookup"><span data-stu-id="0ff1a-126">Tests</span></span>

<span data-ttu-id="0ff1a-127">Évaluez les performances et l’expérience de ces appareils :</span><span class="sxs-lookup"><span data-stu-id="0ff1a-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="0ff1a-128">Quelle est l’expérience de la version finale du pilote disponible ?</span><span class="sxs-lookup"><span data-stu-id="0ff1a-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="0ff1a-129">Qu’est-ce que l’expérience comme sur le MSBDD ?</span><span class="sxs-lookup"><span data-stu-id="0ff1a-129">What is the experience like on the MSBDD?</span></span>

 

 




