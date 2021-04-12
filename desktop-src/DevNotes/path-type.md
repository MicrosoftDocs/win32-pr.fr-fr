---
description: Représente le type de chemin d’accès utilisé comme argument.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Énumération PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522951"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="004bd-103">\_Énumération de type de chemin</span><span class="sxs-lookup"><span data-stu-id="004bd-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="004bd-104">Représente le type de chemin d’accès utilisé comme argument.</span><span class="sxs-lookup"><span data-stu-id="004bd-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="004bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="004bd-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="004bd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="004bd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="004bd-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**\_chemin dos**</span><span class="sxs-lookup"><span data-stu-id="004bd-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="004bd-108">Chemin standard.</span><span class="sxs-lookup"><span data-stu-id="004bd-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="004bd-109"><span id="NT_PATH"></span><span id="nt_path"></span>**\_chemin d’accès NT**</span><span class="sxs-lookup"><span data-stu-id="004bd-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="004bd-110">Chemin d’accès interne.</span><span class="sxs-lookup"><span data-stu-id="004bd-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="004bd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="004bd-111">Requirements</span></span>



| <span data-ttu-id="004bd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="004bd-112">Requirement</span></span> | <span data-ttu-id="004bd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="004bd-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="004bd-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004bd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="004bd-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004bd-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="004bd-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004bd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="004bd-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="004bd-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="004bd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="004bd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004bd-119">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="004bd-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="004bd-120">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="004bd-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




