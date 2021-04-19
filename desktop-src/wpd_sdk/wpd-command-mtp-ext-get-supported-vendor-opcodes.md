---
description: La commande \_ wpd \_ MTP \_ ext \_ \_ prise en charge des OpCodes du fournisseur de la commande wpd \_ \_ envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Commande WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543259"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="92b78-104">Commande \_ wpd \_ MTP \_ MTP \_ afficher \_ les \_ OpCodes fournisseur pris en charge \_</span><span class="sxs-lookup"><span data-stu-id="92b78-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="92b78-105">La **commande \_ wpd \_ MTP \_ ext \_ \_ prise en charge des \_ \_ OpCodes du fournisseur de la commande wpd** envoie un bloc de commande MTP.</span><span class="sxs-lookup"><span data-stu-id="92b78-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="92b78-106">Aucune phase de données ultérieure n’est associée à cette commande.</span><span class="sxs-lookup"><span data-stu-id="92b78-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="92b78-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="92b78-107">Command category</span></span>

<span data-ttu-id="92b78-108">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="92b78-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="92b78-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92b78-109">Parameters</span></span>

<span data-ttu-id="92b78-110">Cette commande n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="92b78-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92b78-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="92b78-111">Return Value</span></span>

<span data-ttu-id="92b78-112">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="92b78-112">The driver returns the following results.</span></span>



| <span data-ttu-id="92b78-113">Résultats</span><span class="sxs-lookup"><span data-stu-id="92b78-113">Result</span></span>                                                | <span data-ttu-id="92b78-114">VarType</span><span class="sxs-lookup"><span data-stu-id="92b78-114">VarType</span></span> | <span data-ttu-id="92b78-115">Description</span><span class="sxs-lookup"><span data-stu-id="92b78-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b78-116">**\_codes d' \_ \_ opération du \_ fournisseur ext MTP \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="92b78-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="92b78-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="92b78-117">VT\_UI4</span></span> | <span data-ttu-id="92b78-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="92b78-118">Required.</span></span> <span data-ttu-id="92b78-119">**IPortableDevicePropVariantCollection** qui contient tous les codes d’opération étendus par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="92b78-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="92b78-120">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="92b78-120">Calling Methods</span></span>

<span data-ttu-id="92b78-121">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="92b78-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="92b78-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92b78-122">Requirements</span></span>



| <span data-ttu-id="92b78-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92b78-123">Requirement</span></span> | <span data-ttu-id="92b78-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="92b78-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b78-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="92b78-125">Header</span></span><br/> | <dl> <span data-ttu-id="92b78-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b78-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b78-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b78-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b78-128">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="92b78-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




