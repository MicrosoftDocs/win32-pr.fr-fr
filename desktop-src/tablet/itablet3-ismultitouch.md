---
description: Détermine si un périphérique d’entrée prend en charge l’interaction tactile multipoint.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3 :: IsMultiTouch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209918"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="ebc11-103">ITablet3 :: IsMultiTouch, méthode</span><span class="sxs-lookup"><span data-stu-id="ebc11-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="ebc11-104">Détermine si un périphérique d’entrée prend en charge l’interaction tactile multipoint.</span><span class="sxs-lookup"><span data-stu-id="ebc11-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebc11-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="ebc11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc11-107">*bIsMultiTouch* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ebc11-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc11-108">Indique si l’appareil est en interaction tactile.</span><span class="sxs-lookup"><span data-stu-id="ebc11-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc11-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebc11-109">Return value</span></span>

<span data-ttu-id="ebc11-110">Retourne **S \_ OK** en cas de réussite, sinon retourne un code d’erreur tel que **E \_ Fail**.</span><span class="sxs-lookup"><span data-stu-id="ebc11-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc11-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ebc11-111">Remarks</span></span>

<span data-ttu-id="ebc11-112">Après avoir déterminé à l’aide de [**IRealTimeStylus3 :: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) ou **ITablet3 :: IsMultiTouch** que l’interaction tactile est disponible, une application peut choisir d’accepter les messages d’entrée tactiles.</span><span class="sxs-lookup"><span data-stu-id="ebc11-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="ebc11-113">Des informations supplémentaires sur le filtrage des méthodes tactiles sont disponibles dans la section de propriété **IRealTimeStylus3 :: MultiTouchEnabled** .</span><span class="sxs-lookup"><span data-stu-id="ebc11-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="ebc11-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="ebc11-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="ebc11-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc11-115">Requirements</span></span>



| <span data-ttu-id="ebc11-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebc11-116">Requirement</span></span> | <span data-ttu-id="ebc11-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc11-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc11-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc11-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc11-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebc11-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc11-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc11-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ebc11-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebc11-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ebc11-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebc11-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc11-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc11-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc11-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="ebc11-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="ebc11-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="ebc11-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




