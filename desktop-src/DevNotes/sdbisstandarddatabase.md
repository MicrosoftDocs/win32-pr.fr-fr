---
description: Détermine si la base de données spécifiée est l’une des bases de données standard (SysMain, AppHelp, Drvmain ou Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033577"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="55759-103">SdbIsStandardDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="55759-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="55759-104">Détermine si la base de données spécifiée est l’une des bases de données standard (SysMain, AppHelp, Drvmain ou Msimain).</span><span class="sxs-lookup"><span data-stu-id="55759-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="55759-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55759-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="55759-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55759-107">*GuidDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55759-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55759-108">GUID de la base de données.</span><span class="sxs-lookup"><span data-stu-id="55759-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55759-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55759-109">Return value</span></span>

<span data-ttu-id="55759-110">La fonction retourne **true** si le GUID représente une base de données standard ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="55759-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="55759-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55759-111">Requirements</span></span>



| <span data-ttu-id="55759-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55759-112">Requirement</span></span> | <span data-ttu-id="55759-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="55759-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55759-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55759-114">Minimum supported client</span></span><br/> | <span data-ttu-id="55759-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55759-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55759-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55759-116">Minimum supported server</span></span><br/> | <span data-ttu-id="55759-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55759-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="55759-118">DLL</span><span class="sxs-lookup"><span data-stu-id="55759-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55759-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55759-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




