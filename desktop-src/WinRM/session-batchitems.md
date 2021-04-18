---
title: Session.Batpropriété chItems (WSManDisp. h)
description: Définit et obtient le nombre d’éléments dans chaque lot d’énumération.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété BatchItems
- Propriété BatchItems Windows Remote Management, objet session
- Windows Remote Management d’objet de session, propriété BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512192"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="02839-106">Session.Batpropriété chItems</span><span class="sxs-lookup"><span data-stu-id="02839-106">Session.BatchItems property</span></span>

<span data-ttu-id="02839-107">Définit et obtient le nombre d’éléments dans chaque lot d’énumération.</span><span class="sxs-lookup"><span data-stu-id="02839-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="02839-108">Cette valeur ne peut pas être modifiée pendant une énumération.</span><span class="sxs-lookup"><span data-stu-id="02839-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="02839-109">Le fournisseur de ressources peut définir une limite.</span><span class="sxs-lookup"><span data-stu-id="02839-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="02839-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="02839-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="02839-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02839-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="02839-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="02839-112">Property value</span></span>

<span data-ttu-id="02839-113">Spécifie le nombre maximal d’éléments retournés pour chaque appel réseau sous-jacent au service.</span><span class="sxs-lookup"><span data-stu-id="02839-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="02839-114">Valeur par défaut : 20.</span><span class="sxs-lookup"><span data-stu-id="02839-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="02839-115">Notes</span><span class="sxs-lookup"><span data-stu-id="02839-115">Remarks</span></span>

<span data-ttu-id="02839-116">Il s’agit d’une fonctionnalité d’optimisation qui contrôle la fréquence des appels réseau entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="02839-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="02839-117">Actuellement, elle est utilisée uniquement pour les énumérations.</span><span class="sxs-lookup"><span data-stu-id="02839-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="02839-118">Pour plus d’informations sur l’énumération des ressources, consultez [**énumérer**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="02839-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02839-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02839-119">Requirements</span></span>



| <span data-ttu-id="02839-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02839-120">Requirement</span></span> | <span data-ttu-id="02839-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="02839-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02839-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02839-122">Minimum supported client</span></span><br/> | <span data-ttu-id="02839-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02839-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="02839-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02839-124">Minimum supported server</span></span><br/> | <span data-ttu-id="02839-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02839-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="02839-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="02839-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="02839-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02839-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02839-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="02839-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02839-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02839-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="02839-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02839-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="02839-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02839-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02839-132">DLL</span><span class="sxs-lookup"><span data-stu-id="02839-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02839-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02839-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02839-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02839-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02839-135">**session**</span><span class="sxs-lookup"><span data-stu-id="02839-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="02839-136">**Énumérer**</span><span class="sxs-lookup"><span data-stu-id="02839-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="02839-137">**Enumerator. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="02839-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





