---
description: Obtient le temps restant avant qu’une opération d’interruption de l’application retardée se poursuive.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation ::D propriété échéanc (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951183"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="ecd57-103">ISuspendingOperation ::D propriété échéanc</span><span class="sxs-lookup"><span data-stu-id="ecd57-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="ecd57-104">Obtient le temps restant avant qu’une opération d’interruption de l’application retardée se poursuive.</span><span class="sxs-lookup"><span data-stu-id="ecd57-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="ecd57-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ecd57-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd57-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecd57-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="ecd57-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ecd57-107">Property value</span></span>

<span data-ttu-id="ecd57-108">Temps restant avant la poursuite de l’opération de suspension d’application retardée.</span><span class="sxs-lookup"><span data-stu-id="ecd57-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd57-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecd57-109">Requirements</span></span>



| <span data-ttu-id="ecd57-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecd57-110">Requirement</span></span> | <span data-ttu-id="ecd57-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecd57-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd57-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd57-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd57-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecd57-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ecd57-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd57-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd57-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecd57-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ecd57-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecd57-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd57-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd57-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecd57-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="ecd57-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecd57-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecd57-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd57-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd57-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd57-121">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="ecd57-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




