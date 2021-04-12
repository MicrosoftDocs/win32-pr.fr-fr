---
description: La propriété ColorKey définit ou récupère la clé de couleur utilisée dans le sous-titrage.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propriété ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481177"
---
# <a name="colorkey-property"></a><span data-ttu-id="8d1fe-103">Propriété ColorKey</span><span class="sxs-lookup"><span data-stu-id="8d1fe-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="8d1fe-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8d1fe-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8d1fe-106">La `ColorKey` propriété définit ou récupère la clé de couleur utilisée dans le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="8d1fe-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d1fe-107">Return Value</span></span>

<span data-ttu-id="8d1fe-108">Retourne une valeur entière représentant la couleur à utiliser comme arrière-plan transparent pour le texte de légende fermée.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="8d1fe-109">La valeur par défaut dans les couleurs 256 est magenta, et non noir dans toute autre profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1fe-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8d1fe-110">Remarks</span></span>

<span data-ttu-id="8d1fe-111">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-111">This property is read/write.</span></span> <span data-ttu-id="8d1fe-112">Cette propriété s’applique uniquement aux légendes fermées, le cas échéant, et non au flux de sous-image.</span><span class="sxs-lookup"><span data-stu-id="8d1fe-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



