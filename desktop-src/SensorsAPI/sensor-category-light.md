---
description: La \_ catégorie capteur \_ Light contient des capteurs qui fournissent des informations sur les caractéristiques de Light.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862262"
---
# <a name="sensor_category_light"></a><span data-ttu-id="c92ac-103">catégorie de capteur \_ \_ Light</span><span class="sxs-lookup"><span data-stu-id="c92ac-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="c92ac-104">La \_ catégorie capteur \_ Light contient des capteurs qui fournissent des informations sur les caractéristiques de Light.</span><span class="sxs-lookup"><span data-stu-id="c92ac-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="c92ac-105">**Types de capteurs définis par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="c92ac-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="c92ac-106">Cette catégorie comprend les types de capteurs définis par la plateforme suivants.</span><span class="sxs-lookup"><span data-stu-id="c92ac-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="c92ac-107">Type de capteur</span><span class="sxs-lookup"><span data-stu-id="c92ac-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="c92ac-108">Description</span><span class="sxs-lookup"><span data-stu-id="c92ac-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="c92ac-109"><dt>**Capteur \_ TAPEZ \_ \_ lumière ambiante**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="c92ac-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="c92ac-110">Capteurs de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="c92ac-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="c92ac-111">**Champs de données définis par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="c92ac-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="c92ac-112">Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID clair :</span><span class="sxs-lookup"><span data-stu-id="c92ac-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="c92ac-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="c92ac-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="c92ac-114">Cette catégorie comprend les champs de données définis par la plateforme suivants.</span><span class="sxs-lookup"><span data-stu-id="c92ac-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="c92ac-115">Nom du champ de données et PID</span><span class="sxs-lookup"><span data-stu-id="c92ac-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="c92ac-116">Description</span><span class="sxs-lookup"><span data-stu-id="c92ac-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="c92ac-117"><dt> **Type de données de capteur \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ac-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="c92ac-118">**VT \_ UI1 VT Vector \| \_**</span><span class="sxs-lookup"><span data-stu-id="c92ac-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="c92ac-119">La chromatique est un tableau compté de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="c92ac-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="c92ac-120">Les données des types vectoriels sont toujours sérialisées en tant que **VT \_ UI1** (un tableau de caractères non signés, de 1 octet).</span><span class="sxs-lookup"><span data-stu-id="c92ac-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="c92ac-121">Ce champ de données contient en fait chaque valeur en tant que valeur réelle IEEE de 4 octets (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="c92ac-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="c92ac-122">Pour plus d’informations sur l’utilisation des tableaux, consultez [récupération des types de vecteurs](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="c92ac-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="c92ac-123"><dt>**Capteur \_ TYPE de données de \_ \_ niveau de lumière \_ \_ Lux**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ac-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="c92ac-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="c92ac-124">**VT\_R4**</span></span><br/> <span data-ttu-id="c92ac-125">Niveau d’éclairage, en lux.</span><span class="sxs-lookup"><span data-stu-id="c92ac-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="c92ac-126"><dt>**Capteur \_ TYPE de données- \_ \_ \_ température \_ légère**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ac-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="c92ac-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="c92ac-127">**VT\_R4**</span></span><br/> <span data-ttu-id="c92ac-128">Température de couleur, en degrés Kelvin.</span><span class="sxs-lookup"><span data-stu-id="c92ac-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="c92ac-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c92ac-129">Requirements</span></span>



| <span data-ttu-id="c92ac-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c92ac-130">Requirement</span></span> | <span data-ttu-id="c92ac-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c92ac-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c92ac-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c92ac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c92ac-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c92ac-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c92ac-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c92ac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c92ac-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c92ac-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c92ac-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c92ac-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c92ac-137"><dt>Capteurs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c92ac-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




