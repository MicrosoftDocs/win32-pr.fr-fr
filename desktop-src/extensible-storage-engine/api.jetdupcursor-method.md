---
description: 'En savoir plus sur : méthode API. JetDupCursor'
title: API. JetDupCursor, méthode
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525630"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="8e48a-103">API. JetDupCursor, méthode</span><span class="sxs-lookup"><span data-stu-id="8e48a-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="8e48a-104">Duplique un curseur ouvert et retourne un descripteur au curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8e48a-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="8e48a-105">Si le curseur qui était dupliqué était un curseur en lecture seule, le curseur dupliqué est également un curseur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8e48a-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="8e48a-106">Tout État lié à la construction d’une clé de recherche ou à la mise à jour d’un enregistrement n’est pas copié dans le curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8e48a-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="8e48a-107">En outre, l’emplacement du curseur d’origine n’est pas dupliqué dans le curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8e48a-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="8e48a-108">Le curseur dupliqué est toujours ouvert sur l’index cluster et son emplacement est toujours sur la première ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="8e48a-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="8e48a-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e48a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e48a-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e48a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e48a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e48a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8e48a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e48a-112">Parameters</span></span>

  - <span data-ttu-id="8e48a-113">sesid</span><span class="sxs-lookup"><span data-stu-id="8e48a-113">sesid</span></span>  
    <span data-ttu-id="8e48a-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e48a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e48a-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e48a-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e48a-116">TableID</span><span class="sxs-lookup"><span data-stu-id="8e48a-116">tableid</span></span>  
    <span data-ttu-id="8e48a-117">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e48a-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8e48a-118">Curseur à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="8e48a-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e48a-119">newTableid</span><span class="sxs-lookup"><span data-stu-id="8e48a-119">newTableid</span></span>  
    <span data-ttu-id="8e48a-120">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e48a-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8e48a-121">Curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8e48a-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e48a-122">grbit</span><span class="sxs-lookup"><span data-stu-id="8e48a-122">grbit</span></span>  
    <span data-ttu-id="8e48a-123">Type : [Microsoft. ISAM. esent. Interop. DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8e48a-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8e48a-124">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="8e48a-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e48a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e48a-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e48a-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8e48a-126">Reference</span></span>

[<span data-ttu-id="8e48a-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="8e48a-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8e48a-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="8e48a-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8e48a-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8e48a-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
