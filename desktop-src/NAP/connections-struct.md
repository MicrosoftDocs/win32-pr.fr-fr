---
title: Structure des connexions (NapEnforcementClient. h)
description: Contient des informations sur la liste des connexions gérées par un enforceur.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Connexion de la structure NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942893"
---
# <a name="connections-structure"></a><span data-ttu-id="cffaa-104">Structure des connexions</span><span class="sxs-lookup"><span data-stu-id="cffaa-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="cffaa-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="cffaa-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cffaa-106">La structure des **connexions** contient des informations sur la liste des connexions gérées par un dispositif d’application.</span><span class="sxs-lookup"><span data-stu-id="cffaa-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cffaa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cffaa-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="cffaa-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cffaa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cffaa-109">**count**</span><span class="sxs-lookup"><span data-stu-id="cffaa-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="cffaa-110">Nombre de connexions actives actuellement gérées par un application dans la plage 0 (zéro) à [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cffaa-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="cffaa-111">**connexions**</span><span class="sxs-lookup"><span data-stu-id="cffaa-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="cffaa-112">Pointeur COM vers une liste d’interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) qui représentent des connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="cffaa-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cffaa-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cffaa-113">Requirements</span></span>



| <span data-ttu-id="cffaa-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cffaa-114">Requirement</span></span> | <span data-ttu-id="cffaa-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cffaa-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cffaa-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cffaa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cffaa-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cffaa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cffaa-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cffaa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cffaa-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cffaa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cffaa-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cffaa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cffaa-121"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cffaa-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cffaa-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="cffaa-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cffaa-123"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cffaa-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cffaa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cffaa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cffaa-125">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="cffaa-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="cffaa-126">Structures NAP</span><span class="sxs-lookup"><span data-stu-id="cffaa-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="cffaa-127">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="cffaa-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





