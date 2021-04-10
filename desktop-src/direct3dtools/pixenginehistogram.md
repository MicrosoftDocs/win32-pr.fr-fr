---
description: Représente un histogramme d’une texture.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineHistogram, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109290"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="75d74-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram, structure</span><span class="sxs-lookup"><span data-stu-id="75d74-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="75d74-104">Représente un histogramme d’une texture.</span><span class="sxs-lookup"><span data-stu-id="75d74-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d74-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="75d74-106">Membres</span><span class="sxs-lookup"><span data-stu-id="75d74-106">Members</span></span>

<span data-ttu-id="75d74-107">**horizontalMin**</span><span class="sxs-lookup"><span data-stu-id="75d74-107">**horizontalMin**</span></span>  
<span data-ttu-id="75d74-108">Valeurs minimales pour chacun des composants X, Y, Z et W dans l’axe horizontal (domaine) de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="75d74-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="75d74-109">**horizontalMax**</span><span class="sxs-lookup"><span data-stu-id="75d74-109">**horizontalMax**</span></span>  
<span data-ttu-id="75d74-110">Valeurs maximales pour chacun des composants X, Y, Z et W dans l’axe horizontal (domaine) de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="75d74-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="75d74-111">**verticalMin**</span><span class="sxs-lookup"><span data-stu-id="75d74-111">**verticalMin**</span></span>  
<span data-ttu-id="75d74-112">Valeurs minimales pour chacun des composants X, Y, Z et W dans l’axe vertical (plage) de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="75d74-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="75d74-113">**verticalMax**</span><span class="sxs-lookup"><span data-stu-id="75d74-113">**verticalMax**</span></span>  
<span data-ttu-id="75d74-114">Valeurs maximales pour chacun des composants X, Y, Z et W dans l’axe vertical (plage) de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="75d74-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="75d74-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="75d74-115">**dataLength**</span></span>  
<span data-ttu-id="75d74-116">Nombre d’échantillons pris en compte dans l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="75d74-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d74-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d74-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="75d74-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="75d74-118">Header</span></span></p></td><td><span data-ttu-id="75d74-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="75d74-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



