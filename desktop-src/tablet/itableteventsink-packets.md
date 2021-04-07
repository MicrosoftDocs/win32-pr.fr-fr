---
description: Se produit lorsque le stylet se déplace sur le digitaliseur.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink ::P méthode ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952425"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="0a6d2-103">ITabletEventSink ::P méthode ackets</span><span class="sxs-lookup"><span data-stu-id="0a6d2-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="0a6d2-104">Se produit lorsque le stylet se déplace sur le digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a6d2-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="0a6d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a6d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6d2-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6d2-108">Identificateur de la tablette.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="0a6d2-109">*cPkts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6d2-110">Nombre de paquets.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="0a6d2-111">*cbPkts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6d2-112">Taille de la mémoire tampon des paquets</span><span class="sxs-lookup"><span data-stu-id="0a6d2-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="0a6d2-113">*pbPkts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6d2-114">Mémoire tampon de paquets.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a6d2-115">*pnSerialNumbers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6d2-116">Tableau des numéros de série.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="0a6d2-117">*confirmation*</span><span class="sxs-lookup"><span data-stu-id="0a6d2-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6d2-118">Identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6d2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a6d2-119">Return value</span></span>

<span data-ttu-id="0a6d2-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-120">This method can return one of these values.</span></span>



| <span data-ttu-id="0a6d2-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0a6d2-121">Return code</span></span>                                                                            | <span data-ttu-id="0a6d2-122">Description</span><span class="sxs-lookup"><span data-stu-id="0a6d2-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0a6d2-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a6d2-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0a6d2-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0a6d2-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0a6d2-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0a6d2-126">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="0a6d2-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a6d2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a6d2-127">Requirements</span></span>



| <span data-ttu-id="0a6d2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a6d2-128">Requirement</span></span> | <span data-ttu-id="0a6d2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a6d2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6d2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6d2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6d2-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a6d2-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0a6d2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6d2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6d2-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6d2-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0a6d2-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a6d2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a6d2-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a6d2-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a6d2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a6d2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6d2-137">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="0a6d2-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




