---
description: 'En savoir plus sur : méthode API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)'
title: Méthode API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100730
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa120cf78001ed608a2385e07f388ae91bc9b425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758986"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-jet_columnid-jet_columndef"></a><span data-ttu-id="f2881-103">Méthode API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="f2881-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span></span>

<span data-ttu-id="f2881-104">Récupère des informations sur une colonne de table.</span><span class="sxs-lookup"><span data-stu-id="f2881-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="f2881-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2881-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2881-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2881-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2881-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2881-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnid, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="f2881-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2881-108">Parameters</span></span>

  - <span data-ttu-id="f2881-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f2881-109">sesid</span></span>  
    <span data-ttu-id="f2881-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2881-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2881-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f2881-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2881-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f2881-112">tableid</span></span>  
    <span data-ttu-id="f2881-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2881-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2881-114">Table contenant la colonne.</span><span class="sxs-lookup"><span data-stu-id="f2881-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2881-115">columnid</span><span class="sxs-lookup"><span data-stu-id="f2881-115">columnid</span></span>  
    <span data-ttu-id="f2881-116">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2881-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f2881-117">ColumnID de la colonne.</span><span class="sxs-lookup"><span data-stu-id="f2881-117">The columnid of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2881-118">columndef</span><span class="sxs-lookup"><span data-stu-id="f2881-118">columndef</span></span>  
    <span data-ttu-id="f2881-119">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="f2881-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="f2881-120">Renseigné avec des informations sur la colonne.</span><span class="sxs-lookup"><span data-stu-id="f2881-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2881-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2881-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2881-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f2881-122">Reference</span></span>

[<span data-ttu-id="f2881-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="f2881-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f2881-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="f2881-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f2881-125">Surcharge JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="f2881-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="f2881-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f2881-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
