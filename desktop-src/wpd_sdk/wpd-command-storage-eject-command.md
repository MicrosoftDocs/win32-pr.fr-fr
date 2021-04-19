---
description: La \_ \_ commande d’éjection du stockage de commande wpd \_ éjecte un support de stockage qui peut être éjecté à distance par l’ordinateur.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Commande WPD_COMMAND_STORAGE_EJECT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539294"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="1e4fe-103">\_Commande wpd \_ stockage commande \_ EJECT</span><span class="sxs-lookup"><span data-stu-id="1e4fe-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="1e4fe-104">La commande d' **\_ éjection du \_ stockage \_ de commande wpd** éjecte un support de stockage qui peut être éjecté à distance par l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="1e4fe-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="1e4fe-105">Command category</span></span>

<span data-ttu-id="1e4fe-106">**\_stockage de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e4fe-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="1e4fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e4fe-107">Parameters</span></span>

<span data-ttu-id="1e4fe-108">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1e4fe-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="1e4fe-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e4fe-109">Parameter</span></span>                          | <span data-ttu-id="1e4fe-110">VarType</span><span class="sxs-lookup"><span data-stu-id="1e4fe-110">VarType</span></span>    | <span data-ttu-id="1e4fe-111">Description</span><span class="sxs-lookup"><span data-stu-id="1e4fe-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="1e4fe-112">\_ID d' \_ objet de stockage de propriétés wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e4fe-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="1e4fe-113">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="1e4fe-113">VT\_LPWSTR</span></span> | <span data-ttu-id="1e4fe-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-114">Required.</span></span> <span data-ttu-id="1e4fe-115">ID d’objet de l’objet de stockage à éjecter.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="1e4fe-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e4fe-116">Return Value</span></span>

<span data-ttu-id="1e4fe-117">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-117">The driver should return the following results.</span></span>



| <span data-ttu-id="1e4fe-118">Résultats</span><span class="sxs-lookup"><span data-stu-id="1e4fe-118">Result</span></span>                                         | <span data-ttu-id="1e4fe-119">VarType</span><span class="sxs-lookup"><span data-stu-id="1e4fe-119">VarType</span></span>   | <span data-ttu-id="1e4fe-120">Description</span><span class="sxs-lookup"><span data-stu-id="1e4fe-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4fe-121">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e4fe-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="1e4fe-122">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="1e4fe-122">VT\_ERROR</span></span> | <span data-ttu-id="1e4fe-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-123">Required.</span></span> <span data-ttu-id="1e4fe-124">**HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="1e4fe-125">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="1e4fe-126">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="1e4fe-127">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="1e4fe-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="1e4fe-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1e4fe-128">VT\_UI4</span></span>   | <span data-ttu-id="1e4fe-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-129">Optional.</span></span> <span data-ttu-id="1e4fe-130">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-130">A driver-specific error code.</span></span> <span data-ttu-id="1e4fe-131">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="1e4fe-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="1e4fe-132">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="1e4fe-132">Calling Methods</span></span>

<span data-ttu-id="1e4fe-133">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="1e4fe-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4fe-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e4fe-134">Requirements</span></span>



| <span data-ttu-id="1e4fe-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e4fe-135">Requirement</span></span> | <span data-ttu-id="1e4fe-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e4fe-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4fe-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e4fe-137">Header</span></span><br/> | <dl> <span data-ttu-id="1e4fe-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4fe-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e4fe-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e4fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4fe-140">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="1e4fe-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




