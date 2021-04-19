---
description: Champ de type dans une entrée de contrôle d’accès (ACE) qui détermine si l’ACE est une entrée du contrôle d’accès qui autorise ou refuse l’accès.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Constantes de type d’ACE d’espace de noms (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540032"
---
# <a name="namespace-ace-type-constants"></a><span data-ttu-id="56219-103">Constantes de type d’ACE d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="56219-103">Namespace ACE Type Constants</span></span>

<span data-ttu-id="56219-104">Champ de **type** dans une entrée de contrôle d’accès (ACE) qui détermine si l’ACE est une entrée du contrôle d’accès qui autorise ou refuse l’accès.</span><span class="sxs-lookup"><span data-stu-id="56219-104">The **Type** field in an access control entry (ACE) that determines whether the ACE is an ACE that allows access or denies access.</span></span>

<dl> <dt>

<span data-ttu-id="56219-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Activer**</span><span class="sxs-lookup"><span data-stu-id="56219-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56219-106">0</span><span class="sxs-lookup"><span data-stu-id="56219-106">0</span></span>
</dt> <dt>



<span data-ttu-id="56219-107">L’ACE autorise l’accès à l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="56219-107">The ACE allows access to the namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56219-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Interdire**</span><span class="sxs-lookup"><span data-stu-id="56219-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56219-109">1</span><span class="sxs-lookup"><span data-stu-id="56219-109">1</span></span>
</dt> <dt>



<span data-ttu-id="56219-110">L’ACE refuse l’accès à l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="56219-110">The ACE denies access to the namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56219-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56219-111">Requirements</span></span>



| <span data-ttu-id="56219-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56219-112">Requirement</span></span> | <span data-ttu-id="56219-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="56219-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56219-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="56219-114">Header</span></span><br/> | <dl> <span data-ttu-id="56219-115"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="56219-115"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56219-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56219-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56219-117">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="56219-117">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="56219-118">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="56219-118">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="56219-119">Établissement de l’héritage de la sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="56219-119">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="56219-120">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="56219-120">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




