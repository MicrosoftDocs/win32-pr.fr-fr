---
description: Pour Windows 7, Windows Mobile Devices prend en charge les attributs de paramètres suivants pour les méthodes et les événements d’un service d’appareil.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Attributs de paramètres (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528361"
---
# <a name="parameter-attributes"></a><span data-ttu-id="1df07-103">Attributs de paramètre</span><span class="sxs-lookup"><span data-stu-id="1df07-103">Parameter Attributes</span></span>

<span data-ttu-id="1df07-104">Pour Windows 7, Windows Mobile Devices prend en charge les attributs de paramètres suivants pour les méthodes et les événements d’un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="1df07-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="1df07-105">Ces attributs sont retournés par les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1df07-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="1df07-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="1df07-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="1df07-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="1df07-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="1df07-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="1df07-108">Attribute</span></span>                                            | <span data-ttu-id="1df07-109">VarType</span><span class="sxs-lookup"><span data-stu-id="1df07-109">VarType</span></span>         | <span data-ttu-id="1df07-110">Description</span><span class="sxs-lookup"><span data-stu-id="1df07-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df07-111">**\_ \_ \_ valeur par défaut de l’attribut du paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="1df07-112">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="1df07-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="1df07-113">Valeur par défaut du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1df07-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="1df07-114">**\_éléments d' \_ \_ énumération d’attribut de paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="1df07-115">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="1df07-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="1df07-116">Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient les valeurs d’énumération pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="1df07-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="1df07-117">**\_formulaire d' \_ attribut de paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="1df07-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="1df07-118">**VT\_UI4**</span></span>     | <span data-ttu-id="1df07-119">Le format des valeurs de paramètre valides est autorisé.</span><span class="sxs-lookup"><span data-stu-id="1df07-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="1df07-120">**\_ \_ \_ taille maximale de l’attribut du paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="1df07-121">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="1df07-121">**VT\_UI8**</span></span>     | <span data-ttu-id="1df07-122">Taille maximale, en octets, du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1df07-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="1df07-123">**\_nom d' \_ attribut du paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="1df07-124">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="1df07-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="1df07-125">Chaîne qui spécifie le nom convivial du script d’un paramètre d’événement ou de méthode.</span><span class="sxs-lookup"><span data-stu-id="1df07-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="1df07-126">Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.</span><span class="sxs-lookup"><span data-stu-id="1df07-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="1df07-127">**\_ordre des \_ attributs du paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="1df07-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="1df07-128">**VT\_UI4**</span></span>     | <span data-ttu-id="1df07-129">Index d’ordre de paramètre de base zéro, afin qu’une valeur d’ordre de 0 corresponde au premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="1df07-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="1df07-130">**\_plage d’attribut de paramètre wpd \_ \_ \_ min.**</span><span class="sxs-lookup"><span data-stu-id="1df07-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="1df07-131">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="1df07-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="1df07-132">Valeur maximale d’un paramètre de la plage de formulaire d’attribut de paramètre WPD de formulaire \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1df07-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="1df07-133">**\_plage d’attributs du paramètre wpd \_ \_ \_ Max.**</span><span class="sxs-lookup"><span data-stu-id="1df07-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="1df07-134">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="1df07-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="1df07-135">Valeur minimale pour un paramètre de la \_ plage de formulaire d’attribut de paramètre wpd \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1df07-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="1df07-136">**\_étape de \_ plage d’attributs du paramètre wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="1df07-137">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="1df07-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="1df07-138">Valeur de pas pour un paramètre de la plage de \_ formulaire d’attribut de paramètre wpd \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1df07-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="1df07-139">**\_ \_ expression régulière d’attribut de paramètre wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="1df07-140">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="1df07-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="1df07-141">Expression régulière qui spécifie des valeurs acceptables pour les paramètres de la forme \_ \_ \_ expression régulière de formulaire d’attribut de paramètre wpd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1df07-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="1df07-142">**\_type d' \_ utilisation d’attribut de paramètre wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1df07-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="1df07-143">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="1df07-143">**VT\_UI4**</span></span>     | <span data-ttu-id="1df07-144">Entier qui spécifie l’utilisation d’un paramètre de méthode, par exemple in/out. Les valeurs valides sont du type d’énumération des [**\_ types d' \_ utilisation \_ de paramètre wpd**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="1df07-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="1df07-145">**\_attribut de paramètre wpd \_ \_ VarType**</span><span class="sxs-lookup"><span data-stu-id="1df07-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="1df07-146">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="1df07-146">**VT\_UI4**</span></span>     | <span data-ttu-id="1df07-147">Paramètre VarType.</span><span class="sxs-lookup"><span data-stu-id="1df07-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="1df07-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1df07-148">Requirements</span></span>



| <span data-ttu-id="1df07-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1df07-149">Requirement</span></span> | <span data-ttu-id="1df07-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1df07-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df07-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="1df07-151">Header</span></span><br/> | <dl> <span data-ttu-id="1df07-152"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df07-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df07-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df07-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df07-154">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="1df07-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




