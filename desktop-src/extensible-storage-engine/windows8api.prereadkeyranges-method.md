---
description: 'En savoir plus sur : méthode Windows8Api. PrereadKeyRanges'
title: Méthode Windows8Api. PrereadKeyRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951445"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="26696-103">Méthode Windows8Api. PrereadKeyRanges</span><span class="sxs-lookup"><span data-stu-id="26696-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="26696-104">Si les enregistrements avec les plages de clés spécifiées ne sont pas dans le cache des tampons, démarrez les lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="26696-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="26696-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26696-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="26696-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="26696-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26696-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26696-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="26696-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26696-108">Parameters</span></span>

  - <span data-ttu-id="26696-109">sesid</span><span class="sxs-lookup"><span data-stu-id="26696-109">sesid</span></span>  
    <span data-ttu-id="26696-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26696-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="26696-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="26696-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-112">TableID</span><span class="sxs-lookup"><span data-stu-id="26696-112">tableid</span></span>  
    <span data-ttu-id="26696-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26696-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="26696-114">Table avec laquelle émettre les prélectures.</span><span class="sxs-lookup"><span data-stu-id="26696-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-115">keysStart</span><span class="sxs-lookup"><span data-stu-id="26696-115">keysStart</span></span>  
    <span data-ttu-id="26696-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="26696-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="26696-117">Début des plages de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-118">keyStartLengths</span><span class="sxs-lookup"><span data-stu-id="26696-118">keyStartLengths</span></span>  
    <span data-ttu-id="26696-119">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="26696-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="26696-120">Longueurs des clés de début à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-121">keysend</span><span class="sxs-lookup"><span data-stu-id="26696-121">keysEnd</span></span>  
    <span data-ttu-id="26696-122">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="26696-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="26696-123">Fin de la plage de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-124">keyEndLengths</span><span class="sxs-lookup"><span data-stu-id="26696-124">keyEndLengths</span></span>  
    <span data-ttu-id="26696-125">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="26696-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="26696-126">Longueurs des touches de fin à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="26696-127">rangeIndex</span></span>  
    <span data-ttu-id="26696-128">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="26696-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="26696-129">Index de la première plage de clés dans le tableau à lire.</span><span class="sxs-lookup"><span data-stu-id="26696-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-130">rangeCount</span><span class="sxs-lookup"><span data-stu-id="26696-130">rangeCount</span></span>  
    <span data-ttu-id="26696-131">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="26696-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="26696-132">Nombre maximal de plages de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-133">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="26696-133">rangesPreread</span></span>  
    <span data-ttu-id="26696-134">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="26696-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="26696-135">Retourne le nombre de clés réellement prélues.</span><span class="sxs-lookup"><span data-stu-id="26696-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-136">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="26696-136">columnsPreread</span></span>  
    <span data-ttu-id="26696-137">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="26696-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="26696-138">Liste des ID de colonne pour les colonnes de valeur longue à prélire.</span><span class="sxs-lookup"><span data-stu-id="26696-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="26696-139">grbit</span><span class="sxs-lookup"><span data-stu-id="26696-139">grbit</span></span>  
    <span data-ttu-id="26696-140">Tapez : [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="26696-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="26696-141">Options de prélecture.</span><span class="sxs-lookup"><span data-stu-id="26696-141">Preread options.</span></span> <span data-ttu-id="26696-142">Utilisé pour spécifier la direction de la prélecture.</span><span class="sxs-lookup"><span data-stu-id="26696-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="26696-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26696-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26696-144">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="26696-144">Reference</span></span>

[<span data-ttu-id="26696-145">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="26696-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="26696-146">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="26696-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="26696-147">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="26696-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
