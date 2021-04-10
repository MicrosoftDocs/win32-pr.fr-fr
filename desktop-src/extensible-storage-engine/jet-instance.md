---
description: 'En savoir plus sur : JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952547"
---
# <a name="jet_instance"></a><span data-ttu-id="b0942-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b0942-103">JET_INSTANCE</span></span>


<span data-ttu-id="b0942-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b0942-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="b0942-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b0942-105">JET_INSTANCE</span></span>

<span data-ttu-id="b0942-106">Le type de données **JET_INSTANCE** contient un descripteur de l’instance de la base de données à utiliser pour un appel à l’API jet.</span><span class="sxs-lookup"><span data-stu-id="b0942-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="b0942-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="b0942-107">Data Types</span></span>

<span data-ttu-id="b0942-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b0942-108">JET_INSTANCE</span></span>

<span data-ttu-id="b0942-109">La **valeur null** ou [JET_instanceNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle d’instance non valide.</span><span class="sxs-lookup"><span data-stu-id="b0942-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="b0942-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b0942-110">Remarks</span></span>

<span data-ttu-id="b0942-111">Ce descripteur est obtenu lorsque vous créez une instance de la base de données en appelant les fonctions [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b0942-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="b0942-112">**Windows XP :**  L’utilisation explicite des instances est prise en charge uniquement sur Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b0942-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="b0942-113">**Windows 2000 :**  Une seule instance globale est prise en charge par processus.</span><span class="sxs-lookup"><span data-stu-id="b0942-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="b0942-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0942-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0942-115"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b0942-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b0942-116">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b0942-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0942-117"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b0942-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b0942-118">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b0942-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0942-119"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b0942-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b0942-120">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b0942-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b0942-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0942-121">See Also</span></span>

[<span data-ttu-id="b0942-122">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b0942-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b0942-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="b0942-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="b0942-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="b0942-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="b0942-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="b0942-125">JetInit2</span></span>](./jetinit2-function.md)
