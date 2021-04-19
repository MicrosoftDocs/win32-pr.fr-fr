---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. Les données sont envoyées de l’hôte à l’appareil.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529929"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="2266a-104">Commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ écrire, commande</span><span class="sxs-lookup"><span data-stu-id="2266a-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="2266a-105">La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire** commande envoie un bloc de commande MTP, qui est suivi d’une phase de données.</span><span class="sxs-lookup"><span data-stu-id="2266a-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="2266a-106">Les données sont envoyées de l’hôte à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2266a-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="2266a-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="2266a-107">Command category</span></span>

<span data-ttu-id="2266a-108">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="2266a-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="2266a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2266a-109">Parameters</span></span>

<span data-ttu-id="2266a-110">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2266a-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="2266a-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2266a-111">Parameter</span></span>                                                | <span data-ttu-id="2266a-112">VarType</span><span class="sxs-lookup"><span data-stu-id="2266a-112">VarType</span></span> | <span data-ttu-id="2266a-113">Description</span><span class="sxs-lookup"><span data-stu-id="2266a-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2266a-114">**\_code d' \_ \_ opération ext \_ \_ de la propriété wpd MTP**</span><span class="sxs-lookup"><span data-stu-id="2266a-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="2266a-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2266a-115">VT\_UI4</span></span> | <span data-ttu-id="2266a-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2266a-116">Required.</span></span> <span data-ttu-id="2266a-117">Identifie un code d’opération MTP étendu par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2266a-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="2266a-118">**param, propriété WPD, \_ \_ \_ paramètres d' \_ opération ext \_**</span><span class="sxs-lookup"><span data-stu-id="2266a-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="2266a-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2266a-119">VT\_UI4</span></span> | <span data-ttu-id="2266a-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2266a-120">Required.</span></span> <span data-ttu-id="2266a-121">Collection **IPortableDevicePropVariantCollection** qui identifie les paramètres requis pour le code d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2266a-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="2266a-122">**\_propriété wpd \_ - \_ \_ \_ taille totale des \_ données de transfert ext \_**</span><span class="sxs-lookup"><span data-stu-id="2266a-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="2266a-123">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="2266a-123">VT\_UI8</span></span> | <span data-ttu-id="2266a-124">Obligatoire. spécifie la taille totale des données, en octets, à l’exception de toute surcharge, à envoyer à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2266a-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="2266a-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2266a-125">Return Value</span></span>

<span data-ttu-id="2266a-126">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="2266a-126">The driver returns the following results.</span></span>



| <span data-ttu-id="2266a-127">Résultats</span><span class="sxs-lookup"><span data-stu-id="2266a-127">Result</span></span>                                                       | <span data-ttu-id="2266a-128">VarType</span><span class="sxs-lookup"><span data-stu-id="2266a-128">VarType</span></span>    | <span data-ttu-id="2266a-129">Description</span><span class="sxs-lookup"><span data-stu-id="2266a-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2266a-130">**\_taille de \_ la \_ \_ \_ \_ mémoire tampon de transfert optimal ext \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="2266a-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="2266a-131">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2266a-131">VT\_UI4</span></span>    | <span data-ttu-id="2266a-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2266a-132">Required.</span></span> <span data-ttu-id="2266a-133">Spécifie la taille optimale de la mémoire tampon de transfert.</span><span class="sxs-lookup"><span data-stu-id="2266a-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="2266a-134">**\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="2266a-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="2266a-135">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="2266a-135">VT\_LPWSTR</span></span> | <span data-ttu-id="2266a-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="2266a-136">Optional.</span></span> <span data-ttu-id="2266a-137">Identificateur de contexte utilisé par le pilote pour les transferts de données suivants.</span><span class="sxs-lookup"><span data-stu-id="2266a-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="2266a-138">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="2266a-138">Calling Methods</span></span>

<span data-ttu-id="2266a-139">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="2266a-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="2266a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2266a-140">Requirements</span></span>



| <span data-ttu-id="2266a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2266a-141">Requirement</span></span> | <span data-ttu-id="2266a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="2266a-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2266a-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="2266a-143">Header</span></span><br/> | <dl> <span data-ttu-id="2266a-144"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="2266a-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2266a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2266a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2266a-146">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="2266a-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




