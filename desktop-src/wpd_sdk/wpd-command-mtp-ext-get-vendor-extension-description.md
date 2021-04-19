---
description: La commande \_ wpd \_ MTP MTP ext extension de la description de l' \_ \_ extension de \_ fournisseur \_ \_ récupère la chaîne de description du fournisseur. Cette chaîne est définie par un jeu de données DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Commande WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539978"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="f3323-104">Commande \_ wpd \_ MTP \_ ext \_ \_ \_ extension \_ de la description de l’extension de fournisseur</span><span class="sxs-lookup"><span data-stu-id="f3323-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="f3323-105">La **commande \_ wpd \_ MTP MTP \_ ext \_ \_ \_ extension \_** de la description de l’extension de fournisseur récupère la chaîne de description du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f3323-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="f3323-106">Cette chaîne est définie par un jeu de données **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="f3323-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="f3323-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="f3323-107">Command category</span></span>

<span data-ttu-id="f3323-108">**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**</span><span class="sxs-lookup"><span data-stu-id="f3323-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="f3323-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3323-109">Parameters</span></span>

<span data-ttu-id="f3323-110">Cette commande n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3323-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3323-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3323-111">Return Value</span></span>

<span data-ttu-id="f3323-112">Le pilote retourne les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="f3323-112">The driver returns the following results.</span></span>



| <span data-ttu-id="f3323-113">Résultats</span><span class="sxs-lookup"><span data-stu-id="f3323-113">Result</span></span>                                                      | <span data-ttu-id="f3323-114">VarType</span><span class="sxs-lookup"><span data-stu-id="f3323-114">VarType</span></span>    | <span data-ttu-id="f3323-115">Description</span><span class="sxs-lookup"><span data-stu-id="f3323-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="f3323-116">**propriété WPD-Description de l' \_ \_ \_ extension de fournisseur ext MTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3323-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="f3323-117">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="f3323-117">VT\_LPWSTR</span></span> | <span data-ttu-id="f3323-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f3323-118">Required.</span></span> <span data-ttu-id="f3323-119">Spécifie la chaîne de description de l’extension de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f3323-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="f3323-120">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="f3323-120">Calling Methods</span></span>

<span data-ttu-id="f3323-121">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f3323-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3323-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3323-122">Requirements</span></span>



| <span data-ttu-id="f3323-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3323-123">Requirement</span></span> | <span data-ttu-id="f3323-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3323-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3323-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3323-125">Header</span></span><br/> | <dl> <span data-ttu-id="f3323-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3323-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3323-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3323-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3323-128">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="f3323-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




