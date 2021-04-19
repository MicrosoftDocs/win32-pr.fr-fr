---
description: 'En savoir plus sur : méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)'
title: Méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f52c900521d28c82245db53b98ab376dd82faec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517467"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="e620d-103">Méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="e620d-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="e620d-104">La fonction JetSetColumn modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e620d-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="e620d-105">Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue (une colonne de type [LONGTEXT](./jet-coltyp-enumeration.md) ou [LONGBINARY](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="e620d-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="e620d-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e620d-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e620d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e620d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e620d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="e620d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e620d-109">Parameters</span></span>

  - <span data-ttu-id="e620d-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e620d-110">sesid</span></span>  
    <span data-ttu-id="e620d-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e620d-112">Session qui effectue la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e620d-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e620d-113">tableid</span></span>  
    <span data-ttu-id="e620d-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e620d-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="e620d-115">The cursor to update.</span></span> <span data-ttu-id="e620d-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="e620d-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-117">columnid</span><span class="sxs-lookup"><span data-stu-id="e620d-117">columnid</span></span>  
    <span data-ttu-id="e620d-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e620d-119">ColumnID à définir.</span><span class="sxs-lookup"><span data-stu-id="e620d-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-120">data</span><span class="sxs-lookup"><span data-stu-id="e620d-120">data</span></span>  
    <span data-ttu-id="e620d-121">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="e620d-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="e620d-122">Données à définir.</span><span class="sxs-lookup"><span data-stu-id="e620d-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="e620d-123">dataSize</span></span>  
    <span data-ttu-id="e620d-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e620d-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e620d-125">Taille des données à définir.</span><span class="sxs-lookup"><span data-stu-id="e620d-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-126">dataOffset</span><span class="sxs-lookup"><span data-stu-id="e620d-126">dataOffset</span></span>  
    <span data-ttu-id="e620d-127">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e620d-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e620d-128">Offset de la mémoire tampon de données à partir duquel définir les données.</span><span class="sxs-lookup"><span data-stu-id="e620d-128">The offset in the data buffer to set data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-129">grbit</span><span class="sxs-lookup"><span data-stu-id="e620d-129">grbit</span></span>  
    <span data-ttu-id="e620d-130">Type : [Microsoft. ISAM. esent. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-130">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e620d-131">Options SetColumn.</span><span class="sxs-lookup"><span data-stu-id="e620d-131">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e620d-132">setinfo</span><span class="sxs-lookup"><span data-stu-id="e620d-132">setinfo</span></span>  
    <span data-ttu-id="e620d-133">Type : [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-133">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="e620d-134">Utilisé pour spécifier ITAG ou un décalage de valeur long.</span><span class="sxs-lookup"><span data-stu-id="e620d-134">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e620d-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e620d-135">Return value</span></span>

<span data-ttu-id="e620d-136">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e620d-136">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e620d-137">Valeur d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="e620d-137">A warning value.</span></span>  

## <a name="remarks"></a><span data-ttu-id="e620d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="e620d-138">Remarks</span></span>

<span data-ttu-id="e620d-139">Il s’agit d’une version interne uniquement de l’API qui prend une mémoire tampon de données et un décalage dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e620d-139">This is an internal-only version of the API that takes a data buffer and an offset into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="e620d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e620d-140">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e620d-141">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e620d-141">Reference</span></span>

[<span data-ttu-id="e620d-142">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e620d-142">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e620d-143">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e620d-143">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e620d-144">Surcharge JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="e620d-144">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="e620d-145">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e620d-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
