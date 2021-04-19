---
description: 'En savoir plus sur : méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)'
title: Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100931
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e43711f40c723e84476bd8d2aa79f3761f87b9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527763"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint64"></a><span data-ttu-id="4ba9f-103">Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</span></span>

<span data-ttu-id="4ba9f-104">Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="4ba9f-105">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="4ba9f-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ba9f-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba9f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ba9f-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As ULong _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As ULongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    ulong data
)
```

#### <a name="parameters"></a><span data-ttu-id="4ba9f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ba9f-109">Parameters</span></span>

  - <span data-ttu-id="4ba9f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4ba9f-110">sesid</span></span>  
    <span data-ttu-id="4ba9f-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4ba9f-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ba9f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4ba9f-113">tableid</span></span>  
    <span data-ttu-id="4ba9f-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4ba9f-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-115">The cursor to update.</span></span> <span data-ttu-id="4ba9f-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ba9f-117">columnid</span><span class="sxs-lookup"><span data-stu-id="4ba9f-117">columnid</span></span>  
    <span data-ttu-id="4ba9f-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4ba9f-119">ColumnID à définir.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ba9f-120">data</span><span class="sxs-lookup"><span data-stu-id="4ba9f-120">data</span></span>  
    <span data-ttu-id="4ba9f-121">Type : [System. UInt64](/dotnet/api/system.uint64)</span><span class="sxs-lookup"><span data-stu-id="4ba9f-121">Type: [System.UInt64](/dotnet/api/system.uint64)</span></span>  
    
    <span data-ttu-id="4ba9f-122">Données à définir.</span><span class="sxs-lookup"><span data-stu-id="4ba9f-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ba9f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ba9f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ba9f-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4ba9f-124">Reference</span></span>

[<span data-ttu-id="4ba9f-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="4ba9f-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4ba9f-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="4ba9f-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4ba9f-127">Surcharge SetColumn</span><span class="sxs-lookup"><span data-stu-id="4ba9f-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="4ba9f-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4ba9f-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
