---
description: 'En savoir plus sur : méthode API. JetSetCurrentIndex4'
title: API. JetSetCurrentIndex4, méthode
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527187"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="2740e-103">API. JetSetCurrentIndex4, méthode</span><span class="sxs-lookup"><span data-stu-id="2740e-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="2740e-104">Définit l’index actuel d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="2740e-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="2740e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2740e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2740e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2740e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2740e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2740e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="2740e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2740e-108">Parameters</span></span>

  - <span data-ttu-id="2740e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2740e-109">sesid</span></span>  
    <span data-ttu-id="2740e-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2740e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2740e-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2740e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2740e-112">TableID</span><span class="sxs-lookup"><span data-stu-id="2740e-112">tableid</span></span>  
    <span data-ttu-id="2740e-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2740e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2740e-114">Curseur sur lequel définir l’index.</span><span class="sxs-lookup"><span data-stu-id="2740e-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="2740e-115">index</span><span class="sxs-lookup"><span data-stu-id="2740e-115">index</span></span>  
    <span data-ttu-id="2740e-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2740e-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2740e-117">Nom de l’index à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2740e-117">The name of the index to be selected.</span></span> <span data-ttu-id="2740e-118">Si la valeur est null ou vide, l’index primaire est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2740e-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="2740e-119">indexid</span><span class="sxs-lookup"><span data-stu-id="2740e-119">indexid</span></span>  
    <span data-ttu-id="2740e-120">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2740e-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="2740e-121">ID de l’index à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2740e-121">The id of the index to select.</span></span> <span data-ttu-id="2740e-122">Cet ID peut être obtenu à l’aide de JetGetIndexInfo ou JetGetTableIndexInfo avec l’option [IndexID contient](./jet-idxinfo-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="2740e-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="2740e-123">grbit</span><span class="sxs-lookup"><span data-stu-id="2740e-123">grbit</span></span>  
    <span data-ttu-id="2740e-124">Type : [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2740e-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2740e-125">Définissez les options d’index.</span><span class="sxs-lookup"><span data-stu-id="2740e-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="2740e-126">itagSequence</span><span class="sxs-lookup"><span data-stu-id="2740e-126">itagSequence</span></span>  
    <span data-ttu-id="2740e-127">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2740e-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2740e-128">Numéro de séquence de la valeur de colonne à valeurs multiples qui sera utilisée pour positionner le curseur sur le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="2740e-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="2740e-129">Ce paramètre est utilisé uniquement conjointement avec [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="2740e-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="2740e-130">Lorsque ce paramètre n’est pas présent ou qu’il est défini sur zéro, sa valeur est supposée être 1.</span><span class="sxs-lookup"><span data-stu-id="2740e-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="2740e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2740e-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2740e-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2740e-132">Reference</span></span>

[<span data-ttu-id="2740e-133">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="2740e-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2740e-134">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="2740e-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2740e-135">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2740e-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
