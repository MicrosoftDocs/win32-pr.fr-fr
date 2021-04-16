---
description: 'En savoir plus sur : méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit)'
title: Méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. esent. Interop. d’un)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201729"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a><span data-ttu-id="8daf2-103">Méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, Int32, PrereadKeysGrbit)</span><span class="sxs-lookup"><span data-stu-id="8daf2-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="8daf2-104">Si les enregistrements avec les clés spécifiées ne se trouvent pas dans le cache des tampons, démarrez les lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8daf2-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="8daf2-105">**Espace de noms :**[Microsoft. ISAM. esent. Interop.](./microsoft.isam.esent.interop.windows7-namespace.md) une  </span><span class="sxs-lookup"><span data-stu-id="8daf2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="8daf2-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8daf2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8daf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8daf2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8daf2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8daf2-108">Parameters</span></span>

  - <span data-ttu-id="8daf2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8daf2-109">sesid</span></span>  
    <span data-ttu-id="8daf2-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8daf2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8daf2-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8daf2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="8daf2-112">tableid</span></span>  
    <span data-ttu-id="8daf2-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8daf2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8daf2-114">Table avec laquelle émettre les prélectures.</span><span class="sxs-lookup"><span data-stu-id="8daf2-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-115">clés</span><span class="sxs-lookup"><span data-stu-id="8daf2-115">keys</span></span>  
    <span data-ttu-id="8daf2-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="8daf2-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="8daf2-117">Clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="8daf2-117">The keys to preread.</span></span> <span data-ttu-id="8daf2-118">Les clés doivent être triées.</span><span class="sxs-lookup"><span data-stu-id="8daf2-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-119">Caractères de longueur</span><span class="sxs-lookup"><span data-stu-id="8daf2-119">keyLengths</span></span>  
    <span data-ttu-id="8daf2-120">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="8daf2-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="8daf2-121">Longueurs des clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="8daf2-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-122">keyIndex</span><span class="sxs-lookup"><span data-stu-id="8daf2-122">keyIndex</span></span>  
    <span data-ttu-id="8daf2-123">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8daf2-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8daf2-124">Index de la première clé dans le tableau de clés à lire.</span><span class="sxs-lookup"><span data-stu-id="8daf2-124">The index of the first key in the keys array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-125">Nombre de frappes</span><span class="sxs-lookup"><span data-stu-id="8daf2-125">keyCount</span></span>  
    <span data-ttu-id="8daf2-126">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8daf2-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8daf2-127">Nombre maximal de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="8daf2-127">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-128">keysPreread</span><span class="sxs-lookup"><span data-stu-id="8daf2-128">keysPreread</span></span>  
    <span data-ttu-id="8daf2-129">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8daf2-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8daf2-130">Retourne le nombre de clés à prélire réellement.</span><span class="sxs-lookup"><span data-stu-id="8daf2-130">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8daf2-131">grbit</span><span class="sxs-lookup"><span data-stu-id="8daf2-131">grbit</span></span>  
    <span data-ttu-id="8daf2-132">Tapez : [Microsoft. ISAM. esent. Interop. PrereadKeysGrbit.](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8daf2-132">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8daf2-133">Options de prélecture.</span><span class="sxs-lookup"><span data-stu-id="8daf2-133">Preread options.</span></span> <span data-ttu-id="8daf2-134">Utilisé pour spécifier la direction de la prélecture.</span><span class="sxs-lookup"><span data-stu-id="8daf2-134">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="8daf2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8daf2-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8daf2-136">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8daf2-136">Reference</span></span>

[<span data-ttu-id="8daf2-137">Windows7Api, classe</span><span class="sxs-lookup"><span data-stu-id="8daf2-137">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="8daf2-138">Membres Windows7Api</span><span class="sxs-lookup"><span data-stu-id="8daf2-138">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="8daf2-139">Surcharge JetPrereadKeys</span><span class="sxs-lookup"><span data-stu-id="8daf2-139">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="8daf2-140">Espace de noms Microsoft. ISAM. esent. Interop. les</span><span class="sxs-lookup"><span data-stu-id="8daf2-140">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
