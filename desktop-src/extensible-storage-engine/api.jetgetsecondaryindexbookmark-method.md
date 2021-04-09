---
description: 'En savoir plus sur : méthode API. JetGetSecondaryIndexBookmark'
title: API. JetGetSecondaryIndexBookmark, méthode
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033908"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="879b6-103">API. JetGetSecondaryIndexBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="879b6-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="879b6-104">Récupère un signet spécial pour l’entrée d’index secondaire à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="879b6-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="879b6-105">Ce signet peut ensuite être utilisé pour repositionner efficacement ce curseur sur la même entrée d’index à l’aide de JetGotoSecondaryIndexBookmark.</span><span class="sxs-lookup"><span data-stu-id="879b6-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="879b6-106">Cela est particulièrement utile lors du repositionnement sur un index secondaire qui contient des clés dupliquées ou qui contient plusieurs entrées d’index pour le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="879b6-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="879b6-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="879b6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="879b6-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="879b6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="879b6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="879b6-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="879b6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="879b6-110">Parameters</span></span>

  - <span data-ttu-id="879b6-111">sesid</span><span class="sxs-lookup"><span data-stu-id="879b6-111">sesid</span></span>  
    <span data-ttu-id="879b6-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="879b6-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="879b6-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="879b6-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-114">TableID</span><span class="sxs-lookup"><span data-stu-id="879b6-114">tableid</span></span>  
    <span data-ttu-id="879b6-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="879b6-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="879b6-116">Curseur à partir duquel récupérer le signet.</span><span class="sxs-lookup"><span data-stu-id="879b6-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="879b6-117">secondaryKey</span></span>  
    <span data-ttu-id="879b6-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="879b6-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="879b6-119">Mémoire tampon de sortie pour la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="879b6-120">secondaryKeySize</span></span>  
    <span data-ttu-id="879b6-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="879b6-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="879b6-122">Taille de la mémoire tampon de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-123">actualSecondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="879b6-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="879b6-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="879b6-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="879b6-125">Retourne la taille de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="879b6-126">primaryKey</span></span>  
    <span data-ttu-id="879b6-127">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="879b6-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="879b6-128">Mémoire tampon de sortie pour la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-129">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="879b6-129">primaryKeySize</span></span>  
    <span data-ttu-id="879b6-130">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="879b6-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="879b6-131">Taille de la mémoire tampon de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-132">actualPrimaryKeySize</span><span class="sxs-lookup"><span data-stu-id="879b6-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="879b6-133">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="879b6-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="879b6-134">Retourne la taille de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="879b6-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="879b6-135">grbit</span><span class="sxs-lookup"><span data-stu-id="879b6-135">grbit</span></span>  
    <span data-ttu-id="879b6-136">Type : [Microsoft. ISAM. esent. Interop. GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="879b6-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="879b6-137">Options pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="879b6-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="879b6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879b6-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="879b6-139">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="879b6-139">Reference</span></span>

[<span data-ttu-id="879b6-140">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="879b6-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="879b6-141">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="879b6-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="879b6-142">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="879b6-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
