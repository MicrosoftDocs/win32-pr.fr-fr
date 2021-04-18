---
description: 'En savoir plus sur : méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)'
title: Méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt64,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100827
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cb4b26015e67e6801fe0e19ee0b0ca8d41ac4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520668"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint64-makekeygrbit"></a><span data-ttu-id="98b25-103">Méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="98b25-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</span></span>

<span data-ttu-id="98b25-104">Construit une clé de recherche qui peut ensuite être utilisée par [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) et [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="98b25-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="98b25-105">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="98b25-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="98b25-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98b25-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="98b25-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="98b25-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98b25-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98b25-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As ULong, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As ULong
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ulong data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="98b25-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98b25-109">Parameters</span></span>

  - <span data-ttu-id="98b25-110">sesid</span><span class="sxs-lookup"><span data-stu-id="98b25-110">sesid</span></span>  
    <span data-ttu-id="98b25-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98b25-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="98b25-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="98b25-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="98b25-113">TableID</span><span class="sxs-lookup"><span data-stu-id="98b25-113">tableid</span></span>  
    <span data-ttu-id="98b25-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98b25-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="98b25-115">Curseur sur lequel créer la clé.</span><span class="sxs-lookup"><span data-stu-id="98b25-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="98b25-116">data</span><span class="sxs-lookup"><span data-stu-id="98b25-116">data</span></span>  
    <span data-ttu-id="98b25-117">Type : [System. UInt64](/dotnet/api/system.uint64)</span><span class="sxs-lookup"><span data-stu-id="98b25-117">Type: [System.UInt64](/dotnet/api/system.uint64)</span></span>  
    
    <span data-ttu-id="98b25-118">Données de colonne pour la colonne clé actuelle de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="98b25-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="98b25-119">grbit</span><span class="sxs-lookup"><span data-stu-id="98b25-119">grbit</span></span>  
    <span data-ttu-id="98b25-120">Type : [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="98b25-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="98b25-121">Options de clé.</span><span class="sxs-lookup"><span data-stu-id="98b25-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="98b25-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b25-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98b25-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="98b25-123">Reference</span></span>

[<span data-ttu-id="98b25-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="98b25-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="98b25-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="98b25-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="98b25-126">Surcharge MakeKey</span><span class="sxs-lookup"><span data-stu-id="98b25-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="98b25-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="98b25-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
