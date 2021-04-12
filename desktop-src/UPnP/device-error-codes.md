---
title: Codes d’erreur de l’appareil
description: Les méthodes InvokeAction et QueryStateVariable retournent des valeurs HRESULT qui peuvent indiquer une erreur d’appareil (autrement dit, une erreur reçue d’un périphérique certifié UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463858"
---
# <a name="device-error-codes"></a><span data-ttu-id="a407e-103">Codes d’erreur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a407e-103">Device Error Codes</span></span>

<span data-ttu-id="a407e-104">Les méthodes [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) et [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) retournent des valeurs **HRESULT** qui peuvent indiquer une erreur d’appareil (autrement dit, une erreur reçue d’un périphérique certifié UPnP).</span><span class="sxs-lookup"><span data-stu-id="a407e-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="a407e-105">Si une erreur est reçue à partir d’un appareil, la méthode ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ou [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) retourne une valeur **HRESULT** basée sur le code d’erreur de l’appareil, comme expliqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a407e-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="a407e-106">Étant donné qu’une conversion est appliquée au code d’erreur de l’appareil pour produire une valeur **HRESULT** , vous ne pouvez pas lire le code d’erreur de l’appareil directement à partir de la valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a407e-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="a407e-107">Conversion d’un code d’erreur d’appareil en HRESULT</span><span class="sxs-lookup"><span data-stu-id="a407e-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="a407e-108">Il existe des codes d’erreur d’appareil standard et non standard.</span><span class="sxs-lookup"><span data-stu-id="a407e-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="a407e-109">Les codes standard ont la même signification sur tous les appareils certifiés UPnP et ont des valeurs inférieures à 600.</span><span class="sxs-lookup"><span data-stu-id="a407e-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="a407e-110">Les codes non standard sont spécifiques au fournisseur et ont des valeurs comprises entre 600 et 899.</span><span class="sxs-lookup"><span data-stu-id="a407e-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="a407e-111">Si le code d’erreur de l’appareil est standard ou non, détermine la façon dont la valeur **HRESULT** est générée :</span><span class="sxs-lookup"><span data-stu-id="a407e-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="a407e-112">Un code d’erreur d’appareil standard est mappé à une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a407e-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="a407e-113">Un code d’erreur d’appareil non standard est incorporé dans la valeur **HRESULT** en appliquant une formule.</span><span class="sxs-lookup"><span data-stu-id="a407e-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="a407e-114">Ces deux procédures peuvent être inversées pour déterminer le code d’erreur de l’appareil à partir d’une valeur **HRESULT** particulière.</span><span class="sxs-lookup"><span data-stu-id="a407e-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="a407e-115">Dérivation d’un code d’erreur d’appareil à partir d’une valeur HRESULT</span><span class="sxs-lookup"><span data-stu-id="a407e-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="a407e-116">Si la valeur **HRESULT** est supérieure ou égale à la **\_ \_ \_ \_ base spécifique d’action UPnP e** (0x80040300) et inférieure ou égale à la valeur **\_ \_ spécifique d’action \_ \_ e** (0x8004042B), le code d’erreur de l’appareil est non standard. Utilisez la formule de la section suivante pour déterminer le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a407e-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="a407e-117">Dans le cas contraire, le code d’erreur de l’appareil est standard : utilisez le tableau de la section mappage pour les codes d’erreur de l’appareil standard, qui fournit le mappage de la valeur **HRESULT** au code d’erreur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a407e-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="a407e-118">Pour obtenir une description textuelle de l’erreur après un appel à [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), définissez le paramètre *pvarRetVal* sur un tableau vide.</span><span class="sxs-lookup"><span data-stu-id="a407e-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="a407e-119">Lors du retour, ce paramètre contient une description textuelle de l’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a407e-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="a407e-120">Formule pour les codes d’erreur d’appareil non standard</span><span class="sxs-lookup"><span data-stu-id="a407e-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="a407e-121">Utilisez la formule suivante si le plug-in de **\_ \_ \_ \_ base spécifique à une action UPnP e** **≤ ≤ valeur** d'**\_ action UPnP e \_ \_ \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="a407e-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="a407e-122">Code d’erreur de l’appareil = (**HRESULT** de la  -  **\_ \_ \_ \_ base spécifique de l’action E**) + **\_ \_ \_ base spécifique** à l’action d’erreur</span><span class="sxs-lookup"><span data-stu-id="a407e-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="a407e-123">En remplaçant les valeurs numériques réelles, l’équation est : code d’erreur de l’appareil = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="a407e-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="a407e-124">Mappage pour les codes d’erreur d’appareil standard</span><span class="sxs-lookup"><span data-stu-id="a407e-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="a407e-125">Utilisez le mappage suivant si la  <  **\_ \_ \_ \_ base spécifique de l’action UPnP E** de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a407e-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="a407e-126">Valeur HRESULT</span><span class="sxs-lookup"><span data-stu-id="a407e-126">HRESULT value</span></span>                    | <span data-ttu-id="a407e-127">Code d’erreur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a407e-127">Device Error Code</span></span>                | <span data-ttu-id="a407e-128">Valeur réelle</span><span class="sxs-lookup"><span data-stu-id="a407e-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="a407e-129">\_ \_ action non valide UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="a407e-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="a407e-130">\_action non valide d’erreur \_</span><span class="sxs-lookup"><span data-stu-id="a407e-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="a407e-131">401</span><span class="sxs-lookup"><span data-stu-id="a407e-131">401</span></span>          |
| <span data-ttu-id="a407e-132">UPNP \_ E \_ arguments non valides \_</span><span class="sxs-lookup"><span data-stu-id="a407e-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="a407e-133">\_argument Fault non valide \_</span><span class="sxs-lookup"><span data-stu-id="a407e-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="a407e-134">402</span><span class="sxs-lookup"><span data-stu-id="a407e-134">402</span></span>          |
| <span data-ttu-id="a407e-135">UPNP \_ E \_ non \_ \_ synchronisé</span><span class="sxs-lookup"><span data-stu-id="a407e-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="a407e-136">Numéro de séquence d’erreur \_ non valide \_ \_</span><span class="sxs-lookup"><span data-stu-id="a407e-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="a407e-137">403</span><span class="sxs-lookup"><span data-stu-id="a407e-137">403</span></span>          |
| <span data-ttu-id="a407e-138">UPNP \_ E \_ variable non valide \_</span><span class="sxs-lookup"><span data-stu-id="a407e-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="a407e-139">VARIABLE d’erreur \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="a407e-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="a407e-140">404</span><span class="sxs-lookup"><span data-stu-id="a407e-140">404</span></span>          |
| <span data-ttu-id="a407e-141">échec de la demande d’action UPNP \_ E \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a407e-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="a407e-142">\_ \_ erreur interne du périphérique défaillant \_</span><span class="sxs-lookup"><span data-stu-id="a407e-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="a407e-143">501</span><span class="sxs-lookup"><span data-stu-id="a407e-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="a407e-144">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="a407e-144">More Information</span></span>

<span data-ttu-id="a407e-145">Les codes d’erreur de l’appareil sont spécifiés dans l' [architecture d’appareil UPnP version 1,0](https://openconnectivity.org/resources/documents.asp).</span><span class="sxs-lookup"><span data-stu-id="a407e-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="a407e-146">Les constantes mentionnées dans cette rubrique sont définies dans les fichiers UPnP. h et UPnP. idl.</span><span class="sxs-lookup"><span data-stu-id="a407e-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




