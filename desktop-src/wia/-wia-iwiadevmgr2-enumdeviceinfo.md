---
description: Crée un énumérateur d’informations de propriété pour chaque périphérique WIA (Windows Image Acquisition) 2,0 disponible.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2 :: EnumDeviceInfo, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752837"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="880cb-103">IWiaDevMgr2 :: EnumDeviceInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="880cb-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="880cb-104">Crée un énumérateur d’informations de propriété pour chaque périphérique WIA (Windows Image Acquisition) 2,0 disponible.</span><span class="sxs-lookup"><span data-stu-id="880cb-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="880cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="880cb-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="880cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="880cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880cb-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="880cb-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880cb-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="880cb-108">Type: **LONG**</span></span>

<span data-ttu-id="880cb-109">Spécifie le type d’appareils WIA 2,0 à énumérer.</span><span class="sxs-lookup"><span data-stu-id="880cb-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="880cb-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DevInfo \_ enum \_ local**</span><span class="sxs-lookup"><span data-stu-id="880cb-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="880cb-111">Seuls les appareils de scanneur actifs connectés localement sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="880cb-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="880cb-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DevInfo \_ enum \_ All**</span><span class="sxs-lookup"><span data-stu-id="880cb-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="880cb-113">Tous les appareils sont énumérés, à la fois localement et à distance, y compris les appareils inactifs (déconnectés) et les appareils traditionnels de ICT uniquement.</span><span class="sxs-lookup"><span data-stu-id="880cb-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="880cb-114">*ppIEnum* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="880cb-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="880cb-115">Type : **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="880cb-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="880cb-116">Reçoit l’adresse d’un pointeur vers l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="880cb-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880cb-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="880cb-117">Return value</span></span>

<span data-ttu-id="880cb-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="880cb-118">Type: **HRESULT**</span></span>

<span data-ttu-id="880cb-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="880cb-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="880cb-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="880cb-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="880cb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="880cb-121">Remarks</span></span>

<span data-ttu-id="880cb-122">La méthode **IWiaDevMgr2 :: EnumDeviceInfo** crée un objet énumérateur qui prend en charge l’interface d' [**\_ \_ informations de développement IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="880cb-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="880cb-123">La méthode stocke un pointeur vers l’interface **IEnumWIA \_ dev \_ info** dans le paramètre *ppIEnum*.</span><span class="sxs-lookup"><span data-stu-id="880cb-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="880cb-124">Les applications peuvent utiliser le pointeur d’interface **IEnumWIA \_ dev \_ info** pour énumérer les propriétés de chaque appareil WIA 2,0 attaché à l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="880cb-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="880cb-125">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="880cb-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="880cb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880cb-126">Requirements</span></span>



| <span data-ttu-id="880cb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="880cb-127">Requirement</span></span> | <span data-ttu-id="880cb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="880cb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="880cb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="880cb-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="880cb-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="880cb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="880cb-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="880cb-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="880cb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="880cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="880cb-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="880cb-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="880cb-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="880cb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="880cb-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="880cb-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
