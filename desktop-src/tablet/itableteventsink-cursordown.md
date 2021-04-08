---
description: Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'ITabletEventSink :: CursorDown, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757054"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="09178-103">ITabletEventSink :: CursorDown, méthode</span><span class="sxs-lookup"><span data-stu-id="09178-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="09178-104">Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.</span><span class="sxs-lookup"><span data-stu-id="09178-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="09178-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09178-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="09178-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09178-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09178-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09178-108">Identificateur de la tablette.</span><span class="sxs-lookup"><span data-stu-id="09178-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="09178-109">*CID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09178-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09178-110">Identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="09178-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="09178-111">*nSerialNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09178-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09178-112">Numéro de série du stylet.</span><span class="sxs-lookup"><span data-stu-id="09178-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="09178-113">*cbPkt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09178-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09178-114">Nombre d’octets dans un paquet de données de stylet.</span><span class="sxs-lookup"><span data-stu-id="09178-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="09178-115">*pbPkt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09178-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09178-116">Données du stylet indiquant l’emplacement où le stylet touche la tablette.</span><span class="sxs-lookup"><span data-stu-id="09178-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09178-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09178-117">Return value</span></span>

<span data-ttu-id="09178-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="09178-118">This method can return one of these values.</span></span>



| <span data-ttu-id="09178-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="09178-119">Return code</span></span>                                                                            | <span data-ttu-id="09178-120">Description</span><span class="sxs-lookup"><span data-stu-id="09178-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="09178-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09178-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="09178-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="09178-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="09178-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="09178-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="09178-124">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="09178-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="09178-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09178-125">Requirements</span></span>



| <span data-ttu-id="09178-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09178-126">Requirement</span></span> | <span data-ttu-id="09178-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="09178-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09178-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09178-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09178-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09178-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09178-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09178-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09178-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="09178-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="09178-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09178-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="09178-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09178-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09178-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09178-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09178-135">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="09178-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




