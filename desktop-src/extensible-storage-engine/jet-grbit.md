---
description: 'En savoir plus sur : JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106535846"
---
# <a name="jet_grbit"></a><span data-ttu-id="73a3b-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="73a3b-103">JET_GRBIT</span></span>


<span data-ttu-id="73a3b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="73a3b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="73a3b-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="73a3b-105">JET_GRBIT</span></span>

<span data-ttu-id="73a3b-106">Le type de données **JET_GRBIT** est un groupe de bits qui contiennent des constantes spécifiques aux fonctions et structures dans lesquelles il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="73a3b-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="73a3b-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="73a3b-107">Data Types</span></span>

<span data-ttu-id="73a3b-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="73a3b-108">JET_GRBIT</span></span>

<span data-ttu-id="73a3b-109">En général, les constantes utilisées comme valeurs pour ce type de données reflètent le nom de l’élément API dans lequel elles sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="73a3b-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="73a3b-110">Par exemple, toutes les constantes transmises à [JetRetrieveColumn](./jetretrievecolumn-function.md) commencent par « JET_bitRetrieve ».</span><span class="sxs-lookup"><span data-stu-id="73a3b-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="73a3b-111">De même, toutes les constantes transmises à [JetSetColumn](./jetsetcolumn-function.md) commencent par « JET_bitSet ».</span><span class="sxs-lookup"><span data-stu-id="73a3b-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="73a3b-112">La valeur zéro provoque l’ignorance du paramètre.</span><span class="sxs-lookup"><span data-stu-id="73a3b-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="73a3b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="73a3b-113">Remarks</span></span>

<span data-ttu-id="73a3b-114">Pour plus d’informations, consultez la fonction ou la structure spécifique.</span><span class="sxs-lookup"><span data-stu-id="73a3b-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="73a3b-115">Les options sont généralement transmises sous la forme d’un ensemble d’indicateurs qui peuvent être combinés.</span><span class="sxs-lookup"><span data-stu-id="73a3b-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="73a3b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73a3b-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73a3b-117"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="73a3b-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73a3b-118">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="73a3b-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73a3b-119"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="73a3b-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73a3b-120">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="73a3b-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73a3b-121"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="73a3b-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73a3b-122">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="73a3b-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="73a3b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a3b-123">See Also</span></span>

[<span data-ttu-id="73a3b-124">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="73a3b-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="73a3b-125">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="73a3b-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
