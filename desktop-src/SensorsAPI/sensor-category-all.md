---
description: La catégorie \_ capteur \_ tout représente l’ensemble de toutes les catégories de capteurs définies par la plateforme.
ms.assetid: e2d9fe6d-450a-446b-968b-0924116af6fe
title: SENSOR_CATEGORY_ALL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2e5641e51dde130cc51d9b2fc35fcc1e158ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750820"
---
# <a name="sensor_category_all"></a><span data-ttu-id="b711c-103">\_catégorie \_ tout du capteur</span><span class="sxs-lookup"><span data-stu-id="b711c-103">SENSOR\_CATEGORY\_ALL</span></span>

<span data-ttu-id="b711c-104">La catégorie \_ capteur \_ tout représente l’ensemble de toutes les catégories de capteurs définies par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="b711c-104">The SENSOR\_CATEGORY\_ALL category represents the set of all platform-defined sensor categories.</span></span>

<span data-ttu-id="b711c-105">**Clés de propriété définies par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="b711c-105">**Platform-Defined Property Keys**</span></span>

<span data-ttu-id="b711c-106">Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID commun :</span><span class="sxs-lookup"><span data-stu-id="b711c-106">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_COMMON\_GUID:</span></span>

<span data-ttu-id="b711c-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span><span class="sxs-lookup"><span data-stu-id="b711c-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span></span>

<span data-ttu-id="b711c-108">Le tableau suivant décrit les champs de données définis par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="b711c-108">The following table describes platform-defined data fields.</span></span>



| <span data-ttu-id="b711c-109">Nom du champ de données et PID</span><span class="sxs-lookup"><span data-stu-id="b711c-109">Data field name and PID</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="b711c-110">Description</span><span class="sxs-lookup"><span data-stu-id="b711c-110">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_TIMESTAMP"></span><span id="sensor_data_type_timestamp"></span><dl> <span data-ttu-id="b711c-111"><dt>**Capteur \_ \_ \_ Horodatage du type de données**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="b711c-111"><dt>**SENSOR\_DATA\_TYPE\_TIMESTAMP**</dt> <dt>(PID = 2 ) </dt></span></span> </dl> | <span data-ttu-id="b711c-112">**de VT \_ fileTime**</span><span class="sxs-lookup"><span data-stu-id="b711c-112">**VT\_FILETIME**</span></span><br/> <span data-ttu-id="b711c-113">Obligatoire pour tous les rapports de données.</span><span class="sxs-lookup"><span data-stu-id="b711c-113">Required for all data reports.</span></span> <span data-ttu-id="b711c-114">Marque chaque rapport de données avec l’heure à laquelle le rapport de données a été créé au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="b711c-114">Marks each data report with the time the data report was created in Coordinated Universal Time (UTC) format.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b711c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b711c-115">Requirements</span></span>



| <span data-ttu-id="b711c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b711c-116">Requirement</span></span> | <span data-ttu-id="b711c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b711c-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b711c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b711c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b711c-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b711c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b711c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b711c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b711c-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b711c-121">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b711c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b711c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b711c-123"><dt>Capteurs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b711c-123"><dt>Sensors.h</dt></span></span> </dl> |



 

 




