---
description: Identifie l’ensemble de règles d’accès pour les données de stockage protégées.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Structure PST_ACCESSRULESET (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533412"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="4fc07-103">ACCESSRULESET PST ( \_ structure)</span><span class="sxs-lookup"><span data-stu-id="4fc07-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="4fc07-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4fc07-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4fc07-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4fc07-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4fc07-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="4fc07-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4fc07-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4fc07-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4fc07-108">Identifie l’ensemble de règles d’accès pour les données de stockage protégées.</span><span class="sxs-lookup"><span data-stu-id="4fc07-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc07-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc07-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="4fc07-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4fc07-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="4fc07-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="4fc07-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="4fc07-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="4fc07-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fc07-113">**cRules**</span><span class="sxs-lookup"><span data-stu-id="4fc07-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="4fc07-114">Nombre de règles dans le tableau **rgRules** .</span><span class="sxs-lookup"><span data-stu-id="4fc07-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="4fc07-115">**rgRules**</span><span class="sxs-lookup"><span data-stu-id="4fc07-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="4fc07-116">Pointeur vers un tableau de structures [**\_ ACCESSRULE PST**](pst-accessrule.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc07-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc07-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fc07-117">Requirements</span></span>



| <span data-ttu-id="4fc07-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fc07-118">Requirement</span></span> | <span data-ttu-id="4fc07-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc07-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc07-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fc07-120">Header</span></span><br/> | <dl> <span data-ttu-id="4fc07-121"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc07-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc07-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc07-123">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="4fc07-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="4fc07-124">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="4fc07-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
