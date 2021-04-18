---
description: La \_ commande de \_ capture d’image continue de la commande wpd \_ \_ \_ lance une capture d’image continue par un objet fonctionnel d’image continue. Si un nouvel objet est créé suite à la capture d’une image, le pilote doit envoyer l’événement de l' \_ objet d’événement wpd \_ \_ ajouté.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Commande WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526696"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="8bb1e-104">\_Commande d' \_ \_ initialisation de capture d’image continue \_ de la commande wpd \_</span><span class="sxs-lookup"><span data-stu-id="8bb1e-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="8bb1e-105">La commande de **\_ \_ capture d' \_ image \_ \_ continue de la commande wpd** lance une capture d’image continue par un objet fonctionnel d’image continue.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="8bb1e-106">Si un nouvel objet est créé suite à la capture d’une image, le pilote doit envoyer l’événement de l' **\_ objet d’événement wpd \_ \_ ajouté** .</span><span class="sxs-lookup"><span data-stu-id="8bb1e-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="8bb1e-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="8bb1e-107">Command category</span></span>

<span data-ttu-id="8bb1e-108">**\_capture d' \_ \_ image continue de catégorie \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="8bb1e-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="8bb1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bb1e-109">Parameters</span></span>

<span data-ttu-id="8bb1e-110">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8bb1e-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="8bb1e-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8bb1e-111">Parameter</span></span>                              | <span data-ttu-id="8bb1e-112">VarType</span><span class="sxs-lookup"><span data-stu-id="8bb1e-112">VarType</span></span>    | <span data-ttu-id="8bb1e-113">Description</span><span class="sxs-lookup"><span data-stu-id="8bb1e-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb1e-114">\_cible de \_ la \_ commande \_ commune de la propriété wpd</span><span class="sxs-lookup"><span data-stu-id="8bb1e-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="8bb1e-115">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="8bb1e-115">VT\_LPWSTR</span></span> | <span data-ttu-id="8bb1e-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-116">Required.</span></span> <span data-ttu-id="8bb1e-117">ID d’objet de l’objet fonctionnel de capture d’image continue sur l’appareil qui doit prendre l’image. Chaque objet fonctionnel de capture d’images continues peut avoir des paramètres différents et peut faire référence à un matériel différent sur un appareil (par exemple, un appareil photo avant ou arrière d’un téléphone) et ce paramètre indique celui à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8bb1e-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bb1e-118">Return Value</span></span>

<span data-ttu-id="8bb1e-119">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-119">The driver should return the following results.</span></span>



| <span data-ttu-id="8bb1e-120">Résultats</span><span class="sxs-lookup"><span data-stu-id="8bb1e-120">Result</span></span>                                         | <span data-ttu-id="8bb1e-121">VarType</span><span class="sxs-lookup"><span data-stu-id="8bb1e-121">VarType</span></span>   | <span data-ttu-id="8bb1e-122">Description</span><span class="sxs-lookup"><span data-stu-id="8bb1e-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb1e-123">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8bb1e-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="8bb1e-124">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="8bb1e-124">VT\_ERROR</span></span> | <span data-ttu-id="8bb1e-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-125">Required.</span></span> <span data-ttu-id="8bb1e-126">**HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="8bb1e-127">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="8bb1e-128">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="8bb1e-129">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="8bb1e-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="8bb1e-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="8bb1e-130">VT\_UI4</span></span>   | <span data-ttu-id="8bb1e-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-131">Optional.</span></span> <span data-ttu-id="8bb1e-132">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-132">A driver-specific error code.</span></span> <span data-ttu-id="8bb1e-133">Cette valeur est généralement utilisée par les fournisseurs de périphériques pour améliorer le diagnostic des erreurs d’appareil lors de l’utilisation de leurs applications.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="8bb1e-134">Les applications à usage général l’ignorent et s’appuient uniquement sur la propriété WPD de \_ \_ HRESULT commun à la \_ place.</span><span class="sxs-lookup"><span data-stu-id="8bb1e-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="8bb1e-135">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="8bb1e-135">Calling Methods</span></span>

<span data-ttu-id="8bb1e-136">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="8bb1e-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb1e-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bb1e-137">Requirements</span></span>



| <span data-ttu-id="8bb1e-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bb1e-138">Requirement</span></span> | <span data-ttu-id="8bb1e-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bb1e-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb1e-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bb1e-140">Header</span></span><br/> | <dl> <span data-ttu-id="8bb1e-141"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb1e-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb1e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bb1e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb1e-143">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="8bb1e-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




