---
description: Sélectionne une carte réseau de registre.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: GetNPPBlobFromUI, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952271"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="d8835-103">GetNPPBlobFromUI fonction)</span><span class="sxs-lookup"><span data-stu-id="d8835-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="d8835-104">La fonction **GetNPPBlobFromUI** sélectionne une carte réseau de registre.</span><span class="sxs-lookup"><span data-stu-id="d8835-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8835-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8835-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d8835-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8835-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8835-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8835-108">Handle d’une fenêtre qui affiche la boîte de dialogue **Sélectionner un réseau** .</span><span class="sxs-lookup"><span data-stu-id="d8835-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d8835-109">*hFilterBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8835-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8835-110">Handle d’un [*objet blob de filtre*](f.md) utilisé pour limiter les cartes réseau affichées.</span><span class="sxs-lookup"><span data-stu-id="d8835-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d8835-111">*phBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8835-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8835-112">Pointeur vers le handle de l’objet BLOB qui représente la carte réseau sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d8835-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8835-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8835-113">Return value</span></span>

<span data-ttu-id="d8835-114">Si la fonction réussit (l’utilisateur sélectionne une carte réseau), la valeur de retour est NMERR \_ Success et l’objet BLOB vers lequel pointe *phBlob* est renseigné.</span><span class="sxs-lookup"><span data-stu-id="d8835-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="d8835-115">Si l’utilisateur ne sélectionne pas une carte réseau, la valeur de retour est **NMERR \_ aucun \_ NPP \_** n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d8835-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="d8835-116">Si la fonction échoue, la valeur de retour est une autre valeur NMERR.</span><span class="sxs-lookup"><span data-stu-id="d8835-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8835-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d8835-117">Remarks</span></span>

<span data-ttu-id="d8835-118">Quand elle est appelée, Moniteur réseau affiche la boîte de dialogue **Sélectionner un réseau** , que vous pouvez utiliser pour sélectionner une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="d8835-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="d8835-119">L’objet BLOB NPP qui représente la carte réseau est renvoyé à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="d8835-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="d8835-120">Si l’objet BLOB nommé par *hFilterBlob* est un [*objet BLOB spécial*](s.md), le Finder tente de le traiter.</span><span class="sxs-lookup"><span data-stu-id="d8835-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="d8835-121">Par exemple, un appel qui avait précédemment retourné un objet BLOB spécial à partir du NPP distant.</span><span class="sxs-lookup"><span data-stu-id="d8835-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="d8835-122">L’application a inséré la balise requise, le nom de l’ordinateur \_ .</span><span class="sxs-lookup"><span data-stu-id="d8835-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="d8835-123">Dans ce cas, le Finder transmet cet objet BLOB au NPP distant, qui retourne ensuite une table d’objets BLOB NPP représentant l’ordinateur demandé.</span><span class="sxs-lookup"><span data-stu-id="d8835-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="d8835-124">Ces objets BLOB NPP distants s’affichent dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d8835-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="d8835-125">L’appelant doit appeler la fonction [DestroyBlob](destroyblob.md) , qui détruit l’objet BLOB retourné lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d8835-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="d8835-126">Pour plus d’informations sur l’un des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="d8835-126">For more information about</span></span> | <span data-ttu-id="d8835-127">Consultez</span><span class="sxs-lookup"><span data-stu-id="d8835-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d8835-128">Trois façons de sélectionner des cartes réseau</span><span class="sxs-lookup"><span data-stu-id="d8835-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="d8835-129">Sélection d’une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="d8835-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="d8835-130">Spécification d’un objet BLOB de filtre</span><span class="sxs-lookup"><span data-stu-id="d8835-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="d8835-131">Spécification d’un objet BLOB de filtre</span><span class="sxs-lookup"><span data-stu-id="d8835-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="d8835-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8835-132">Requirements</span></span>



| <span data-ttu-id="d8835-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8835-133">Requirement</span></span> | <span data-ttu-id="d8835-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8835-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8835-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8835-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d8835-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8835-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d8835-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8835-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d8835-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8835-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8835-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8835-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8835-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8835-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d8835-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8835-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8835-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8835-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8835-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d8835-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8835-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8835-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8835-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8835-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8835-146">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="d8835-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="d8835-147">SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="d8835-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




