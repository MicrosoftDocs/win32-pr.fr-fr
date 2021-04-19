---
description: 'En savoir plus sur : méthode API. JetGotoSecondaryIndexBookmark'
title: API. JetGotoSecondaryIndexBookmark, méthode
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526311"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="36554-103">API. JetGotoSecondaryIndexBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="36554-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="36554-104">Positionne un curseur sur une entrée d’index associée au signet d’index secondaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="36554-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="36554-105">Le signet de l’index secondaire doit être utilisé avec le même index sur la même table que celle à partir de laquelle il a été récupéré à l’origine.</span><span class="sxs-lookup"><span data-stu-id="36554-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="36554-106">Le signet d’index secondaire d’une entrée d’index peut être récupéré à l’aide de JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit).</span><span class="sxs-lookup"><span data-stu-id="36554-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="36554-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36554-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36554-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36554-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36554-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36554-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="36554-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36554-110">Parameters</span></span>

  - <span data-ttu-id="36554-111">sesid</span><span class="sxs-lookup"><span data-stu-id="36554-111">sesid</span></span>  
    <span data-ttu-id="36554-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36554-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="36554-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="36554-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-114">TableID</span><span class="sxs-lookup"><span data-stu-id="36554-114">tableid</span></span>  
    <span data-ttu-id="36554-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36554-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="36554-116">Curseur de la table à positionner.</span><span class="sxs-lookup"><span data-stu-id="36554-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="36554-117">secondaryKey</span></span>  
    <span data-ttu-id="36554-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="36554-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="36554-119">Mémoire tampon qui contient la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="36554-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="36554-120">secondaryKeySize</span></span>  
    <span data-ttu-id="36554-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="36554-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="36554-122">Taille de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="36554-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="36554-123">primaryKey</span></span>  
    <span data-ttu-id="36554-124">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="36554-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="36554-125">Mémoire tampon qui contient la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="36554-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-126">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="36554-126">primaryKeySize</span></span>  
    <span data-ttu-id="36554-127">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="36554-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="36554-128">Taille de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="36554-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="36554-129">grbit</span><span class="sxs-lookup"><span data-stu-id="36554-129">grbit</span></span>  
    <span data-ttu-id="36554-130">Type : [Microsoft. ISAM. esent. Interop. GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="36554-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="36554-131">Options de positionnement du signet.</span><span class="sxs-lookup"><span data-stu-id="36554-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="36554-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36554-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36554-133">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="36554-133">Reference</span></span>

[<span data-ttu-id="36554-134">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="36554-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="36554-135">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="36554-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="36554-136">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36554-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
