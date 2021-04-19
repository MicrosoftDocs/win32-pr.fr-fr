---
title: Constantes IMAPi
description: IMAPi définit les constantes suivantes.
ms.assetid: 3ae67227-1cee-4e9c-a7fe-228de596030a
topic_type:
- apiref
api_name:
- IMAPI_SECTOR_SIZE
- IMAPI_SECTORS_PER_SECOND_AT_1X_CD
- IMAPI_SECTORS_PER_SECOND_AT_1X_DVD
- IMAPI_SECTORS_PER_SECOND_AT_1X_BD
api_location:
- Imapi2.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb8c6ac1d855509e67ce5e066410f107172d2ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518058"
---
# <a name="imapi-constants"></a><span data-ttu-id="a653b-103">Constantes IMAPi</span><span class="sxs-lookup"><span data-stu-id="a653b-103">IMAPI Constants</span></span>

<span data-ttu-id="a653b-104">IMAPi définit les constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a653b-104">IMAPI defines the following constants.</span></span>



| <span data-ttu-id="a653b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a653b-105">Constant</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="a653b-106">Description</span><span class="sxs-lookup"><span data-stu-id="a653b-106">Description</span></span>                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="IMAPI_SECTOR_SIZE"></span><span id="imapi_sector_size"></span><dl> <span data-ttu-id="a653b-107"><dt>**taille de \_ secteur IMAPI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a653b-107"><dt>**IMAPI\_SECTOR\_SIZE**</dt></span></span> </dl>                                                        | <span data-ttu-id="a653b-108">Nombre d’octets dans un secteur.</span><span class="sxs-lookup"><span data-stu-id="a653b-108">Number of bytes in a sector.</span></span><br/>                                                  |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_CD"></span><span id="imapi_sectors_per_second_at_1x_cd"></span><dl> <span data-ttu-id="a653b-109"><dt>**\_Secteurs IMAPI \_ par \_ seconde \_ sur \_ \_ CD 1x**</dt></span><span class="sxs-lookup"><span data-stu-id="a653b-109"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_CD**</dt></span></span> </dl>    | <span data-ttu-id="a653b-110">Taux de base de la vitesse de rotation d’un CD, mesuré en secteurs par seconde.</span><span class="sxs-lookup"><span data-stu-id="a653b-110">Base rate of speed that a CD spins, measured in sectors per second.</span></span><br/>           |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_DVD"></span><span id="imapi_sectors_per_second_at_1x_dvd"></span><dl> <span data-ttu-id="a653b-111"><dt>**\_Secteurs IMAPI \_ par \_ seconde \_ sur \_ un \_ DVD 1x**</dt></span><span class="sxs-lookup"><span data-stu-id="a653b-111"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_DVD**</dt></span></span> </dl> | <span data-ttu-id="a653b-112">Taux de base de la vitesse de rotation d’un DVD, mesuré en secteurs par seconde.</span><span class="sxs-lookup"><span data-stu-id="a653b-112">Base rate of speed that a DVD spins, measured in sectors per second.</span></span><br/>          |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_BD"></span><span id="imapi_sectors_per_second_at_1x_bd"></span><dl> <span data-ttu-id="a653b-113"><dt>**\_Secteurs IMAPI \_ par \_ seconde \_ sur \_ 1x \_ BD**</dt></span><span class="sxs-lookup"><span data-stu-id="a653b-113"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_BD**</dt></span></span> </dl>    | <span data-ttu-id="a653b-114">Taux de base de la vitesse de rotation d’un disque Blu-Ray, mesuré en secteurs par seconde.</span><span class="sxs-lookup"><span data-stu-id="a653b-114">Base rate of speed that a Blu-ray disc spins, measured in sectors per second.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a653b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a653b-115">Requirements</span></span>



| <span data-ttu-id="a653b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a653b-116">Requirement</span></span> | <span data-ttu-id="a653b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a653b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a653b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a653b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a653b-119">Windows Vista, Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a653b-119">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a653b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a653b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a653b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a653b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a653b-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="a653b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a653b-123"><dt>Imapi2. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a653b-123"><dt>Imapi2.idl</dt></span></span> </dl> |



 

 





