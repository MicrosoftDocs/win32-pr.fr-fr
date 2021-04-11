---
description: 'En savoir plus sur : méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)'
title: Méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
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
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201774"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="11ba4-103">Méthode API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="11ba4-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="11ba4-104">**Remarque : cette API est désormais obsolète.**</span><span class="sxs-lookup"><span data-stu-id="11ba4-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="11ba4-105">Récupère des informations sur les index d’une table.</span><span class="sxs-lookup"><span data-stu-id="11ba4-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="11ba4-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11ba4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="11ba4-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="11ba4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11ba4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11ba4-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="11ba4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11ba4-109">Parameters</span></span>

  - <span data-ttu-id="11ba4-110">sesid</span><span class="sxs-lookup"><span data-stu-id="11ba4-110">sesid</span></span>  
    <span data-ttu-id="11ba4-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11ba4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="11ba4-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="11ba4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="11ba4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="11ba4-113">tableid</span></span>  
    <span data-ttu-id="11ba4-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11ba4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="11ba4-115">Table pour laquelle récupérer les informations d’index.</span><span class="sxs-lookup"><span data-stu-id="11ba4-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="11ba4-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="11ba4-116">indexname</span></span>  
    <span data-ttu-id="11ba4-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="11ba4-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="11ba4-118">Ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="11ba4-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="11ba4-119">indexlist</span><span class="sxs-lookup"><span data-stu-id="11ba4-119">indexlist</span></span>  
    <span data-ttu-id="11ba4-120">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="11ba4-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="11ba4-121">Renseigné avec des informations sur les index de la table.</span><span class="sxs-lookup"><span data-stu-id="11ba4-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="11ba4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11ba4-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11ba4-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="11ba4-123">Reference</span></span>

[<span data-ttu-id="11ba4-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="11ba4-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="11ba4-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="11ba4-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="11ba4-126">Surcharge JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="11ba4-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="11ba4-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="11ba4-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
