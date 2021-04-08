---
description: 'En savoir plus sur : méthode API. TrySeek'
title: API. TrySeek, méthode
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862222"
---
# <a name="apitryseek-method"></a><span data-ttu-id="42045-103">API. TrySeek, méthode</span><span class="sxs-lookup"><span data-stu-id="42045-103">Api.TrySeek method</span></span>

<span data-ttu-id="42045-104">Positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="42045-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="42045-105">Une clé de recherche doit avoir été construite précédemment à l’aide de JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="42045-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="42045-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42045-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42045-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42045-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42045-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42045-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="42045-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42045-109">Parameters</span></span>

  - <span data-ttu-id="42045-110">sesid</span><span class="sxs-lookup"><span data-stu-id="42045-110">sesid</span></span>  
    <span data-ttu-id="42045-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42045-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="42045-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="42045-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="42045-113">TableID</span><span class="sxs-lookup"><span data-stu-id="42045-113">tableid</span></span>  
    <span data-ttu-id="42045-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42045-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="42045-115">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="42045-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="42045-116">grbit</span><span class="sxs-lookup"><span data-stu-id="42045-116">grbit</span></span>  
    <span data-ttu-id="42045-117">Type : [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="42045-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="42045-118">Option Seek.</span><span class="sxs-lookup"><span data-stu-id="42045-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="42045-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42045-119">Return value</span></span>

<span data-ttu-id="42045-120">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="42045-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="42045-121">True si un enregistrement correspondant au critère a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="42045-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42045-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42045-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42045-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="42045-123">Reference</span></span>

[<span data-ttu-id="42045-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="42045-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="42045-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="42045-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="42045-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="42045-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
