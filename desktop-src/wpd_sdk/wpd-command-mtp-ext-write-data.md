---
description: La commande \_ wpd \_ MTP \_ \_ Write ext \_ Data envoie des données à l’appareil après l’exécution de la commande wpd \_ \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Commande WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541646"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="13768-103">Commande \_ wpd \_ MTP \_ ext. \_ écriture de \_ données</span><span class="sxs-lookup"><span data-stu-id="13768-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="13768-104">La **commande \_ wpd \_ MTP \_ \_ Write ext \_ Data** envoie des données à l’appareil après l’exécution de la commande **wpd \_ \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire** .</span><span class="sxs-lookup"><span data-stu-id="13768-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="13768-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="13768-105">Command category</span></span>

<span data-ttu-id="13768-106">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="13768-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="13768-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13768-107">Parameters</span></span>

<span data-ttu-id="13768-108">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="13768-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="13768-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="13768-109">Parameter</span></span>                                                    | <span data-ttu-id="13768-110">VarType</span><span class="sxs-lookup"><span data-stu-id="13768-110">VarType</span></span>             | <span data-ttu-id="13768-111">Description</span><span class="sxs-lookup"><span data-stu-id="13768-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13768-112">**\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="13768-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="13768-113">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="13768-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="13768-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="13768-114">Required.</span></span> <span data-ttu-id="13768-115">Identifie le contexte qui a été retourné par l’appel précédent à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13768-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="13768-116">**\_propriété wpd \_ \_ \_ \_ nombre \_ d’octets de transfert ext MTP \_ à \_ écrire**</span><span class="sxs-lookup"><span data-stu-id="13768-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="13768-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="13768-117">VT\_UI4</span></span>             | <span data-ttu-id="13768-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="13768-118">Required.</span></span> <span data-ttu-id="13768-119">Spécifie le nombre d’octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="13768-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="13768-120">**\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="13768-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="13768-121">VT \_ UI1 VT Vector \| \_</span><span class="sxs-lookup"><span data-stu-id="13768-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="13768-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="13768-122">Required.</span></span> <span data-ttu-id="13768-123">Identifie la mémoire tampon dans laquelle les données de l’appareil sont copiées.</span><span class="sxs-lookup"><span data-stu-id="13768-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="13768-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13768-124">Return Value</span></span>

<span data-ttu-id="13768-125">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="13768-125">The driver returns the following results.</span></span>



| <span data-ttu-id="13768-126">Résultats</span><span class="sxs-lookup"><span data-stu-id="13768-126">Result</span></span>                                                     | <span data-ttu-id="13768-127">VarType</span><span class="sxs-lookup"><span data-stu-id="13768-127">VarType</span></span> | <span data-ttu-id="13768-128">Description</span><span class="sxs-lookup"><span data-stu-id="13768-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="13768-129">**\_propriété wpd \_ nombre d’octets de \_ transfert ext MTP \_ \_ \_ \_ écrits**</span><span class="sxs-lookup"><span data-stu-id="13768-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="13768-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="13768-130">VT\_UI4</span></span> | <span data-ttu-id="13768-131">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="13768-131">Required.</span></span> <span data-ttu-id="13768-132">Spécifie le nombre d’octets envoyés à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13768-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="13768-133">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="13768-133">Calling Methods</span></span>

<span data-ttu-id="13768-134">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="13768-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="13768-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13768-135">Requirements</span></span>



| <span data-ttu-id="13768-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13768-136">Requirement</span></span> | <span data-ttu-id="13768-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="13768-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13768-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="13768-138">Header</span></span><br/> | <dl> <span data-ttu-id="13768-139"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="13768-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13768-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13768-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13768-141">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="13768-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




