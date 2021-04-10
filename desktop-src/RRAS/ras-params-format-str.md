---
title: Énumération RAS_PARAMS_FORMAT (rassapi. h)
description: Le \_ \_ type d’énumération de format params RAS est utilisé dans la \_ structure de paramètres RAS pour indiquer le type de données associé à une clé spécifique au média.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT d’énumération RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104392"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="a69c2-104">\_Énumération de format des paramètres RAS \_</span><span class="sxs-lookup"><span data-stu-id="a69c2-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="a69c2-105">\[L’énumération de **\_ \_ format des paramètres RAS** n’est pas prise en charge par Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a69c2-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="a69c2-106">Le type d’énumération de **\_ \_ format params RAS** est utilisé dans la structure de [**\_ paramètres RAS**](ras-parameters-str.md) pour indiquer le type de données associé à une clé spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="a69c2-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a69c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a69c2-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="a69c2-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a69c2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a69c2-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span><span class="sxs-lookup"><span data-stu-id="a69c2-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a69c2-110">Indique que les données associées à la clé sont un nombre.</span><span class="sxs-lookup"><span data-stu-id="a69c2-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="a69c2-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span><span class="sxs-lookup"><span data-stu-id="a69c2-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="a69c2-112">Indique que les données associées à la clé sont une chaîne.</span><span class="sxs-lookup"><span data-stu-id="a69c2-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a69c2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a69c2-113">Requirements</span></span>



| <span data-ttu-id="a69c2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a69c2-114">Requirement</span></span> | <span data-ttu-id="a69c2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a69c2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a69c2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a69c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a69c2-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a69c2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a69c2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a69c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a69c2-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a69c2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a69c2-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a69c2-120">End of client support</span></span><br/>    | <span data-ttu-id="a69c2-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a69c2-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a69c2-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a69c2-122">End of server support</span></span><br/>    | <span data-ttu-id="a69c2-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a69c2-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a69c2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a69c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a69c2-125"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a69c2-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a69c2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a69c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a69c2-127">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="a69c2-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a69c2-128">Énumérations de l’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="a69c2-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a69c2-129">**\_paramètres RAS**</span><span class="sxs-lookup"><span data-stu-id="a69c2-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





