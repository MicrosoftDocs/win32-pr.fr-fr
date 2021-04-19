---
description: La propriété balance définit ou récupère le solde du haut-parleur pour la sortie du flux audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propriété balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512872"
---
# <a name="balance-property"></a><span data-ttu-id="fdcd3-103">Propriété balance</span><span class="sxs-lookup"><span data-stu-id="fdcd3-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="fdcd3-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fdcd3-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fdcd3-106">La `Balance` propriété définit ou récupère le solde du haut-parleur pour la sortie du flux audio.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="fdcd3-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fdcd3-107">Return Value</span></span>

<span data-ttu-id="fdcd3-108">Retourne une valeur entière représentant les niveaux de solde.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="fdcd3-109">La plage d’entrée autorisée est comprise entre-10 000 et 10 000.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="fdcd3-110">La valeur 0 définit un équilibre neutre, c’est-à-dire que les haut-parleurs gauche et droit reçoivent le même signal audio amplitude.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdcd3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fdcd3-111">Remarks</span></span>

<span data-ttu-id="fdcd3-112">Cette propriété est en lecture/écriture avec une valeur par défaut de 0, ce qui signifie que les deux enceintes reçoivent des signaux audio équivalents.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="fdcd3-113">Comme avec la propriété [**volume**](volume-property.md) , Units correspond à 0,01 décibels (multiplié par-1 lorsque</span><span class="sxs-lookup"><span data-stu-id="fdcd3-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="fdcd3-114">est une valeur positive).</span><span class="sxs-lookup"><span data-stu-id="fdcd3-114">is a positive value).</span></span> <span data-ttu-id="fdcd3-115">Par exemple, la valeur 1000 indique 10 dB sur le canal droit et 90 dB sur le canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="fdcd3-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



