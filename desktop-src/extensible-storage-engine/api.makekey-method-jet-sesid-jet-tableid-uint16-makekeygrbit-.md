---
description: 'En savoir plus sur : méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)'
title: Méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt16,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100844
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41df8909993b6c274d1a85737b13c2f618bc8fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522422"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint16-makekeygrbit"></a><span data-ttu-id="aacd3-103">Méthode API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="aacd3-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</span></span>

<span data-ttu-id="aacd3-104">Construit une clé de recherche qui peut ensuite être utilisée par [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) et [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="aacd3-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="aacd3-105">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="aacd3-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="aacd3-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aacd3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aacd3-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aacd3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aacd3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aacd3-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UShort, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UShort
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ushort data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="aacd3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aacd3-109">Parameters</span></span>

  - <span data-ttu-id="aacd3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="aacd3-110">sesid</span></span>  
    <span data-ttu-id="aacd3-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aacd3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="aacd3-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="aacd3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="aacd3-113">TableID</span><span class="sxs-lookup"><span data-stu-id="aacd3-113">tableid</span></span>  
    <span data-ttu-id="aacd3-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aacd3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="aacd3-115">Curseur sur lequel créer la clé.</span><span class="sxs-lookup"><span data-stu-id="aacd3-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="aacd3-116">data</span><span class="sxs-lookup"><span data-stu-id="aacd3-116">data</span></span>  
    <span data-ttu-id="aacd3-117">Type : [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="aacd3-117">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="aacd3-118">Données de colonne pour la colonne clé actuelle de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="aacd3-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="aacd3-119">grbit</span><span class="sxs-lookup"><span data-stu-id="aacd3-119">grbit</span></span>  
    <span data-ttu-id="aacd3-120">Type : [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aacd3-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="aacd3-121">Options de clé.</span><span class="sxs-lookup"><span data-stu-id="aacd3-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="aacd3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aacd3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aacd3-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="aacd3-123">Reference</span></span>

[<span data-ttu-id="aacd3-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="aacd3-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="aacd3-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="aacd3-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="aacd3-126">Surcharge MakeKey</span><span class="sxs-lookup"><span data-stu-id="aacd3-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="aacd3-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aacd3-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
