---
description: 'La méthode IWiaItem2 :: EnumRegisterEventInfo crée un énumérateur que vous pouvez utiliser pour obtenir des informations sur les événements pour lesquels une application est inscrite.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2 :: EnumRegisterEventInfo, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113311"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="6fdf8-103">IWiaItem2 :: EnumRegisterEventInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6fdf8-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="6fdf8-104">La méthode **IWiaItem2 :: EnumRegisterEventInfo** crée un énumérateur que vous pouvez utiliser pour obtenir des informations sur les événements pour lesquels une application est inscrite.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdf8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fdf8-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="6fdf8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fdf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fdf8-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fdf8-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdf8-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="6fdf8-108">Type: **LONG**</span></span>

<span data-ttu-id="6fdf8-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-109">Not used.</span></span> <span data-ttu-id="6fdf8-110">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6fdf8-111">*pEventGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fdf8-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdf8-112">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="6fdf8-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="6fdf8-113">Pointeur vers un identificateur qui spécifie l’événement matériel pour lequel vous souhaitez obtenir des informations d’inscription.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="6fdf8-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6fdf8-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdf8-115">Type : **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="6fdf8-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="6fdf8-116">Adresse d’un pointeur vers l’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="6fdf8-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fdf8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fdf8-117">Return value</span></span>

<span data-ttu-id="6fdf8-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6fdf8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="6fdf8-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fdf8-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fdf8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fdf8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6fdf8-121">Remarks</span></span>

<span data-ttu-id="6fdf8-122">Une application appelle cette méthode pour créer un objet énumérateur pour les informations d’événement.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="6fdf8-123">**IWiaItem2 :: EnumRegisterEventInfo** stocke l’adresse de l’interface de [**\_ développement \_ IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) de l’objet énumérateur dans le paramètre *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="6fdf8-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="6fdf8-124">Le programme utilise ensuite le pointeur d’interface pour énumérer les propriétés de l’événement pour lequel il est enregistré.</span><span class="sxs-lookup"><span data-stu-id="6fdf8-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="6fdf8-125">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="6fdf8-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdf8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fdf8-126">Requirements</span></span>



| <span data-ttu-id="6fdf8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fdf8-127">Requirement</span></span> | <span data-ttu-id="6fdf8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fdf8-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6fdf8-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fdf8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdf8-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fdf8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fdf8-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fdf8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdf8-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fdf8-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6fdf8-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fdf8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fdf8-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdf8-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
