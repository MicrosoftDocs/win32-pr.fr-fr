---
description: L' \_ \_ autre catégorie de capteur contient des capteurs qui prennent en charge la classe personnalisée dans le pilote de classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033918"
---
# <a name="sensor_category_other"></a><span data-ttu-id="08032-103">catégorie de capteur \_ \_ autre</span><span class="sxs-lookup"><span data-stu-id="08032-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="08032-104">L' \_ \_ autre catégorie de capteur contient des capteurs qui prennent en charge la classe personnalisée dans le pilote de classe HID.</span><span class="sxs-lookup"><span data-stu-id="08032-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="08032-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**TYPE de capteur \_ \_ personnalisé**</span><span class="sxs-lookup"><span data-stu-id="08032-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08032-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="08032-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="08032-107">Capteur personnalisé qui prend en charge la classe personnalisée dans le pilote de classe HID.</span><span class="sxs-lookup"><span data-stu-id="08032-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="08032-108">**Champs de données définis par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="08032-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="08032-109">Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le type de données de capteur \_ \_ \_ \_ GUID personnalisé :</span><span class="sxs-lookup"><span data-stu-id="08032-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="08032-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="08032-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="08032-111">Cette catégorie comprend les champs de données définis par la plateforme suivants.</span><span class="sxs-lookup"><span data-stu-id="08032-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="08032-112">Nom du champ de données et PID</span><span class="sxs-lookup"><span data-stu-id="08032-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="08032-113">Description</span><span class="sxs-lookup"><span data-stu-id="08032-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="08032-114"><dt>**Capteur \_ \_ \_ \_ Utilisation personnalisée du type de données**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="08032-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="08032-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="08032-116">Utilisation HID qui peut être utilisée pour distinguer plusieurs capteurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="08032-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="08032-117"><dt>**Capteur \_ \_Type de \_ données \_ \_ tableau booléen personnalisé**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="08032-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="08032-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="08032-119">Tableau de valeurs booléennes pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="08032-120"><dt>**Capteur \_ \_Type de \_ données \_ value1 personnalisée**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="08032-121">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-122">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="08032-123"><dt>**Capteur \_ \_Type de \_ données \_ value2 personnalisé**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="08032-124">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-125">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="08032-126"><dt>**Capteur \_ \_Type de \_ données \_ valeur3 personnalisé**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="08032-127">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-128">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="08032-129"><dt>**Capteur \_ \_Type de \_ données \_ VALUE4 personnalisé**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="08032-130">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-131">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="08032-132"><dt>**Capteur \_ \_Type de \_ données \_ VALUE5 personnalisé**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="08032-133">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-134">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="08032-135"><dt>**Capteur \_ \_Type de \_ données \_ VALUE6 personnalisé**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="08032-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="08032-136">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="08032-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="08032-137">L’une des six valeurs disponibles pour un capteur personnalisé donné.</span><span class="sxs-lookup"><span data-stu-id="08032-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="08032-138">Notes</span><span class="sxs-lookup"><span data-stu-id="08032-138">Remarks</span></span>

<span data-ttu-id="08032-139">Un capteur qui prend en charge la classe générique dans le pilote de classe HID est mappé à l’une des autres catégories définies (biométrique, électrique, environnement, etc.).</span><span class="sxs-lookup"><span data-stu-id="08032-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="08032-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08032-140">Requirements</span></span>



| <span data-ttu-id="08032-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08032-141">Requirement</span></span> | <span data-ttu-id="08032-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="08032-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08032-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08032-143">Minimum supported client</span></span><br/> | <span data-ttu-id="08032-144">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08032-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08032-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08032-145">Minimum supported server</span></span><br/> | <span data-ttu-id="08032-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="08032-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="08032-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="08032-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="08032-148"><dt>Capteurs. h</dt></span><span class="sxs-lookup"><span data-stu-id="08032-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




