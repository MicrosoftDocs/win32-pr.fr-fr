---
description: 'En savoir plus sur : méthode API. MakeKey (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)'
title: Méthode API. MakeKey (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100821
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
ms.openlocfilehash: 0d638c3f63cf99a65e363ca13d1347cced4f1962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320330"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-byte-makekeygrbit"></a><span data-ttu-id="49d03-103">Méthode API. MakeKey (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="49d03-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</span></span>

<span data-ttu-id="49d03-104">Construit une clé de recherche qui peut ensuite être utilisée par [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) et [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="49d03-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="49d03-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49d03-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49d03-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49d03-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49d03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49d03-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="49d03-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49d03-108">Parameters</span></span>

  - <span data-ttu-id="49d03-109">sesid</span><span class="sxs-lookup"><span data-stu-id="49d03-109">sesid</span></span>  
    <span data-ttu-id="49d03-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49d03-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="49d03-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="49d03-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="49d03-112">TableID</span><span class="sxs-lookup"><span data-stu-id="49d03-112">tableid</span></span>  
    <span data-ttu-id="49d03-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49d03-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="49d03-114">Curseur sur lequel créer la clé.</span><span class="sxs-lookup"><span data-stu-id="49d03-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="49d03-115">data</span><span class="sxs-lookup"><span data-stu-id="49d03-115">data</span></span>  
    <span data-ttu-id="49d03-116">Type : [System. Byte](/dotnet/api/system.byte)</span><span class="sxs-lookup"><span data-stu-id="49d03-116">Type: [System.Byte](/dotnet/api/system.byte)</span></span>  
    
    <span data-ttu-id="49d03-117">Données de colonne pour la colonne clé actuelle de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="49d03-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="49d03-118">grbit</span><span class="sxs-lookup"><span data-stu-id="49d03-118">grbit</span></span>  
    <span data-ttu-id="49d03-119">Type : [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="49d03-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="49d03-120">Options de clé.</span><span class="sxs-lookup"><span data-stu-id="49d03-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="49d03-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49d03-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49d03-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="49d03-122">Reference</span></span>

[<span data-ttu-id="49d03-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="49d03-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="49d03-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="49d03-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="49d03-125">Surcharge MakeKey</span><span class="sxs-lookup"><span data-stu-id="49d03-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="49d03-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="49d03-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
