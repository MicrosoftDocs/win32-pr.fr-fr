---
description: 'En savoir plus sur : méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, SetColumnGrbit, JET_SETINFO)'
title: Méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545136"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="4feab-103">Méthode API. JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, SetColumnGrbit, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="4feab-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="4feab-104">La fonction JetSetColumn modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="4feab-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="4feab-105">Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue (une colonne de type [LONGTEXT](./jet-coltyp-enumeration.md) ou [LONGBINARY](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="4feab-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="4feab-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4feab-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4feab-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4feab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4feab-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="4feab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4feab-109">Parameters</span></span>

  - <span data-ttu-id="4feab-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4feab-110">sesid</span></span>  
    <span data-ttu-id="4feab-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4feab-112">Session qui effectue la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4feab-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4feab-113">tableid</span></span>  
    <span data-ttu-id="4feab-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4feab-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="4feab-115">The cursor to update.</span></span> <span data-ttu-id="4feab-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="4feab-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-117">columnid</span><span class="sxs-lookup"><span data-stu-id="4feab-117">columnid</span></span>  
    <span data-ttu-id="4feab-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4feab-119">ColumnID à définir.</span><span class="sxs-lookup"><span data-stu-id="4feab-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-120">data</span><span class="sxs-lookup"><span data-stu-id="4feab-120">data</span></span>  
    <span data-ttu-id="4feab-121">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="4feab-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="4feab-122">Données à définir.</span><span class="sxs-lookup"><span data-stu-id="4feab-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="4feab-123">dataSize</span></span>  
    <span data-ttu-id="4feab-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4feab-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4feab-125">Taille des données à définir.</span><span class="sxs-lookup"><span data-stu-id="4feab-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-126">grbit</span><span class="sxs-lookup"><span data-stu-id="4feab-126">grbit</span></span>  
    <span data-ttu-id="4feab-127">Type : [Microsoft. ISAM. esent. Interop. SetColumnGrbit](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4feab-128">Options SetColumn.</span><span class="sxs-lookup"><span data-stu-id="4feab-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="4feab-129">setinfo</span><span class="sxs-lookup"><span data-stu-id="4feab-129">setinfo</span></span>  
    <span data-ttu-id="4feab-130">Type : [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="4feab-131">Utilisé pour spécifier ITAG ou un décalage de valeur long.</span><span class="sxs-lookup"><span data-stu-id="4feab-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4feab-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4feab-132">Return value</span></span>

<span data-ttu-id="4feab-133">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4feab-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="4feab-134">Code d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="4feab-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="4feab-135">Notes</span><span class="sxs-lookup"><span data-stu-id="4feab-135">Remarks</span></span>

<span data-ttu-id="4feab-136">Les méthodes SetColumn fournissent des substitutions spécifiques au type de données qui peuvent être plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="4feab-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="4feab-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4feab-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4feab-138">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4feab-138">Reference</span></span>

[<span data-ttu-id="4feab-139">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="4feab-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4feab-140">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="4feab-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4feab-141">Surcharge JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="4feab-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="4feab-142">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4feab-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
