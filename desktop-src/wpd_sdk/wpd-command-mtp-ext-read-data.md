---
description: La commande \_ wpd \_ MTP \_ ext \_ Read \_ Data de la commande wpd récupère les données de l’appareil après l’exécution de la commande wpd \_ \_ MTP \_ ext \_ Execute \_ \_ , avec les \_ données \_ à \_ lire.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Commande WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526575"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="d3291-103">Commande \_ wpd \_ MTP de lecture de \_ données MTP ext \_ \_</span><span class="sxs-lookup"><span data-stu-id="d3291-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="d3291-104">La **commande \_ wpd \_ MTP \_ ext \_ Read \_ Data** de la commande wpd récupère les données de l’appareil après l’exécution de la commande **wpd \_ \_ MTP \_ ext \_ Execute, \_ avec les \_ \_ données \_ à \_ lire** .</span><span class="sxs-lookup"><span data-stu-id="d3291-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="d3291-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="d3291-105">Command category</span></span>

<span data-ttu-id="d3291-106">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="d3291-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="d3291-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3291-107">Parameters</span></span>

<span data-ttu-id="d3291-108">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d3291-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="d3291-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d3291-109">Parameter</span></span>                                                   | <span data-ttu-id="d3291-110">VarType</span><span class="sxs-lookup"><span data-stu-id="d3291-110">VarType</span></span>             | <span data-ttu-id="d3291-111">Description</span><span class="sxs-lookup"><span data-stu-id="d3291-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3291-112">**\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="d3291-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="d3291-113">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="d3291-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="d3291-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3291-114">Required.</span></span> <span data-ttu-id="d3291-115">Identifie le contexte qui a été retourné par l’appel précédent à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3291-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="d3291-116">**\_propriété wpd \_ \_ \_ \_ nombre \_ d’octets de transfert ext \_ à \_ lire**</span><span class="sxs-lookup"><span data-stu-id="d3291-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="d3291-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d3291-117">VT\_UI4</span></span>             | <span data-ttu-id="d3291-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3291-118">Required.</span></span> <span data-ttu-id="d3291-119">Spécifie le nombre d’octets à lire.</span><span class="sxs-lookup"><span data-stu-id="d3291-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="d3291-120">**\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="d3291-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="d3291-121">VT \_ UI1 VT Vector \| \_</span><span class="sxs-lookup"><span data-stu-id="d3291-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="d3291-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3291-122">Required.</span></span> <span data-ttu-id="d3291-123">Identifie la mémoire tampon dans laquelle les données de l’appareil sont copiées.</span><span class="sxs-lookup"><span data-stu-id="d3291-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="d3291-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d3291-124">Return Value</span></span>

<span data-ttu-id="d3291-125">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="d3291-125">The driver returns the following results.</span></span>



| <span data-ttu-id="d3291-126">Résultats</span><span class="sxs-lookup"><span data-stu-id="d3291-126">Result</span></span>                                                  | <span data-ttu-id="d3291-127">VarType</span><span class="sxs-lookup"><span data-stu-id="d3291-127">VarType</span></span>             | <span data-ttu-id="d3291-128">Description</span><span class="sxs-lookup"><span data-stu-id="d3291-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d3291-129">**\_propriété wpd \_ nombre \_ d' \_ octets de transfert ext de transfert MTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d3291-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="d3291-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d3291-130">VT\_UI4</span></span>             | <span data-ttu-id="d3291-131">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3291-131">Required.</span></span> <span data-ttu-id="d3291-132">Spécifie le nombre d’octets reçus à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3291-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="d3291-133">**\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**</span><span class="sxs-lookup"><span data-stu-id="d3291-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="d3291-134">VT \_ UI1 VT Vector \| \_</span><span class="sxs-lookup"><span data-stu-id="d3291-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="d3291-135">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3291-135">Required.</span></span> <span data-ttu-id="d3291-136">Mémoire tampon qui contient les données de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3291-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="d3291-137">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="d3291-137">Calling Methods</span></span>

<span data-ttu-id="d3291-138">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="d3291-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3291-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3291-139">Requirements</span></span>



| <span data-ttu-id="d3291-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3291-140">Requirement</span></span> | <span data-ttu-id="d3291-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3291-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3291-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3291-142">Header</span></span><br/> | <dl> <span data-ttu-id="d3291-143"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3291-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3291-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3291-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3291-145">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="d3291-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




