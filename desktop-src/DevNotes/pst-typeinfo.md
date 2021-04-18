---
description: Décrit un type ou un sous-type.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Structure PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533188"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="7d6e8-103">PST, \_ structure</span><span class="sxs-lookup"><span data-stu-id="7d6e8-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="7d6e8-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7d6e8-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7d6e8-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7d6e8-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="7d6e8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7d6e8-108">Décrit un type ou un sous-type.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6e8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d6e8-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="7d6e8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7d6e8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d6e8-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7d6e8-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="7d6e8-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="7d6e8-114">Pointeur vers une chaîne de caractères larges qui représente le nom complet du type.</span><span class="sxs-lookup"><span data-stu-id="7d6e8-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d6e8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d6e8-115">Requirements</span></span>



| <span data-ttu-id="7d6e8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d6e8-116">Requirement</span></span> | <span data-ttu-id="7d6e8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d6e8-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6e8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d6e8-118">Header</span></span><br/> | <dl> <span data-ttu-id="7d6e8-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6e8-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6e8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d6e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6e8-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="7d6e8-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="7d6e8-123">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="7d6e8-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="7d6e8-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
