---
description: Types de données pour les méthodes de stockage protégées.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Types PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541121"
---
# <a name="pstore-types"></a><span data-ttu-id="b99e2-103">Types PStore</span><span class="sxs-lookup"><span data-stu-id="b99e2-103">PStore Types</span></span>

<span data-ttu-id="b99e2-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b99e2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b99e2-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b99e2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b99e2-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="b99e2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b99e2-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b99e2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b99e2-108">Types de données pour les méthodes de stockage protégées.</span><span class="sxs-lookup"><span data-stu-id="b99e2-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="b99e2-109">**\_ACCESSMODE PST**</span><span class="sxs-lookup"><span data-stu-id="b99e2-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="b99e2-110">Définit le mode de lecture ou d’écriture de la règle d’accès.</span><span class="sxs-lookup"><span data-stu-id="b99e2-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="b99e2-111">**\_ACCESSCLAUSETYPE PST**</span><span class="sxs-lookup"><span data-stu-id="b99e2-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="b99e2-112">Définit le type de clause de la règle d’accès.</span><span class="sxs-lookup"><span data-stu-id="b99e2-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="b99e2-113">**\_clé PST**</span><span class="sxs-lookup"><span data-stu-id="b99e2-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="b99e2-114">Définit la clé pour l’élément stocké.</span><span class="sxs-lookup"><span data-stu-id="b99e2-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b99e2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b99e2-115">Requirements</span></span>



| <span data-ttu-id="b99e2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b99e2-116">Requirement</span></span> | <span data-ttu-id="b99e2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b99e2-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b99e2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b99e2-118">Header</span></span><br/> | <dl> <span data-ttu-id="b99e2-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b99e2-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
