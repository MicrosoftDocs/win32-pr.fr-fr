---
description: Spécifie les autorisations de contrôle d’accès pour un répertoire sur une carte à puce.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Énumération CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201366"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="17a6b-103">\_ \_ Énumération des conditions d’accès au répertoire des cartes \_</span><span class="sxs-lookup"><span data-stu-id="17a6b-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="17a6b-104">L’énumération des **\_ conditions d' \_ accès \_ au répertoire** de la carte spécifie les autorisations de contrôle d’accès pour un répertoire sur une [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="17a6b-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17a6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17a6b-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="17a6b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="17a6b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="17a6b-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="17a6b-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="17a6b-108">Cette valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17a6b-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17a6b-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="17a6b-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="17a6b-110">Certains utilisateurs peuvent lire, écrire et supprimer le répertoire.</span><span class="sxs-lookup"><span data-stu-id="17a6b-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="17a6b-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="17a6b-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="17a6b-112">Les administrateurs peuvent lire, écrire et supprimer le répertoire.</span><span class="sxs-lookup"><span data-stu-id="17a6b-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17a6b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17a6b-113">Requirements</span></span>



| <span data-ttu-id="17a6b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17a6b-114">Requirement</span></span> | <span data-ttu-id="17a6b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="17a6b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17a6b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17a6b-117">Windows XP, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17a6b-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="17a6b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17a6b-119">Windows Server 2003, Windows Server 2003 \[ Desktop Apps uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17a6b-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="17a6b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="17a6b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a6b-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a6b-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a6b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17a6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a6b-123">Fournisseur de services de chiffrement de la carte à puce de base Microsoft</span><span class="sxs-lookup"><span data-stu-id="17a6b-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="17a6b-124">**CardCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="17a6b-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="17a6b-125">**CardDeleteDirectory**</span><span class="sxs-lookup"><span data-stu-id="17a6b-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
