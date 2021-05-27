---
title: D1102 trop de handles ouverts
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Un grand nombre d’interfaces qui n’ont pas été publiées ont été trouvées. Actuellement, il existe des interfaces non libérées allouées par cette DLL.
keywords:
- D1102 trop grand nombre de handles ouverts Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548684"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="0d17a-105">D1102 : trop de handles ouverts</span><span class="sxs-lookup"><span data-stu-id="0d17a-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="0d17a-106">Un grand nombre d’interfaces qui n’ont pas été publiées ont été trouvées.</span><span class="sxs-lookup"><span data-stu-id="0d17a-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="0d17a-107">Actuellement, il \[ *existe des* \] interfaces non libérées allouées par cette dll.</span><span class="sxs-lookup"><span data-stu-id="0d17a-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="0d17a-108">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="0d17a-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="0d17a-109"><span id="number"></span><span id="NUMBER"></span>*certain*</span><span class="sxs-lookup"><span data-stu-id="0d17a-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="0d17a-110">Nombre d’interfaces non libérées allouées par cette DLL.</span><span class="sxs-lookup"><span data-stu-id="0d17a-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="0d17a-111">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="0d17a-111">Error Level</span></span> | <span data-ttu-id="0d17a-112">Avertissement</span><span class="sxs-lookup"><span data-stu-id="0d17a-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="0d17a-113">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="0d17a-113">Possible Causes</span></span>

<span data-ttu-id="0d17a-114">Un grand nombre de ressources ont été créées.</span><span class="sxs-lookup"><span data-stu-id="0d17a-114">A large number of resources were created.</span></span> <span data-ttu-id="0d17a-115">Bien que Direct2D n’ait aucune limite supérieure quant au nombre de ressources disponibles (à l’exception de la mémoire), la couche de débogage émet ce message d’information lorsqu’il rencontre des objets actifs 1001, des objets en direct 2001, ou 3001 des objets actifs, etc. en effet, cela peut indiquer une fuite dans l’application.</span><span class="sxs-lookup"><span data-stu-id="0d17a-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




