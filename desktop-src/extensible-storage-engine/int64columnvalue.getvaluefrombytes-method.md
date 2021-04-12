---
description: 'En savoir plus sur : méthode Int64ColumnValue. GetValueFromBytes'
title: Méthode Int64ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103365
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a33d85fb929f61d67d814ad47eb64406b77e7c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320753"
---
# <a name="int64columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="4f684-103">Méthode Int64ColumnValue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="4f684-103">Int64ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="4f684-104">Données récupérées à partir d’ESENT, décoder les données et définir la valeur dans l’objet ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="4f684-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="4f684-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f684-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f684-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f684-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f684-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f684-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="4f684-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f684-108">Parameters</span></span>

  - <span data-ttu-id="4f684-109">value</span><span class="sxs-lookup"><span data-stu-id="4f684-109">value</span></span>  
    <span data-ttu-id="4f684-110">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="4f684-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="4f684-111">Tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="4f684-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f684-112">index_début</span><span class="sxs-lookup"><span data-stu-id="4f684-112">startIndex</span></span>  
    <span data-ttu-id="4f684-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4f684-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4f684-114">Position de départ dans les octets.</span><span class="sxs-lookup"><span data-stu-id="4f684-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f684-115">count</span><span class="sxs-lookup"><span data-stu-id="4f684-115">count</span></span>  
    <span data-ttu-id="4f684-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4f684-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4f684-117">Nombre d'octets à décoder.</span><span class="sxs-lookup"><span data-stu-id="4f684-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f684-118">Raise</span><span class="sxs-lookup"><span data-stu-id="4f684-118">err</span></span>  
    <span data-ttu-id="4f684-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4f684-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4f684-120">L’erreur retournée par ESENT.</span><span class="sxs-lookup"><span data-stu-id="4f684-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f684-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f684-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f684-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4f684-122">Reference</span></span>

[<span data-ttu-id="4f684-123">Int64ColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="4f684-123">Int64ColumnValue class</span></span>](./int64columnvalue-class.md)

[<span data-ttu-id="4f684-124">Membres Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="4f684-124">Int64ColumnValue members</span></span>](./int64columnvalue-members.md)

[<span data-ttu-id="4f684-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4f684-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
