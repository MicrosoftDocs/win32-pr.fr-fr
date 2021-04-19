---
description: Spécifie les autorisations de contrôle d’accès pour un fichier sur une carte à puce.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Énumération CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514603"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="9741d-103">\_ \_ Énumération des conditions d’accès au fichier de carte \_</span><span class="sxs-lookup"><span data-stu-id="9741d-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="9741d-104">L’énumération des conditions d’accès au fichier de carte spécifie les autorisations de contrôle d’accès pour un fichier sur une [*carte à puce*](../secgloss/s-gly.md). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9741d-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9741d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9741d-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="9741d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9741d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9741d-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="9741d-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="9741d-108">Cette valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9741d-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9741d-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span><span class="sxs-lookup"><span data-stu-id="9741d-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="9741d-110">Tout le monde peut lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="9741d-110">Everyone can read the file.</span></span> <span data-ttu-id="9741d-111">Des utilisateurs spécifiques peuvent écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9741d-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="9741d-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span><span class="sxs-lookup"><span data-stu-id="9741d-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="9741d-113">Seuls les utilisateurs spécifiques peuvent lire ou écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9741d-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="9741d-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span><span class="sxs-lookup"><span data-stu-id="9741d-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="9741d-115">Tout le monde peut lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="9741d-115">Everyone can read the file.</span></span> <span data-ttu-id="9741d-116">Les administrateurs peuvent écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9741d-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="9741d-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span><span class="sxs-lookup"><span data-stu-id="9741d-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="9741d-118">Les autorisations d’accès au fichier sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="9741d-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9741d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9741d-119">Requirements</span></span>



| <span data-ttu-id="9741d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9741d-120">Requirement</span></span> | <span data-ttu-id="9741d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9741d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9741d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9741d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9741d-123">Windows XP, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9741d-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9741d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9741d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9741d-125">Windows Server 2003, Windows Server 2003 \[ Desktop Apps uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9741d-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="9741d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9741d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9741d-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="9741d-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9741d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9741d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9741d-129">Fournisseur de services de chiffrement de la carte à puce de base Microsoft</span><span class="sxs-lookup"><span data-stu-id="9741d-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="9741d-130">**\_informations sur le fichier de carte \_**</span><span class="sxs-lookup"><span data-stu-id="9741d-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="9741d-131">**CardCreateFile**</span><span class="sxs-lookup"><span data-stu-id="9741d-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
