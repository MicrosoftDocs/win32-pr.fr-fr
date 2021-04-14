---
title: Structure RAS_PARAMETERS (rassapi. h)
description: La \_ structure des paramètres RAS est utilisée par la fonction RasAdminPortGetInfo pour retourner le nom et la valeur d’un paramètre spécifique au média associé à un port sur un serveur RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509070"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="a1f7f-104">\_Structure des paramètres RAS</span><span class="sxs-lookup"><span data-stu-id="a1f7f-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="a1f7f-105">\[La structure des **\_ paramètres RAS** n’est pas prise en charge par Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a1f7f-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="a1f7f-106">La structure des **\_ paramètres RAS** est utilisée par la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) pour retourner le nom et la valeur d’un paramètre spécifique au média associé à un port sur un serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f7f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f7f-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="a1f7f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a1f7f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1f7f-109">**\_Clé P**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="a1f7f-110">Spécifie le nom de la clé qui représente le paramètre spécifique au média, par exemple MAXCONNECTBPS.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="a1f7f-111">**\_Type P**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="a1f7f-112">Identifie le type de données associé au paramètre.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="a1f7f-113">Ce membre peut être l’une des valeurs suivantes de l’énumération de [**\_ \_ format des paramètres RAS**](ras-params-format-str.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f7f-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="a1f7f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f7f-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="a1f7f-115">Signification</span><span class="sxs-lookup"><span data-stu-id="a1f7f-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="a1f7f-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7f-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="a1f7f-117">Indique que les données associées à la clé sont un nombre.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="a1f7f-118"><dt>**ParamString**</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7f-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="a1f7f-119">Indique que les données associées à la clé sont une chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1f7f-120">**\_Attributs P**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="a1f7f-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1f7f-122">**\_Valeur P**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="a1f7f-123">Spécifie la valeur associée au paramètre.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="a1f7f-124">Ce membre est une Union de [**\_ \_ valeurs de paramètre RAS**](ras-params-value-str.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f7f-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="a1f7f-125">Si le membre de **\_ type P** est ParamNumber, le membre **Number** de l’Union contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="a1f7f-126">Si **P \_ type** est ParamString, le membre **String** de l’Union contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="a1f7f-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1f7f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1f7f-127">Requirements</span></span>



| <span data-ttu-id="a1f7f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1f7f-128">Requirement</span></span> | <span data-ttu-id="a1f7f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f7f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f7f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f7f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f7f-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1f7f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a1f7f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f7f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f7f-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1f7f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a1f7f-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a1f7f-134">End of client support</span></span><br/>    | <span data-ttu-id="a1f7f-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1f7f-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a1f7f-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a1f7f-136">End of server support</span></span><br/>    | <span data-ttu-id="a1f7f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1f7f-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a1f7f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1f7f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f7f-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7f-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f7f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f7f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f7f-141">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="a1f7f-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a1f7f-142">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="a1f7f-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="a1f7f-143">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="a1f7f-144">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="a1f7f-145">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a1f7f-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





