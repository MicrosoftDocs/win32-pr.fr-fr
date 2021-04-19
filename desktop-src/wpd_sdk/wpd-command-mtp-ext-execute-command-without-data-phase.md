---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans \_ \_ commande Data phase envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526368"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="ec750-104">Commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans \_ \_ commande Data phase</span><span class="sxs-lookup"><span data-stu-id="ec750-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="ec750-105">La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans commande \_ Data \_ phase** envoie un bloc de commande MTP.</span><span class="sxs-lookup"><span data-stu-id="ec750-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="ec750-106">Aucune phase de données ultérieure n’est associée à cette commande.</span><span class="sxs-lookup"><span data-stu-id="ec750-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="ec750-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="ec750-107">Command category</span></span>

<span data-ttu-id="ec750-108">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="ec750-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="ec750-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec750-109">Parameters</span></span>

<span data-ttu-id="ec750-110">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ec750-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="ec750-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ec750-111">Parameter</span></span>                                      | <span data-ttu-id="ec750-112">VarType</span><span class="sxs-lookup"><span data-stu-id="ec750-112">VarType</span></span> | <span data-ttu-id="ec750-113">Description</span><span class="sxs-lookup"><span data-stu-id="ec750-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec750-114">**\_code d' \_ \_ opération ext \_ \_ de la propriété wpd MTP**</span><span class="sxs-lookup"><span data-stu-id="ec750-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="ec750-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ec750-115">VT\_UI4</span></span> | <span data-ttu-id="ec750-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ec750-116">Required.</span></span> <span data-ttu-id="ec750-117">Identifie un code d’opération MTP étendu par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec750-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="ec750-118">**param, propriété WPD, \_ \_ \_ paramètres d' \_ opération ext \_**</span><span class="sxs-lookup"><span data-stu-id="ec750-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="ec750-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ec750-119">VT\_UI4</span></span> | <span data-ttu-id="ec750-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ec750-120">Required.</span></span> <span data-ttu-id="ec750-121">Un **IPortableDevicePropVariantCollection**, qui identifie les paramètres requis pour le code d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec750-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="ec750-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec750-122">Return Value</span></span>

<span data-ttu-id="ec750-123">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="ec750-123">The driver returns the following results.</span></span>



| <span data-ttu-id="ec750-124">Résultats</span><span class="sxs-lookup"><span data-stu-id="ec750-124">Result</span></span>                                        | <span data-ttu-id="ec750-125">VarType</span><span class="sxs-lookup"><span data-stu-id="ec750-125">VarType</span></span> | <span data-ttu-id="ec750-126">Description</span><span class="sxs-lookup"><span data-stu-id="ec750-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec750-127">**\_Code de \_ \_ réponse MTP \_ ext \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="ec750-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="ec750-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ec750-128">VT\_UI4</span></span> | <span data-ttu-id="ec750-129">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ec750-129">Required.</span></span> <span data-ttu-id="ec750-130">Code de réponse au code d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec750-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="ec750-131">**param, propriété WPD, \_ \_ \_ paramètres de \_ réponse ext \_**</span><span class="sxs-lookup"><span data-stu-id="ec750-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="ec750-132">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ec750-132">VT\_UI4</span></span> | <span data-ttu-id="ec750-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ec750-133">Optional.</span></span> <span data-ttu-id="ec750-134">**IPortableDevicePropVariantCollection** qui identifie les paramètres de réponse.</span><span class="sxs-lookup"><span data-stu-id="ec750-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="ec750-135">Cette collection peut être vide.</span><span class="sxs-lookup"><span data-stu-id="ec750-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="ec750-136">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="ec750-136">Calling Methods</span></span>

<span data-ttu-id="ec750-137">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="ec750-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec750-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec750-138">Requirements</span></span>



| <span data-ttu-id="ec750-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec750-139">Requirement</span></span> | <span data-ttu-id="ec750-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec750-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec750-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec750-141">Header</span></span><br/> | <dl> <span data-ttu-id="ec750-142"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec750-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec750-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec750-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec750-144">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="ec750-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




