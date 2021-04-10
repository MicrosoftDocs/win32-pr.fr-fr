---
description: 'En savoir plus sur : méthode API. JetMakeKey'
title: API. JetMakeKey, méthode
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952857"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="3dcab-103">API. JetMakeKey, méthode</span><span class="sxs-lookup"><span data-stu-id="3dcab-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="3dcab-104">Construit des clés de recherche qui peuvent ensuite être utilisées par [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) et [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="3dcab-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="3dcab-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3dcab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3dcab-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3dcab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dcab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3dcab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dcab-108">Parameters</span></span>

  - <span data-ttu-id="3dcab-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3dcab-109">sesid</span></span>  
    <span data-ttu-id="3dcab-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3dcab-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3dcab-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3dcab-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dcab-112">TableID</span><span class="sxs-lookup"><span data-stu-id="3dcab-112">tableid</span></span>  
    <span data-ttu-id="3dcab-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3dcab-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3dcab-114">Curseur sur lequel créer la clé.</span><span class="sxs-lookup"><span data-stu-id="3dcab-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dcab-115">data</span><span class="sxs-lookup"><span data-stu-id="3dcab-115">data</span></span>  
    <span data-ttu-id="3dcab-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="3dcab-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="3dcab-117">Données de colonne pour la colonne clé actuelle de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="3dcab-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dcab-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="3dcab-118">dataSize</span></span>  
    <span data-ttu-id="3dcab-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3dcab-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3dcab-120">Taille des données.</span><span class="sxs-lookup"><span data-stu-id="3dcab-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dcab-121">grbit</span><span class="sxs-lookup"><span data-stu-id="3dcab-121">grbit</span></span>  
    <span data-ttu-id="3dcab-122">Type : [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3dcab-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3dcab-123">Options de clé.</span><span class="sxs-lookup"><span data-stu-id="3dcab-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dcab-124">Notes</span><span class="sxs-lookup"><span data-stu-id="3dcab-124">Remarks</span></span>

<span data-ttu-id="3dcab-125">Les fonctions MakeKey fournissent des fonctionnalités de création de clés propres au type de données.</span><span class="sxs-lookup"><span data-stu-id="3dcab-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="3dcab-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dcab-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3dcab-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3dcab-127">Reference</span></span>

[<span data-ttu-id="3dcab-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="3dcab-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3dcab-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="3dcab-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3dcab-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3dcab-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
