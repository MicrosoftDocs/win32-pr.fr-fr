---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ lire commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. (Les données sont envoyées de l’appareil à l’ordinateur hôte.)
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545576"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="020aa-104">Commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ lire, commande</span><span class="sxs-lookup"><span data-stu-id="020aa-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="020aa-105">La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ lire** commande envoie un bloc de commande MTP, qui est suivi d’une phase de données.</span><span class="sxs-lookup"><span data-stu-id="020aa-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="020aa-106">(Les données sont envoyées de l’appareil à l’hôte.)</span><span class="sxs-lookup"><span data-stu-id="020aa-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="020aa-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="020aa-107">Command category</span></span>

<span data-ttu-id="020aa-108">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="020aa-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="020aa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="020aa-109">Parameters</span></span>

<span data-ttu-id="020aa-110">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="020aa-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="020aa-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="020aa-111">Parameter</span></span>                                      | <span data-ttu-id="020aa-112">VarType</span><span class="sxs-lookup"><span data-stu-id="020aa-112">VarType</span></span> | <span data-ttu-id="020aa-113">Description</span><span class="sxs-lookup"><span data-stu-id="020aa-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020aa-114">**\_code d' \_ \_ opération ext \_ \_ de la propriété wpd MTP**</span><span class="sxs-lookup"><span data-stu-id="020aa-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="020aa-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="020aa-115">VT\_UI4</span></span> | <span data-ttu-id="020aa-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="020aa-116">Required.</span></span> <span data-ttu-id="020aa-117">Identifie un code d’opération MTP étendu par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="020aa-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="020aa-118">**param, propriété WPD, \_ \_ \_ paramètres d' \_ opération ext \_**</span><span class="sxs-lookup"><span data-stu-id="020aa-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="020aa-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="020aa-119">VT\_UI4</span></span> | <span data-ttu-id="020aa-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="020aa-120">Required.</span></span> <span data-ttu-id="020aa-121">Un **IPortableDevicePropVariantCollection**, qui identifie les paramètres requis pour le code d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="020aa-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="020aa-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="020aa-122">Return Value</span></span>

<span data-ttu-id="020aa-123">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="020aa-123">The driver returns the following results.</span></span>



| <span data-ttu-id="020aa-124">Résultats</span><span class="sxs-lookup"><span data-stu-id="020aa-124">Result</span></span>                                                       | <span data-ttu-id="020aa-125">VarType</span><span class="sxs-lookup"><span data-stu-id="020aa-125">VarType</span></span>    | <span data-ttu-id="020aa-126">Description</span><span class="sxs-lookup"><span data-stu-id="020aa-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020aa-127">**\_propriété wpd \_ - \_ \_ \_ taille totale des \_ données de transfert ext \_**</span><span class="sxs-lookup"><span data-stu-id="020aa-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="020aa-128">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="020aa-128">VT\_UI8</span></span>    | <span data-ttu-id="020aa-129">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="020aa-129">Required.</span></span> <span data-ttu-id="020aa-130">Retourne la taille totale des données, en octets, à l’exclusion de toute surcharge provenant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="020aa-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="020aa-131">Si l’appareil signale une DataSize inconnue (0xFFFFFFFF), le pilote doit appeler **ReadData** à plusieurs reprises jusqu’à ce qu’un petit bloc soit reçu.</span><span class="sxs-lookup"><span data-stu-id="020aa-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="020aa-132">**\_taille de \_ la \_ \_ \_ \_ mémoire tampon de transfert optimal ext \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="020aa-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="020aa-133">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="020aa-133">VT\_UI4</span></span>    | <span data-ttu-id="020aa-134">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="020aa-134">Optional.</span></span> <span data-ttu-id="020aa-135">Retourne la taille optimale de la mémoire tampon de transfert.</span><span class="sxs-lookup"><span data-stu-id="020aa-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="020aa-136">**\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="020aa-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="020aa-137">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="020aa-137">VT\_LPWSTR</span></span> | <span data-ttu-id="020aa-138">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="020aa-138">Required.</span></span> <span data-ttu-id="020aa-139">Spécifie l’identificateur de contexte pour les transferts de données suivants.</span><span class="sxs-lookup"><span data-stu-id="020aa-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="020aa-140">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="020aa-140">Calling Methods</span></span>

<span data-ttu-id="020aa-141">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="020aa-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="020aa-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="020aa-142">Requirements</span></span>



| <span data-ttu-id="020aa-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="020aa-143">Requirement</span></span> | <span data-ttu-id="020aa-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="020aa-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="020aa-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="020aa-145">Header</span></span><br/> | <dl> <span data-ttu-id="020aa-146"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="020aa-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="020aa-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="020aa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="020aa-148">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="020aa-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




