---
description: 'En savoir plus sur : méthode API. JetEscrowUpdate'
title: API. JetEscrowUpdate, méthode
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514404"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="96322-103">API. JetEscrowUpdate, méthode</span><span class="sxs-lookup"><span data-stu-id="96322-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="96322-104">Effectue une opération d’addition atomique sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="96322-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="96322-105">Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits.</span><span class="sxs-lookup"><span data-stu-id="96322-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="96322-106">Voir aussi [EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="96322-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="96322-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="96322-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="96322-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="96322-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="96322-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96322-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="96322-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96322-110">Parameters</span></span>

  - <span data-ttu-id="96322-111">sesid</span><span class="sxs-lookup"><span data-stu-id="96322-111">sesid</span></span>  
    <span data-ttu-id="96322-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="96322-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="96322-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="96322-113">The session to use.</span></span> <span data-ttu-id="96322-114">La session doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="96322-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-115">TableID</span><span class="sxs-lookup"><span data-stu-id="96322-115">tableid</span></span>  
    <span data-ttu-id="96322-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="96322-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="96322-117">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="96322-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-118">columnid</span><span class="sxs-lookup"><span data-stu-id="96322-118">columnid</span></span>  
    <span data-ttu-id="96322-119">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="96322-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="96322-120">Colonne à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="96322-120">The column to update.</span></span> <span data-ttu-id="96322-121">Il doit s’agir d’une colonne pouvant être mise à jour par dépôt.</span><span class="sxs-lookup"><span data-stu-id="96322-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-122">delta</span><span class="sxs-lookup"><span data-stu-id="96322-122">delta</span></span>  
    <span data-ttu-id="96322-123">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="96322-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="96322-124">Mémoire tampon contenant le addend.</span><span class="sxs-lookup"><span data-stu-id="96322-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-125">pas de différentiel</span><span class="sxs-lookup"><span data-stu-id="96322-125">deltaSize</span></span>  
    <span data-ttu-id="96322-126">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96322-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96322-127">Taille du addend.</span><span class="sxs-lookup"><span data-stu-id="96322-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-128">previousValue</span><span class="sxs-lookup"><span data-stu-id="96322-128">previousValue</span></span>  
    <span data-ttu-id="96322-129">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="96322-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="96322-130">Mémoire tampon de sortie qui recevra la valeur actuelle de la colonne.</span><span class="sxs-lookup"><span data-stu-id="96322-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="96322-131">Cette mémoire tampon peut être null.</span><span class="sxs-lookup"><span data-stu-id="96322-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-132">previousValueLength</span><span class="sxs-lookup"><span data-stu-id="96322-132">previousValueLength</span></span>  
    <span data-ttu-id="96322-133">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96322-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96322-134">Taille de la mémoire tampon previousValue.</span><span class="sxs-lookup"><span data-stu-id="96322-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-135">actualPreviousValueLength</span><span class="sxs-lookup"><span data-stu-id="96322-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="96322-136">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="96322-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="96322-137">Retourne la taille réelle du previousValue.</span><span class="sxs-lookup"><span data-stu-id="96322-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="96322-138">grbit</span><span class="sxs-lookup"><span data-stu-id="96322-138">grbit</span></span>  
    <span data-ttu-id="96322-139">Type : [Microsoft. ISAM. esent. Interop. EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="96322-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="96322-140">Options de mise à jour du tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="96322-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="96322-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96322-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96322-142">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="96322-142">Reference</span></span>

[<span data-ttu-id="96322-143">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="96322-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="96322-144">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="96322-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="96322-145">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="96322-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
