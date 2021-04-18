---
description: Décrit une règle d’accès aux éléments stockés dans le stockage protégé.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Structure PST_ACCESSRULE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528950"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="62822-103">ACCESSRULE PST ( \_ structure)</span><span class="sxs-lookup"><span data-stu-id="62822-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="62822-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="62822-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="62822-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="62822-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="62822-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="62822-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="62822-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="62822-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="62822-108">Décrit une règle d’accès aux éléments stockés dans le stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="62822-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="62822-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62822-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="62822-110">Membres</span><span class="sxs-lookup"><span data-stu-id="62822-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="62822-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="62822-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="62822-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="62822-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="62822-113">**AccessModeFlags**</span><span class="sxs-lookup"><span data-stu-id="62822-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="62822-114">Modes d’accès auxquels un ensemble spécifié de clauses d’accès appartient.</span><span class="sxs-lookup"><span data-stu-id="62822-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="62822-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="62822-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="62822-116">Signification</span><span class="sxs-lookup"><span data-stu-id="62822-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="62822-117"><dt>**Fichier PST \_ LIRE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="62822-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="62822-118">Mode d’accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="62822-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="62822-119"><dt>**Fichier PST \_ ÉCRIRE**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="62822-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="62822-120">Mode d’accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="62822-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62822-121">**cClauses**</span><span class="sxs-lookup"><span data-stu-id="62822-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="62822-122">Nombre de structures dans le tableau **rgClauses** .</span><span class="sxs-lookup"><span data-stu-id="62822-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="62822-123">**rgClauses**</span><span class="sxs-lookup"><span data-stu-id="62822-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="62822-124">Pointeur vers un tableau de structures [**\_ ACCESSCLAUSE PST**](pst-accessclause.md) .</span><span class="sxs-lookup"><span data-stu-id="62822-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62822-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62822-125">Requirements</span></span>



| <span data-ttu-id="62822-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62822-126">Requirement</span></span> | <span data-ttu-id="62822-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="62822-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="62822-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="62822-128">Header</span></span><br/> | <dl> <span data-ttu-id="62822-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="62822-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62822-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62822-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62822-131">**\_ACCESSCLAUSE PST**</span><span class="sxs-lookup"><span data-stu-id="62822-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="62822-132">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="62822-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
