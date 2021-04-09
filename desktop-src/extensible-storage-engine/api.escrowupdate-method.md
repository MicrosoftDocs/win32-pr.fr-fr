---
description: 'En savoir plus sur : méthode API. EscrowUpdate'
title: API. EscrowUpdate, méthode
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749508"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="5070a-103">API. EscrowUpdate, méthode</span><span class="sxs-lookup"><span data-stu-id="5070a-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="5070a-104">Effectuer une addition atomique sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="5070a-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="5070a-105">La colonne doit être de type [long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="5070a-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="5070a-106">Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits.</span><span class="sxs-lookup"><span data-stu-id="5070a-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="5070a-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5070a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5070a-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5070a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5070a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5070a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="5070a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5070a-110">Parameters</span></span>

  - <span data-ttu-id="5070a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="5070a-111">sesid</span></span>  
    <span data-ttu-id="5070a-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5070a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5070a-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5070a-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5070a-114">TableID</span><span class="sxs-lookup"><span data-stu-id="5070a-114">tableid</span></span>  
    <span data-ttu-id="5070a-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5070a-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5070a-116">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="5070a-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="5070a-117">columnid</span><span class="sxs-lookup"><span data-stu-id="5070a-117">columnid</span></span>  
    <span data-ttu-id="5070a-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5070a-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5070a-119">Colonne à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="5070a-119">The column to update.</span></span> <span data-ttu-id="5070a-120">Il doit s’agir d’une colonne pouvant être mise à jour par dépôt.</span><span class="sxs-lookup"><span data-stu-id="5070a-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5070a-121">delta</span><span class="sxs-lookup"><span data-stu-id="5070a-121">delta</span></span>  
    <span data-ttu-id="5070a-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5070a-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5070a-123">Delta à appliquer à la colonne.</span><span class="sxs-lookup"><span data-stu-id="5070a-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5070a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5070a-124">Return value</span></span>

<span data-ttu-id="5070a-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5070a-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="5070a-126">Valeur actuelle de la colonne telle qu’elle est stockée dans la base de données (le contrôle de version est ignoré).</span><span class="sxs-lookup"><span data-stu-id="5070a-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="5070a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="5070a-127">Remarks</span></span>

<span data-ttu-id="5070a-128">Cette méthode encapsule [JetEscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="5070a-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5070a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5070a-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5070a-130">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5070a-130">Reference</span></span>

[<span data-ttu-id="5070a-131">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="5070a-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5070a-132">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="5070a-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5070a-133">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5070a-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
