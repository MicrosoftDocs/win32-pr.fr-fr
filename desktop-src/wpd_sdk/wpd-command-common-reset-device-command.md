---
description: La commande de \_ réinitialisation d’appareil pour la commande wpd réinitialise \_ \_ \_ l’appareil. Cela ne signifie pas de reformatage ; Cela équivaut à éteindre et rallumer l’appareil.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Commande WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521775"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="c890d-104">Commande WPD- \_ \_ commande de \_ réinitialisation d' \_ appareil courante</span><span class="sxs-lookup"><span data-stu-id="c890d-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="c890d-105">La commande de **\_ \_ \_ réinitialisation d' \_ appareil pour la commande wpd** réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c890d-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="c890d-106">Cela ne signifie pas de reformatage ; Cela équivaut à éteindre et rallumer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c890d-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="c890d-107">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="c890d-107">Command category</span></span>

<span data-ttu-id="c890d-108">**WPD, \_ catégorie \_ commune**</span><span class="sxs-lookup"><span data-stu-id="c890d-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="c890d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c890d-109">Parameters</span></span>

<span data-ttu-id="c890d-110">Cette commande n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c890d-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c890d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c890d-111">Return Value</span></span>

<span data-ttu-id="c890d-112">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="c890d-112">The driver should return the following results.</span></span>



| <span data-ttu-id="c890d-113">Résultats</span><span class="sxs-lookup"><span data-stu-id="c890d-113">Result</span></span>                                         | <span data-ttu-id="c890d-114">VarType</span><span class="sxs-lookup"><span data-stu-id="c890d-114">VarType</span></span>   | <span data-ttu-id="c890d-115">Description</span><span class="sxs-lookup"><span data-stu-id="c890d-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c890d-116">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c890d-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="c890d-117">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="c890d-117">VT\_ERROR</span></span> | <span data-ttu-id="c890d-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c890d-118">Required.</span></span> <span data-ttu-id="c890d-119">**HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="c890d-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="c890d-120">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="c890d-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="c890d-121">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="c890d-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="c890d-122">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="c890d-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="c890d-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c890d-123">VT\_UI4</span></span>   | <span data-ttu-id="c890d-124">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c890d-124">Optional.</span></span> <span data-ttu-id="c890d-125">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="c890d-125">A driver-specific error code.</span></span> <span data-ttu-id="c890d-126">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="c890d-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="c890d-127">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="c890d-127">Calling Methods</span></span>

<span data-ttu-id="c890d-128">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="c890d-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c890d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c890d-129">Requirements</span></span>



| <span data-ttu-id="c890d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c890d-130">Requirement</span></span> | <span data-ttu-id="c890d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c890d-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c890d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c890d-132">Header</span></span><br/> | <dl> <span data-ttu-id="c890d-133"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c890d-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c890d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c890d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c890d-135">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="c890d-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




