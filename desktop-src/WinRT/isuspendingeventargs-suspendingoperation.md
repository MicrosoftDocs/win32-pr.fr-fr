---
description: Obtient l’opération d’interruption de l’application.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'ISuspendingEventArgs :: SuspendingOperation, propriété (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862613"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="20bda-103">ISuspendingEventArgs :: SuspendingOperation, propriété</span><span class="sxs-lookup"><span data-stu-id="20bda-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="20bda-104">Obtient l’opération d’interruption de l’application.</span><span class="sxs-lookup"><span data-stu-id="20bda-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="20bda-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="20bda-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bda-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20bda-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="20bda-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="20bda-107">Property value</span></span>

<span data-ttu-id="20bda-108">Opération de suspension.</span><span class="sxs-lookup"><span data-stu-id="20bda-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bda-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20bda-109">Requirements</span></span>



| <span data-ttu-id="20bda-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20bda-110">Requirement</span></span> | <span data-ttu-id="20bda-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="20bda-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bda-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20bda-112">Minimum supported client</span></span><br/> | <span data-ttu-id="20bda-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="20bda-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="20bda-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20bda-114">Minimum supported server</span></span><br/> | <span data-ttu-id="20bda-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20bda-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="20bda-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="20bda-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="20bda-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="20bda-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="20bda-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="20bda-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20bda-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20bda-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bda-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20bda-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bda-121">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="20bda-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




