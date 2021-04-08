---
title: Types de données du journal des événements Windows (WinEvt. h)
description: 'Le journal des événements Windows définit les types de données suivants :'
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741388"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="e7fe0-106">Types de données du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="e7fe0-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="e7fe0-107">Le journal des événements Windows définit les types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="e7fe0-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="e7fe0-108">**\_Gestionnaire evt**</span><span class="sxs-lookup"><span data-stu-id="e7fe0-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="e7fe0-109">Handle d’un objet du journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="e7fe0-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="e7fe0-110">**\_handle PEVT**</span><span class="sxs-lookup"><span data-stu-id="e7fe0-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="e7fe0-111">Pointeur vers le handle d’un objet du journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="e7fe0-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="e7fe0-112">**\_handle de \_ propriété du tableau d’objets evt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7fe0-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="e7fe0-113">Handle d’un tableau d’objets du journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="e7fe0-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7fe0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7fe0-114">Requirements</span></span>



| <span data-ttu-id="e7fe0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7fe0-115">Requirement</span></span> | <span data-ttu-id="e7fe0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7fe0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fe0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7fe0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fe0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7fe0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e7fe0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7fe0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fe0-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7fe0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e7fe0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7fe0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7fe0-122"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7fe0-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





