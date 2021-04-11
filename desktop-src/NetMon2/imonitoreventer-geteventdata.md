---
description: La méthode GetEventData alloue de l’espace pour les structures NMEVENTDATA et NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer :: GetEventData, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201370"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="d948d-103">IMonitorEventer :: GetEventData, méthode</span><span class="sxs-lookup"><span data-stu-id="d948d-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="d948d-104">La méthode **GetEventData** alloue de l’espace pour les structures [NMEVENTDATA](nmeventdata.md) et [NMCOLUMNINFO](nmcolumninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d948d-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="d948d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d948d-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="d948d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d948d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d948d-107">*bNumColumns* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d948d-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d948d-108">Nombre de structures **NMCOLUMNINFO** nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d948d-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="d948d-109">*ppNMEventData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d948d-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d948d-110">Adresse de la structure **NMEVENTDATA** retournée.</span><span class="sxs-lookup"><span data-stu-id="d948d-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d948d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d948d-111">Return value</span></span>

<span data-ttu-id="d948d-112">Si la méthode réussit, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d948d-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="d948d-113">Si la méthode échoue, la valeur de retour est NMERR à une \_ mémoire insuffisante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d948d-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d948d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d948d-114">Remarks</span></span>

<span data-ttu-id="d948d-115">Les analyses appellent cette méthode pour allouer de la mémoire aux structures d’informations de colonne et de données d’événement.</span><span class="sxs-lookup"><span data-stu-id="d948d-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="d948d-116">Pour libérer la mémoire allouée pour une structure **NMEVENTDATA** , consultez [IMonitorEventer :: FreeEventData](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="d948d-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d948d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d948d-117">Requirements</span></span>



| <span data-ttu-id="d948d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d948d-118">Requirement</span></span> | <span data-ttu-id="d948d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d948d-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d948d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d948d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d948d-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d948d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d948d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d948d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d948d-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d948d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d948d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d948d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d948d-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d948d-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d948d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d948d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d948d-127">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="d948d-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="d948d-128">IMonitorEventer::FreeEventData</span><span class="sxs-lookup"><span data-stu-id="d948d-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="d948d-129">NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="d948d-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="d948d-130">NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="d948d-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




