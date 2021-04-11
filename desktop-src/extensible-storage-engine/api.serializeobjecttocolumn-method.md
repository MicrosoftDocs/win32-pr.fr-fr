---
description: 'En savoir plus sur : méthode API. SerializeObjectToColumn'
title: API. SerializeObjectToColumn, méthode
TOCTitle: 'SerializeObjectToColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.serializeobjecttocolumn(v=EXCHG.10)
ms:contentKeyID: 55100915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21b0e421b68287b983fc43482e3a2385b2a160f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203534"
---
# <a name="apiserializeobjecttocolumn-method"></a><span data-ttu-id="b4e4e-103">API. SerializeObjectToColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="b4e4e-103">Api.SerializeObjectToColumn method</span></span>

<span data-ttu-id="b4e4e-104">Écrire une forme sérialisée d’un objet dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-104">Write a serialized form of an object to a column.</span></span>

<span data-ttu-id="b4e4e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4e4e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e4e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4e4e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SerializeObjectToColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    value As Object _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim value As ObjectApi.SerializeObjectToColumn(sesid, _
    tableid, columnid, value)
```

``` csharp
public static void SerializeObjectToColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Object value
)
```

#### <a name="parameters"></a><span data-ttu-id="b4e4e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4e4e-108">Parameters</span></span>

  - <span data-ttu-id="b4e4e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b4e4e-109">sesid</span></span>  
    <span data-ttu-id="b4e4e-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b4e4e-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4e4e-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b4e4e-112">tableid</span></span>  
    <span data-ttu-id="b4e4e-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b4e4e-114">Table dans laquelle écrire.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-114">The table to write to.</span></span> <span data-ttu-id="b4e4e-115">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4e4e-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b4e4e-116">columnid</span></span>  
    <span data-ttu-id="b4e4e-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b4e4e-118">Colonne dans laquelle écrire.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-118">The column to write to.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4e4e-119">value</span><span class="sxs-lookup"><span data-stu-id="b4e4e-119">value</span></span>  
    <span data-ttu-id="b4e4e-120">Type : [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="b4e4e-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="b4e4e-121">Objet à écrire.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-121">The object to write.</span></span> <span data-ttu-id="b4e4e-122">L’objet doit être sérialisable.</span><span class="sxs-lookup"><span data-stu-id="b4e4e-122">The object must be serializable.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4e4e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4e4e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4e4e-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b4e4e-124">Reference</span></span>

[<span data-ttu-id="b4e4e-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b4e4e-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b4e4e-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b4e4e-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b4e4e-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4e4e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
