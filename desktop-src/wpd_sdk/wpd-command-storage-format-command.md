---
description: La \_ commande de format de stockage de commande wpd \_ \_ met en forme un objet fonctionnel de stockage sur l’appareil.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Commande WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528919"
---
# <a name="wpd_command_storage_format-command"></a><span data-ttu-id="6d17a-103">\_Commande de \_ format de stockage de commande wpd \_</span><span class="sxs-lookup"><span data-stu-id="6d17a-103">WPD\_COMMAND\_STORAGE\_FORMAT Command</span></span>

<span data-ttu-id="6d17a-104">La commande de **\_ format de \_ stockage \_ de commande wpd** met en forme un objet fonctionnel de stockage sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6d17a-104">The **WPD\_COMMAND\_STORAGE\_FORMAT** command formats a storage functional object on the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="6d17a-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="6d17a-105">Command category</span></span>

<span data-ttu-id="6d17a-106">**\_stockage de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="6d17a-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="6d17a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d17a-107">Parameters</span></span>

<span data-ttu-id="6d17a-108">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6d17a-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="6d17a-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6d17a-109">Parameter</span></span>                          | <span data-ttu-id="6d17a-110">VarType</span><span class="sxs-lookup"><span data-stu-id="6d17a-110">VarType</span></span>    | <span data-ttu-id="6d17a-111">Description</span><span class="sxs-lookup"><span data-stu-id="6d17a-111">Description</span></span>                                              |
|------------------------------------|------------|----------------------------------------------------------|
| <span data-ttu-id="6d17a-112">\_ID d' \_ objet de stockage de propriétés wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d17a-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="6d17a-113">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="6d17a-113">VT\_LPWSTR</span></span> | <span data-ttu-id="6d17a-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6d17a-114">Required.</span></span> <span data-ttu-id="6d17a-115">ID d’objet du support de stockage à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="6d17a-115">The object ID of the storage medium to format.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="6d17a-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d17a-116">Return Value</span></span>

<span data-ttu-id="6d17a-117">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="6d17a-117">The driver should return the following results.</span></span>



| <span data-ttu-id="6d17a-118">Résultats</span><span class="sxs-lookup"><span data-stu-id="6d17a-118">Result</span></span>                                         | <span data-ttu-id="6d17a-119">VarType</span><span class="sxs-lookup"><span data-stu-id="6d17a-119">VarType</span></span>   | <span data-ttu-id="6d17a-120">Description</span><span class="sxs-lookup"><span data-stu-id="6d17a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d17a-121">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d17a-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="6d17a-122">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="6d17a-122">VT\_ERROR</span></span> | <span data-ttu-id="6d17a-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6d17a-123">Required.</span></span> <span data-ttu-id="6d17a-124">**HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="6d17a-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="6d17a-125">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="6d17a-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="6d17a-126">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="6d17a-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="6d17a-127">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="6d17a-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="6d17a-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6d17a-128">VT\_UI4</span></span>   | <span data-ttu-id="6d17a-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6d17a-129">Optional.</span></span> <span data-ttu-id="6d17a-130">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="6d17a-130">A driver-specific error code.</span></span> <span data-ttu-id="6d17a-131">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="6d17a-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="6d17a-132">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="6d17a-132">Calling Methods</span></span>

<span data-ttu-id="6d17a-133">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="6d17a-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d17a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d17a-134">Requirements</span></span>



| <span data-ttu-id="6d17a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d17a-135">Requirement</span></span> | <span data-ttu-id="6d17a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d17a-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d17a-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d17a-137">Header</span></span><br/> | <dl> <span data-ttu-id="6d17a-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d17a-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d17a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d17a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d17a-140">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="6d17a-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




