---
description: La catégorie de l' \_ Analyseur de catégorie de capteur \_ contient des capteurs qui fournissent des informations obtenues par analyse.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951068"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="7c2ee-103">\_scanneur de catégorie de capteur \_</span><span class="sxs-lookup"><span data-stu-id="7c2ee-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="7c2ee-104">La catégorie de l' \_ Analyseur de catégorie de capteur \_ contient des capteurs qui fournissent des informations obtenues par analyse.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="7c2ee-105">**Types de capteurs définis par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="7c2ee-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="7c2ee-106">Cette catégorie comprend les types de capteurs définis par la plateforme suivants.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="7c2ee-107">Type de capteur</span><span class="sxs-lookup"><span data-stu-id="7c2ee-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="7c2ee-108">Description</span><span class="sxs-lookup"><span data-stu-id="7c2ee-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="7c2ee-109"><dt>**Capteur \_ TAPEZ le \_ \_ scanneur de codes-barres**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ee-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="7c2ee-110">Capteurs qui utilisent l’analyse optique pour lire les codes-barres.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="7c2ee-111"><dt>**Capteur \_ TAPEZ \_ le \_ scanneur RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ee-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="7c2ee-112">Capteurs d’analyse d’ID de fréquence radio.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="7c2ee-113">**Champs de données définis par la plateforme**</span><span class="sxs-lookup"><span data-stu-id="7c2ee-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="7c2ee-114">Les clés de propriété définies par la plateforme pour cette catégorie sont basées sur le \_ \_ GUID du scanneur du type de données du capteur \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="7c2ee-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="7c2ee-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="7c2ee-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="7c2ee-116">Cette catégorie comprend les champs de données définis par la plateforme suivants.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="7c2ee-117">Nom du champ de données et PID</span><span class="sxs-lookup"><span data-stu-id="7c2ee-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="7c2ee-118">Description</span><span class="sxs-lookup"><span data-stu-id="7c2ee-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="7c2ee-119"><dt>**Capteur \_ TYPE de données \_ \_ \_ étiquette RFID \_ 40 \_ bit**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ee-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="7c2ee-120">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="7c2ee-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="7c2ee-121">valeur de la balise d’ID de fréquence radio 40 bits.</span><span class="sxs-lookup"><span data-stu-id="7c2ee-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7c2ee-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c2ee-122">Requirements</span></span>



| <span data-ttu-id="7c2ee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c2ee-123">Requirement</span></span> | <span data-ttu-id="7c2ee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c2ee-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2ee-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c2ee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2ee-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c2ee-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c2ee-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c2ee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2ee-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c2ee-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="7c2ee-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c2ee-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2ee-130"><dt>Capteurs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ee-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




