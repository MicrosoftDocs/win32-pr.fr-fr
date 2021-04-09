---
description: La méthode TakePicture de l’objet Item fait qu’un appareil photo numérique prend une image et retourne un objet Item qui représente l’image résultante. Cette méthode s’applique uniquement aux appareils photo numériques.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Item. TakePicture, méthode (wiavideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952067"
---
# <a name="itemtakepicture-method"></a><span data-ttu-id="e6fe2-104">Item. TakePicture, méthode</span><span class="sxs-lookup"><span data-stu-id="e6fe2-104">Item.TakePicture method</span></span>

<span data-ttu-id="e6fe2-105">La méthode **TakePicture** de l’objet [**Item**](-wia-item.md) fait qu’un appareil photo numérique prend une image et retourne un objet **Item** qui représente l’image résultante.</span><span class="sxs-lookup"><span data-stu-id="e6fe2-105">The **TakePicture** method of the [**Item**](-wia-item.md) object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="e6fe2-106">Cette méthode s’applique uniquement aux appareils photo numériques.</span><span class="sxs-lookup"><span data-stu-id="e6fe2-106">This method applies only to digital camera devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fe2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6fe2-107">Syntax</span></span>


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a><span data-ttu-id="e6fe2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6fe2-108">Parameters</span></span>

<span data-ttu-id="e6fe2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6fe2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6fe2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6fe2-110">Return value</span></span>

<span data-ttu-id="e6fe2-111">Type : **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="e6fe2-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="e6fe2-112">Objet d' [**élément**](-wia-item.md) qui représente l’image créée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e6fe2-112">An [**Item**](-wia-item.md) object that represents the image that this method creates.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6fe2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6fe2-113">Requirements</span></span>



| <span data-ttu-id="e6fe2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6fe2-114">Requirement</span></span> | <span data-ttu-id="e6fe2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6fe2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fe2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6fe2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6fe2-117">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6fe2-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6fe2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6fe2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6fe2-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6fe2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e6fe2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6fe2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6fe2-121"><dt>Wiavideo. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6fe2-121"><dt>Wiavideo.h</dt></span></span> </dl>                         |
| <span data-ttu-id="e6fe2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e6fe2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6fe2-123"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e6fe2-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




