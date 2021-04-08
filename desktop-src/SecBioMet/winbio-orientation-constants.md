---
title: Constantes WINBIO_ORIENTATION ( \_ types WINBIO. h)
description: Les constantes suivantes spécifient les orientations d’appareil photo possibles que le composant capteur spécifie comme étant obligatoires.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844382"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="9a23e-103">\_Constantes d’orientation WINBIO</span><span class="sxs-lookup"><span data-stu-id="9a23e-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="9a23e-104">Les constantes suivantes spécifient les orientations d’appareil photo possibles que le composant capteur spécifie comme étant obligatoires.</span><span class="sxs-lookup"><span data-stu-id="9a23e-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="9a23e-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="9a23e-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="9a23e-106">Description</span><span class="sxs-lookup"><span data-stu-id="9a23e-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="9a23e-107"><dt>**WINBIO \_ ORIENTATION \_ non spécifiée**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9a23e-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9a23e-108">Une orientation obligatoire pour l’appareil photo n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9a23e-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="9a23e-109"><dt>**WINBIO \_ ORIENTATION \_ paysage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9a23e-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="9a23e-110">L’orientation paysage est requise pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9a23e-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="9a23e-111"><dt>**WINBIO \_ ORIENTATION \_ portrait**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9a23e-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="9a23e-112">L’orientation portrait est requise pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9a23e-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="9a23e-113"><dt>**WINBIO \_ ORIENTATION \_ any**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9a23e-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="9a23e-114">Toute orientation est autorisée pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9a23e-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="9a23e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a23e-115">Requirements</span></span>



| <span data-ttu-id="9a23e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a23e-116">Requirement</span></span> | <span data-ttu-id="9a23e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a23e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a23e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a23e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a23e-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a23e-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="9a23e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a23e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a23e-121">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a23e-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="9a23e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a23e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a23e-123"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="9a23e-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a23e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a23e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a23e-125">**\_ \_ informations sur le capteur étendu WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9a23e-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





