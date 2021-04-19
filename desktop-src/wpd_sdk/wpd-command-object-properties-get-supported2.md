---
description: Récupère les propriétés prises en charge par un objet.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Commande WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543858"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="dab1c-103">Propriétés de l' \_ objet de commande wpd \_ recevoir une \_ \_ \_ commande prise en charge</span><span class="sxs-lookup"><span data-stu-id="dab1c-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="dab1c-104">La commande propriétés de l' **\_ objet de commande wpd obtenir la \_ \_ \_ \_ prise en charge** récupère les propriétés prises en charge par un objet.</span><span class="sxs-lookup"><span data-stu-id="dab1c-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="dab1c-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="dab1c-105">Command Category</span></span>

<span data-ttu-id="dab1c-106">**Propriétés de l' \_ objet de catégorie wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dab1c-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="dab1c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dab1c-107">Parameters</span></span>

<span data-ttu-id="dab1c-108">Le pilote attend le paramètre suivant.</span><span class="sxs-lookup"><span data-stu-id="dab1c-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="dab1c-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dab1c-109">Parameter</span></span>                                         | <span data-ttu-id="dab1c-110">VarType</span><span class="sxs-lookup"><span data-stu-id="dab1c-110">VarType</span></span>        | <span data-ttu-id="dab1c-111">Description</span><span class="sxs-lookup"><span data-stu-id="dab1c-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="dab1c-112">**\_ID d' \_ \_ objet des \_ propriétés \_ de l’objet de propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="dab1c-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="dab1c-113">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="dab1c-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="dab1c-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dab1c-114">Required.</span></span> <span data-ttu-id="dab1c-115">ID de l’objet qui contient les propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="dab1c-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="dab1c-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dab1c-116">Return Value</span></span>

<span data-ttu-id="dab1c-117">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="dab1c-117">The driver should return the following results.</span></span>



| <span data-ttu-id="dab1c-118">Résultats</span><span class="sxs-lookup"><span data-stu-id="dab1c-118">Result</span></span>                                                | <span data-ttu-id="dab1c-119">VarType</span><span class="sxs-lookup"><span data-stu-id="dab1c-119">VarType</span></span>         | <span data-ttu-id="dab1c-120">Description</span><span class="sxs-lookup"><span data-stu-id="dab1c-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab1c-121">**Propriétés de l’objet de propriété WPD, \_ \_ \_ clés de \_ propriété \_**</span><span class="sxs-lookup"><span data-stu-id="dab1c-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="dab1c-122">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="dab1c-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="dab1c-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dab1c-123">Required.</span></span> <span data-ttu-id="dab1c-124">Interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui spécifie toutes les propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="dab1c-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="dab1c-125">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dab1c-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="dab1c-126">**\_erreur VT**</span><span class="sxs-lookup"><span data-stu-id="dab1c-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="dab1c-127">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dab1c-127">Required.</span></span> <span data-ttu-id="dab1c-128">Valeur **HRESULT** qui indique la réussite ou l’échec global.</span><span class="sxs-lookup"><span data-stu-id="dab1c-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="dab1c-129">Les valeurs possibles des résultats incluent les [codes d’erreur des appareils mobiles Windows](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dab1c-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="dab1c-130">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** , mais il n’est pas nécessaire de retourner une autre valeur de résultat.</span><span class="sxs-lookup"><span data-stu-id="dab1c-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="dab1c-131">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="dab1c-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="dab1c-132">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="dab1c-132">**VT\_UI4**</span></span>     | <span data-ttu-id="dab1c-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="dab1c-133">Optional.</span></span> <span data-ttu-id="dab1c-134">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="dab1c-134">A driver-specific error code.</span></span> <span data-ttu-id="dab1c-135">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="dab1c-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="dab1c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dab1c-136">Requirements</span></span>



| <span data-ttu-id="dab1c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dab1c-137">Requirement</span></span> | <span data-ttu-id="dab1c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="dab1c-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab1c-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="dab1c-139">Header</span></span><br/> | <dl> <span data-ttu-id="dab1c-140"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab1c-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab1c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab1c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab1c-142">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="dab1c-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




