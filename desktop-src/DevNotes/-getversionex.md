---
description: Obtient des informations sur la version du système d’exploitation.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541034"
---
# <a name="_getversionex-function"></a><span data-ttu-id="2ad48-103">\_Fonction GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="2ad48-103">\_GetVersionEx function</span></span>

<span data-ttu-id="2ad48-104">\[Cette fonction est un wrapper sur la fonction **GetVersionEx** .</span><span class="sxs-lookup"><span data-stu-id="2ad48-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="2ad48-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="2ad48-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="2ad48-106">Les applications doivent appeler **GetVersionEx** directement.\]</span><span class="sxs-lookup"><span data-stu-id="2ad48-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="2ad48-107">Obtient des informations sur la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2ad48-107">Gets information about the operating system version.</span></span> <span data-ttu-id="2ad48-108">Consultez [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="2ad48-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad48-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ad48-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="2ad48-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ad48-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad48-111">*...*</span><span class="sxs-lookup"><span data-stu-id="2ad48-111">*...*</span></span> 
<span data-ttu-id="2ad48-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2ad48-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2ad48-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ad48-113">Requirements</span></span>



| <span data-ttu-id="2ad48-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ad48-114">Requirement</span></span> | <span data-ttu-id="2ad48-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ad48-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad48-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2ad48-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2ad48-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ad48-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad48-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ad48-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad48-119">**Tourne**</span><span class="sxs-lookup"><span data-stu-id="2ad48-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
