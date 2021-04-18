---
description: La \_ commande wpd \_ SMS \_ Send lance l’envoi d’un message SMS (Short Message Service) par un objet fonctionnel SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Commande WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526004"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="befae-103">Commande \_ wpd \_ SMS \_ Send, commande</span><span class="sxs-lookup"><span data-stu-id="befae-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="befae-104">La **commande \_ wpd \_ SMS \_ Send** lance l’envoi d’un message SMS (Short Message Service) par un objet fonctionnel SMS.</span><span class="sxs-lookup"><span data-stu-id="befae-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="befae-105">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="befae-105">Command category</span></span>

<span data-ttu-id="befae-106">**\_SMS de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="befae-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="befae-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="befae-107">Parameters</span></span>

<span data-ttu-id="befae-108">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="befae-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="befae-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="befae-109">Parameter</span></span>                              | <span data-ttu-id="befae-110">VarType</span><span class="sxs-lookup"><span data-stu-id="befae-110">VarType</span></span>             | <span data-ttu-id="befae-111">Description</span><span class="sxs-lookup"><span data-stu-id="befae-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="befae-112">\_cible de \_ la \_ commande \_ commune de la propriété wpd</span><span class="sxs-lookup"><span data-stu-id="befae-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="befae-113">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="befae-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="befae-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="befae-114">Required.</span></span> <span data-ttu-id="befae-115">ID d’objet de l’objet fonctionnel SMS qui doit envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="befae-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="befae-116">Différents objets fonctionnels SMS peuvent avoir des paramètres différents.</span><span class="sxs-lookup"><span data-stu-id="befae-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="befae-117">\_propriété wpd \_ \_ destinataire SMS</span><span class="sxs-lookup"><span data-stu-id="befae-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="befae-118">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="befae-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="befae-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="befae-119">Required.</span></span> <span data-ttu-id="befae-120">URI du destinataire.</span><span class="sxs-lookup"><span data-stu-id="befae-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="befae-121">\_type de \_ \_ message SMS \_ de la propriété wpd</span><span class="sxs-lookup"><span data-stu-id="befae-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="befae-122">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="befae-122">VT\_UI4</span></span>             | <span data-ttu-id="befae-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="befae-123">Required.</span></span> <span data-ttu-id="befae-124">Énumérateur [**de \_ \_ types de messages SMS**](sms-message-types.md) qui indique le type de message (texte ou binaire).</span><span class="sxs-lookup"><span data-stu-id="befae-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="befae-125">\_ \_ \_ message texte SMS de la propriété wpd \_</span><span class="sxs-lookup"><span data-stu-id="befae-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="befae-126">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="befae-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="befae-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="befae-127">Optional.</span></span> <span data-ttu-id="befae-128">Si **la \_ propriété \_ wpd \_ \_ type de message SMS** indique un message texte, il s’agit de la chaîne de message ; sinon, ce paramètre n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="befae-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="befae-129">\_propriété wpd \_ \_ message binaire \_ SMS</span><span class="sxs-lookup"><span data-stu-id="befae-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="befae-130">VT \_ UI1 VT Vector \| \_</span><span class="sxs-lookup"><span data-stu-id="befae-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="befae-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="befae-131">Optional.</span></span> <span data-ttu-id="befae-132">Si **la \_ propriété \_ wpd \_ \_ type de message SMS** indique un message binaire, il s’agit d’un pointeur vers un tableau d’octets ; sinon, ce paramètre n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="befae-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="befae-133">Le premier DWORD de la valeur est la longueur du tableau, en octets.</span><span class="sxs-lookup"><span data-stu-id="befae-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="befae-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="befae-134">Return Value</span></span>

<span data-ttu-id="befae-135">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="befae-135">The driver should return the following results.</span></span>



| <span data-ttu-id="befae-136">Résultats</span><span class="sxs-lookup"><span data-stu-id="befae-136">Result</span></span>                                         | <span data-ttu-id="befae-137">VarType</span><span class="sxs-lookup"><span data-stu-id="befae-137">VarType</span></span>   | <span data-ttu-id="befae-138">Description</span><span class="sxs-lookup"><span data-stu-id="befae-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="befae-139">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="befae-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="befae-140">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="befae-140">VT\_ERROR</span></span> | <span data-ttu-id="befae-141">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="befae-141">Required.</span></span> <span data-ttu-id="befae-142">**HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="befae-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="befae-143">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="befae-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="befae-144">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="befae-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="befae-145">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="befae-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="befae-146">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="befae-146">VT\_UI4</span></span>   | <span data-ttu-id="befae-147">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="befae-147">Optional.</span></span> <span data-ttu-id="befae-148">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="befae-148">A driver-specific error code.</span></span> <span data-ttu-id="befae-149">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="befae-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="befae-150">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="befae-150">Calling Methods</span></span>

<span data-ttu-id="befae-151">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="befae-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="befae-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="befae-152">Requirements</span></span>



| <span data-ttu-id="befae-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="befae-153">Requirement</span></span> | <span data-ttu-id="befae-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="befae-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="befae-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="befae-155">Header</span></span><br/> | <dl> <span data-ttu-id="befae-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="befae-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befae-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="befae-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befae-158">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="befae-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




