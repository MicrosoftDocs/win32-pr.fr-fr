---
description: 'En savoir plus sur : méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)'
title: Méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32 , JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32[],Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100746
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1706fc554eedd4a8a9365263b93c5763fb350a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514240"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-int32--jet_tblinfo"></a><span data-ttu-id="d9d4a-103">Méthode API. JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32 , JET_TblInfo)</span></span>

<span data-ttu-id="d9d4a-104">Récupère différents éléments d’informations sur une table dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="d9d4a-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="d9d4a-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9d4a-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9d4a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    result As Integer(), _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As Integer()
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int[] result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="d9d4a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9d4a-108">Parameters</span></span>

  - <span data-ttu-id="d9d4a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d9d4a-109">sesid</span></span>  
    <span data-ttu-id="d9d4a-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d9d4a-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d9d4a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9d4a-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d9d4a-112">tableid</span></span>  
    <span data-ttu-id="d9d4a-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d9d4a-114">Table dont les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="d9d4a-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9d4a-115">result</span><span class="sxs-lookup"><span data-stu-id="d9d4a-115">result</span></span>  
    <span data-ttu-id="d9d4a-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="d9d4a-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="d9d4a-117">Informations récupérées.</span><span class="sxs-lookup"><span data-stu-id="d9d4a-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9d4a-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="d9d4a-118">infoLevel</span></span>  
    <span data-ttu-id="d9d4a-119">Type : [Microsoft.ISAM.esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d9d4a-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="d9d4a-120">Type d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d9d4a-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d4a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d9d4a-121">Remarks</span></span>

<span data-ttu-id="d9d4a-122">Cette surcharge est utilisée avec [SpaceUsage](./jet-tblinfo-enumeration.md) et [SpaceAlloc](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d9d4a-122">This overload is used with [SpaceUsage](./jet-tblinfo-enumeration.md) and [SpaceAlloc](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9d4a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9d4a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9d4a-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d9d4a-124">Reference</span></span>

[<span data-ttu-id="d9d4a-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d9d4a-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d9d4a-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d9d4a-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d9d4a-127">Surcharge JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="d9d4a-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="d9d4a-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9d4a-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
