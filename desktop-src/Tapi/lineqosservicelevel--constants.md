---
description: Ces constantes sont utilisées par un TSP pour identifier le type de niveau de qualité de service (QoS) requis.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534824"
---
# <a name="lineqosservicelevel_-constants"></a><span data-ttu-id="7d163-103">\_Constantes LINEQOSSERVICELEVEL</span><span class="sxs-lookup"><span data-stu-id="7d163-103">LINEQOSSERVICELEVEL\_ Constants</span></span>

<span data-ttu-id="7d163-104">Ces constantes sont utilisées par un TSP pour identifier le type de niveau de qualité de service (QoS) requis.</span><span class="sxs-lookup"><span data-stu-id="7d163-104">These constants are used by a TSP to identify the type of a QoS (Quality of Service) level required.</span></span>

<dl> <dt>

<span data-ttu-id="7d163-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="7d163-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="7d163-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d163-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="7d163-107">Le niveau de qualité de service demandé est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d163-107">The quality of service level requested is a requirement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d163-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="7d163-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL\_IFAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="7d163-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7d163-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="7d163-110">Niveau de qualité de service requis, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="7d163-110">The quality of service level required, if available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d163-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**</span><span class="sxs-lookup"><span data-stu-id="7d163-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL\_BESTEFFORT**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="7d163-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7d163-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="7d163-113">Le niveau de qualité de service requis est « meilleur effort ».</span><span class="sxs-lookup"><span data-stu-id="7d163-113">The quality of service level required is "best effort."</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d163-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d163-114">Requirements</span></span>



| <span data-ttu-id="7d163-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d163-115">Requirement</span></span> | <span data-ttu-id="7d163-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d163-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7d163-117">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7d163-117">TAPI version</span></span><br/> | <span data-ttu-id="7d163-118">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="7d163-118">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="7d163-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d163-119">Header</span></span><br/>       | <dl> <span data-ttu-id="7d163-120"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d163-120"><dt>Tspi.h</dt></span></span> </dl> |



 

 




