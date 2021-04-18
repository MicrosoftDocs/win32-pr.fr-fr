---
description: 'En savoir plus sur : méthode API. JetDeleteColumn2'
title: API. JetDeleteColumn2, méthode
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516227"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="1a4ab-103">API. JetDeleteColumn2, méthode</span><span class="sxs-lookup"><span data-stu-id="1a4ab-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="1a4ab-104">Supprime une colonne d’une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="1a4ab-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="1a4ab-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a4ab-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a4ab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1a4ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a4ab-108">Parameters</span></span>

  - <span data-ttu-id="1a4ab-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1a4ab-109">sesid</span></span>  
    <span data-ttu-id="1a4ab-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a4ab-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1a4ab-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a4ab-112">TableID</span><span class="sxs-lookup"><span data-stu-id="1a4ab-112">tableid</span></span>  
    <span data-ttu-id="1a4ab-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1a4ab-114">Curseur sur la table à partir duquel supprimer la colonne.</span><span class="sxs-lookup"><span data-stu-id="1a4ab-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a4ab-115">colonne</span><span class="sxs-lookup"><span data-stu-id="1a4ab-115">column</span></span>  
    <span data-ttu-id="1a4ab-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1a4ab-117">Nom de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="1a4ab-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a4ab-118">grbit</span><span class="sxs-lookup"><span data-stu-id="1a4ab-118">grbit</span></span>  
    <span data-ttu-id="1a4ab-119">Type : [Microsoft. ISAM. esent. Interop. DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1a4ab-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1a4ab-120">Options de suppression de colonne.</span><span class="sxs-lookup"><span data-stu-id="1a4ab-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a4ab-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a4ab-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a4ab-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1a4ab-122">Reference</span></span>

[<span data-ttu-id="1a4ab-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="1a4ab-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a4ab-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="1a4ab-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a4ab-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a4ab-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
