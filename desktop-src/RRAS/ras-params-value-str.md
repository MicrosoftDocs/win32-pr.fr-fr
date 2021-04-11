---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: La \_ \_ valeur Union des paramètres RAS est utilisée dans la \_ structure de paramètres RAS pour stocker les données associées à un paramètre spécifique au média.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS RAS_PARAMS_VALUE Union
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102832"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="d90e0-104">Union des valeurs des \_ paramètres RAS \_</span><span class="sxs-lookup"><span data-stu-id="d90e0-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="d90e0-105">\[L’Union des **\_ \_ valeurs des paramètres RAS** n’est pas prise en charge par Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="d90e0-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="d90e0-106">La **\_ \_ valeur** Union des paramètres RAS est utilisée dans la structure de [**\_ paramètres RAS**](ras-parameters-str.md) pour stocker les données associées à un paramètre spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="d90e0-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="d90e0-107">Le membre de **\_ type P** de la structure de **\_ paramètres RAS** utilise une valeur de l’énumération de [**\_ \_ format params**](ras-params-format-str.md) des paramètres d’accès distant pour indiquer le type de valeur actuellement stocké dans la **\_ \_ valeur** des paramètres RAS.</span><span class="sxs-lookup"><span data-stu-id="d90e0-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90e0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d90e0-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="d90e0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d90e0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d90e0-110">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d90e0-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="d90e0-111">Si le membre de **\_ type P** de la structure de [**\_ paramètres ras**](ras-parameters-str.md) est ParamNumber, le membre **Number** contient la valeur du paramètre spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="d90e0-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="d90e0-112">Par exemple, le paramètre MAXCONNECTBPS est de type ParamNumber, et la valeur peut être 19200.</span><span class="sxs-lookup"><span data-stu-id="d90e0-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="d90e0-113">Si le membre de **\_ type P** de la structure de [**\_ paramètres ras**](ras-parameters-str.md) est ParamNumber, le membre **Number** contient la valeur du paramètre spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="d90e0-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="d90e0-114">Par exemple, le paramètre MAXCONNECTBPS est de type ParamNumber, et la valeur peut être 19200.</span><span class="sxs-lookup"><span data-stu-id="d90e0-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="d90e0-115">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d90e0-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="d90e0-116">Si le membre de **\_ type P** de la structure de [**\_ paramètres RAS**](ras-parameters-str.md) est ParamString, le membre de **chaîne** contient la valeur du paramètre spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="d90e0-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="d90e0-117">**Durée**</span><span class="sxs-lookup"><span data-stu-id="d90e0-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="d90e0-118">Spécifie la longueur, en caractères, de la chaîne vers laquelle pointe le membre de **données** .</span><span class="sxs-lookup"><span data-stu-id="d90e0-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="d90e0-119">**Données**</span><span class="sxs-lookup"><span data-stu-id="d90e0-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="d90e0-120">Pointeur vers une mémoire tampon qui contient la valeur de chaîne d’un paramètre spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="d90e0-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d90e0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d90e0-121">Requirements</span></span>



| <span data-ttu-id="d90e0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d90e0-122">Requirement</span></span> | <span data-ttu-id="d90e0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d90e0-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d90e0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d90e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d90e0-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d90e0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d90e0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d90e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d90e0-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d90e0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d90e0-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d90e0-128">End of client support</span></span><br/>    | <span data-ttu-id="d90e0-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d90e0-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d90e0-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d90e0-130">End of server support</span></span><br/>    | <span data-ttu-id="d90e0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d90e0-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d90e0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d90e0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d90e0-133"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d90e0-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d90e0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d90e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90e0-135">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="d90e0-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d90e0-136">Union d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="d90e0-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="d90e0-137">**\_paramètres RAS**</span><span class="sxs-lookup"><span data-stu-id="d90e0-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="d90e0-138">**\_format des paramètres \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="d90e0-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





