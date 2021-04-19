---
description: Contient des informations sur la clause d’accès pour le stockage protégé.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Structure PST_ACCESSCLAUSE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528781"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="b81b8-103">ACCESSCLAUSE PST ( \_ structure)</span><span class="sxs-lookup"><span data-stu-id="b81b8-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="b81b8-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b81b8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b81b8-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b81b8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b81b8-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="b81b8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b81b8-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b81b8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b81b8-108">Contient des informations sur la clause d’accès pour le stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="b81b8-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b81b8-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="b81b8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b81b8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b81b8-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="b81b8-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b81b8-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="b81b8-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b81b8-113">**ClauseType**</span><span class="sxs-lookup"><span data-stu-id="b81b8-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="b81b8-114">Type de données vers lequel pointe le membre **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="b81b8-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="b81b8-115">Pour plus d’informations, consultez [**types Pstore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="b81b8-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b81b8-116">**cbClauseData**</span><span class="sxs-lookup"><span data-stu-id="b81b8-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="b81b8-117">Taille des données vers lesquelles pointe le membre **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="b81b8-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="b81b8-118">**pbClauseData**</span><span class="sxs-lookup"><span data-stu-id="b81b8-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="b81b8-119">Pointeur vers les données de la clause d’accès.</span><span class="sxs-lookup"><span data-stu-id="b81b8-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b81b8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b81b8-120">Requirements</span></span>



| <span data-ttu-id="b81b8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b81b8-121">Requirement</span></span> | <span data-ttu-id="b81b8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b81b8-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b81b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b81b8-123">Header</span></span><br/> | <dl> <span data-ttu-id="b81b8-124"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81b8-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81b8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b81b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81b8-126">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="b81b8-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
