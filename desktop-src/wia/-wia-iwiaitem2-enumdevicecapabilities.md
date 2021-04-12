---
description: Crée un énumérateur qui est utilisé pour déterminer les commandes et les événements pris en charge par un appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2 :: EnumDeviceCapabilities, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526469"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="4c34b-103">IWiaItem2 :: EnumDeviceCapabilities, méthode</span><span class="sxs-lookup"><span data-stu-id="4c34b-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="4c34b-104">Crée un énumérateur qui est utilisé pour déterminer les commandes et les événements pris en charge par un appareil WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c34b-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c34b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c34b-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="4c34b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c34b-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c34b-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c34b-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="4c34b-108">Type: **LONG**</span></span>

<span data-ttu-id="4c34b-109">Spécifie un indicateur qui sélectionne le type de fonctionnalités à énumérer.</span><span class="sxs-lookup"><span data-stu-id="4c34b-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="4c34b-110">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c34b-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="4c34b-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**commandes de l' \_ appareil WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c34b-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="4c34b-112">Énumérer les commandes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4c34b-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="4c34b-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_événements d’appareil WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c34b-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="4c34b-114">Énumérer les événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4c34b-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4c34b-115">*ppIEnumWIA \_ \_Majuscules de développement* \[\]</span><span class="sxs-lookup"><span data-stu-id="4c34b-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c34b-116">Type : **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c34b-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="4c34b-117">Reçoit un pointeur vers l’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) créée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4c34b-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c34b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c34b-118">Return value</span></span>

<span data-ttu-id="4c34b-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4c34b-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4c34b-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c34b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c34b-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c34b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c34b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4c34b-122">Remarks</span></span>

<span data-ttu-id="4c34b-123">Cette méthode est utilisée pour créer un objet énumérateur pour obtenir le jeu de commandes et d’événements pris en charge par un appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c34b-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="4c34b-124">Le paramètre *lFlags* est utilisé pour spécifier les genres de fonctionnalités d’appareil à énumérer.</span><span class="sxs-lookup"><span data-stu-id="4c34b-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="4c34b-125">La méthode **IWiaItem2 :: EnumDeviceCapabilities** stocke l’adresse de l’interface de l’objet énumérateur dans le paramètre *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="4c34b-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="4c34b-126">Cette méthode peut uniquement être appelée sur l’élément racine des objets [**IWiaItem2**](-wia-iwiaitem2.md) d’un arbre d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4c34b-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="4c34b-127">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="4c34b-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c34b-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c34b-128">Requirements</span></span>



| <span data-ttu-id="4c34b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c34b-129">Requirement</span></span> | <span data-ttu-id="4c34b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c34b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c34b-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c34b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c34b-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c34b-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c34b-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c34b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c34b-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c34b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c34b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c34b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c34b-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c34b-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c34b-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="4c34b-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c34b-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c34b-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
