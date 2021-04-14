---
description: Ferme la base de données de shims initialisée à l’aide de la fonction SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523335"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="5790f-103">SdbReleaseDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="5790f-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="5790f-104">Ferme la base de données de shims initialisée à l’aide de la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="5790f-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5790f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5790f-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="5790f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5790f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5790f-107">*hSDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5790f-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5790f-108">Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="5790f-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5790f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5790f-109">Return value</span></span>

<span data-ttu-id="5790f-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5790f-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5790f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5790f-111">Requirements</span></span>



| <span data-ttu-id="5790f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5790f-112">Requirement</span></span> | <span data-ttu-id="5790f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5790f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5790f-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5790f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5790f-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5790f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5790f-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5790f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5790f-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5790f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5790f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5790f-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5790f-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5790f-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5790f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5790f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5790f-121">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="5790f-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




