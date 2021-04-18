---
description: Les appareils mobiles Windows (WPD) prennent en charge les propriétés suivantes des paramètres de commande.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Paramètres de commande (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526773"
---
# <a name="command-parameters"></a><span data-ttu-id="85f9e-103">Paramètres de commande</span><span class="sxs-lookup"><span data-stu-id="85f9e-103">Command Parameters</span></span>

<span data-ttu-id="85f9e-104">Les appareils mobiles Windows (WPD) prennent en charge les propriétés suivantes des paramètres de commande.</span><span class="sxs-lookup"><span data-stu-id="85f9e-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="85f9e-105">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="85f9e-105">**Property**</span></span>                                            | <span data-ttu-id="85f9e-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="85f9e-106">**VarType**</span></span>     | <span data-ttu-id="85f9e-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="85f9e-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f9e-108">**\_ \_ \_ informations sur le client \_ commun de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="85f9e-109">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="85f9e-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="85f9e-110">Interface [**IPortableDeviceValues**](iportabledevicevalues.md) que le pilote utilise pour identifier le client.</span><span class="sxs-lookup"><span data-stu-id="85f9e-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="85f9e-111">**\_contexte des \_ \_ informations du client commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="85f9e-112">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="85f9e-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="85f9e-113">Contexte spécifié par le pilote qui identifie un client pour toutes les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="85f9e-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="85f9e-114">**\_catégorie de \_ \_ commande commune \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="85f9e-115">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="85f9e-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="85f9e-116">La partie **GUID** de la valeur **PROPERTYKEY** de la commande.</span><span class="sxs-lookup"><span data-stu-id="85f9e-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="85f9e-117">**\_ID de \_ \_ commande commune \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="85f9e-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="85f9e-118">**VT\_UI4**</span></span>     | <span data-ttu-id="85f9e-119">Portion d’ID unique persistante (PID) de la valeur **PROPERTYKEY** de la commande.</span><span class="sxs-lookup"><span data-stu-id="85f9e-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="85f9e-120">**\_cible de \_ la \_ commande \_ commune de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="85f9e-121">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="85f9e-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="85f9e-122">Identificateur de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="85f9e-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="85f9e-123">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="85f9e-124">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="85f9e-124">**VT\_UI4**</span></span>     | <span data-ttu-id="85f9e-125">Code d’erreur spécifique au pilote retourné par un pilote WPD.</span><span class="sxs-lookup"><span data-stu-id="85f9e-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="85f9e-126">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="85f9e-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="85f9e-127">**\_erreur VT**</span><span class="sxs-lookup"><span data-stu-id="85f9e-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="85f9e-128">Valeur **HRESULT** retournée par un pilote wpd pour une opération particulière.</span><span class="sxs-lookup"><span data-stu-id="85f9e-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="85f9e-129">**\_ID d' \_ \_ objet commun \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="85f9e-130">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="85f9e-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="85f9e-131">Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type Variant **VT \_ LPWStr** qui contient une liste d’identificateurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="85f9e-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="85f9e-132">**\_ \_ ID communs des propriétés \_ persistantes communes \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="85f9e-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="85f9e-133">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="85f9e-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="85f9e-134">Interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type Variant **VT \_ LPWStr** qui contient une liste de PID.</span><span class="sxs-lookup"><span data-stu-id="85f9e-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="85f9e-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85f9e-135">Requirements</span></span>



| <span data-ttu-id="85f9e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85f9e-136">Requirement</span></span> | <span data-ttu-id="85f9e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="85f9e-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f9e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="85f9e-138">Header</span></span><br/> | <dl> <span data-ttu-id="85f9e-139"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f9e-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f9e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85f9e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f9e-141">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="85f9e-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




