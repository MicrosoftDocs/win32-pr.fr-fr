---
description: 'En savoir plus sur : méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)'
title: Méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100751
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b4933a2dd80201cd6de87caa392b4d2aad0901e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530712"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexid-jet_idxinfo"></a><span data-ttu-id="19dcc-103">Méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="19dcc-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</span></span>

<span data-ttu-id="19dcc-104">Récupère des informations sur les index d’une table.</span><span class="sxs-lookup"><span data-stu-id="19dcc-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="19dcc-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19dcc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19dcc-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19dcc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19dcc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19dcc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXID, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As JET_INDEXID
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXID result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="19dcc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19dcc-108">Parameters</span></span>

  - <span data-ttu-id="19dcc-109">sesid</span><span class="sxs-lookup"><span data-stu-id="19dcc-109">sesid</span></span>  
    <span data-ttu-id="19dcc-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="19dcc-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="19dcc-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="19dcc-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="19dcc-112">TableID</span><span class="sxs-lookup"><span data-stu-id="19dcc-112">tableid</span></span>  
    <span data-ttu-id="19dcc-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="19dcc-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="19dcc-114">Table pour laquelle récupérer les informations d’index.</span><span class="sxs-lookup"><span data-stu-id="19dcc-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="19dcc-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="19dcc-115">indexname</span></span>  
    <span data-ttu-id="19dcc-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="19dcc-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="19dcc-117">Nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="19dcc-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="19dcc-118">result</span><span class="sxs-lookup"><span data-stu-id="19dcc-118">result</span></span>  
    <span data-ttu-id="19dcc-119">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="19dcc-119">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="19dcc-120">Renseigné avec des informations sur les index de la table.</span><span class="sxs-lookup"><span data-stu-id="19dcc-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="19dcc-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="19dcc-121">infoLevel</span></span>  
    <span data-ttu-id="19dcc-122">Type : [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="19dcc-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="19dcc-123">Type d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="19dcc-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="19dcc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19dcc-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19dcc-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="19dcc-125">Reference</span></span>

[<span data-ttu-id="19dcc-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="19dcc-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="19dcc-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="19dcc-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="19dcc-128">Surcharge JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="19dcc-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="19dcc-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="19dcc-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
