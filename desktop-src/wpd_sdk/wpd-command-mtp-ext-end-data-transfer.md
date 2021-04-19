---
description: La commande WPD de \_ \_ fin de \_ \_ \_ transfert de données de fin MTP MTP \_ termine une réponse de transfert de données et de lecture de l’appareil.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Commande WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540022"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="059e6-103">Commande \_ wpd \_ MTP \_ MTP \_ End \_ Data \_ Transfer</span><span class="sxs-lookup"><span data-stu-id="059e6-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="059e6-104">La commande **wpd de fin de \_ \_ \_ \_ \_ \_ transfert de données de fin MTP MTP** termine une réponse de transfert de données et de lecture de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="059e6-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="059e6-105">Le transfert est initié par la commande [**wpd \_ \_ MTP \_ ext \_ Execute \_ Command, avec les \_ \_ données \_ à \_ lire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) ou la commande [**wpd \_ \_ MTP \_ ext \_ Execute \_ Command avec les \_ \_ données \_ à \_ écrire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) .</span><span class="sxs-lookup"><span data-stu-id="059e6-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="059e6-106">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="059e6-106">Command category</span></span>

<span data-ttu-id="059e6-107">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="059e6-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="059e6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="059e6-108">Parameters</span></span>

<span data-ttu-id="059e6-109">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="059e6-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="059e6-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="059e6-110">Parameter</span></span>                                      | <span data-ttu-id="059e6-111">VarType</span><span class="sxs-lookup"><span data-stu-id="059e6-111">VarType</span></span>    | <span data-ttu-id="059e6-112">Description</span><span class="sxs-lookup"><span data-stu-id="059e6-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="059e6-113">**\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="059e6-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="059e6-114">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="059e6-114">VT\_LPWSTR</span></span> | <span data-ttu-id="059e6-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="059e6-115">Required.</span></span> <span data-ttu-id="059e6-116">Identifie le contexte retourné par un appel de méthode antérieur.</span><span class="sxs-lookup"><span data-stu-id="059e6-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="059e6-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="059e6-117">Return Value</span></span>

<span data-ttu-id="059e6-118">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="059e6-118">The driver returns the following results.</span></span>



| <span data-ttu-id="059e6-119">Résultats</span><span class="sxs-lookup"><span data-stu-id="059e6-119">Result</span></span>                                        | <span data-ttu-id="059e6-120">VarType</span><span class="sxs-lookup"><span data-stu-id="059e6-120">VarType</span></span> | <span data-ttu-id="059e6-121">Description</span><span class="sxs-lookup"><span data-stu-id="059e6-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="059e6-122">**\_Code de \_ \_ réponse MTP \_ ext \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="059e6-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="059e6-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="059e6-123">VT\_UI4</span></span> | <span data-ttu-id="059e6-124">Requis. code de réponse au code d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="059e6-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="059e6-125">**param, propriété WPD, \_ \_ \_ paramètres de \_ réponse ext \_**</span><span class="sxs-lookup"><span data-stu-id="059e6-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="059e6-126">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="059e6-126">VT\_UI4</span></span> | <span data-ttu-id="059e6-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="059e6-127">Optional.</span></span> <span data-ttu-id="059e6-128">Collection **IPortableDevicePropVariantCollection** qui identifie les paramètres de réponse.</span><span class="sxs-lookup"><span data-stu-id="059e6-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="059e6-129">Cette collection peut être vide.</span><span class="sxs-lookup"><span data-stu-id="059e6-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="059e6-130">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="059e6-130">Calling Methods</span></span>

<span data-ttu-id="059e6-131">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="059e6-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="059e6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="059e6-132">Requirements</span></span>



| <span data-ttu-id="059e6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="059e6-133">Requirement</span></span> | <span data-ttu-id="059e6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="059e6-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="059e6-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="059e6-135">Header</span></span><br/> | <dl> <span data-ttu-id="059e6-136"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="059e6-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="059e6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="059e6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059e6-138">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="059e6-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

