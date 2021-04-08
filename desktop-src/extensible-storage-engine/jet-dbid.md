---
description: 'En savoir plus sur : JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751373"
---
# <a name="jet_dbid"></a><span data-ttu-id="c10ea-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="c10ea-103">JET_DBID</span></span>


<span data-ttu-id="c10ea-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c10ea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="c10ea-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="c10ea-105">JET_DBID</span></span>

<span data-ttu-id="c10ea-106">Le type de données **JET_DBID** contient le descripteur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c10ea-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="c10ea-107">Un descripteur de base de données est utilisé pour gérer le schéma d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="c10ea-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="c10ea-108">Il peut également être utilisé pour gérer les tables à l’intérieur de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="c10ea-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="c10ea-109">Types de données</span><span class="sxs-lookup"><span data-stu-id="c10ea-109">Data Types</span></span>

<span data-ttu-id="c10ea-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="c10ea-110">JET_DBID</span></span>

<span data-ttu-id="c10ea-111">Handle de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c10ea-111">Handle to the database.</span></span>

<span data-ttu-id="c10ea-112">La valeur JET_dbidNil indique que le handle n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c10ea-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="c10ea-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c10ea-113">Remarks</span></span>

<span data-ttu-id="c10ea-114">Un descripteur de base de données est créé au moyen d’un appel à [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c10ea-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="c10ea-115">Un descripteur de base de données peut être explicitement fermé par [JetCloseDatabase](./jetclosedatabase-function.md) ou fermé implicitement par [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="c10ea-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="c10ea-116">Un descripteur de base de données peut être utilisé uniquement dans la session dans laquelle il a été créé.</span><span class="sxs-lookup"><span data-stu-id="c10ea-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="c10ea-117">L’existence d’un descripteur de base de données correspond à l’ouverture logique d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="c10ea-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="c10ea-118">Une ouverture logique est différente de l’ouverture physique d’une base de données, qui se produit lorsqu’une base de données est attachée au système.</span><span class="sxs-lookup"><span data-stu-id="c10ea-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="c10ea-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c10ea-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c10ea-120"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c10ea-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c10ea-121">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c10ea-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c10ea-122"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c10ea-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c10ea-123">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c10ea-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c10ea-124"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c10ea-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c10ea-125">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c10ea-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c10ea-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c10ea-126">See Also</span></span>

[<span data-ttu-id="c10ea-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="c10ea-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="c10ea-128">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="c10ea-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="c10ea-129">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="c10ea-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="c10ea-130">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="c10ea-130">JetEndSession</span></span>](./jetendsession-function.md)
