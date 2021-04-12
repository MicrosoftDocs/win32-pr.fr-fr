---
description: 'En savoir plus sur : méthode BytesColumnValue. GetValueFromBytes'
title: Méthode BytesColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4651851d6dea72663d002b5f4269f33919e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210190"
---
# <a name="bytescolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="c8ca9-103">Méthode BytesColumnValue. GetValueFromBytes</span><span class="sxs-lookup"><span data-stu-id="c8ca9-103">BytesColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="c8ca9-104">Données récupérées à partir d’ESENT, décoder les données et définir la valeur dans l’objet ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="c8ca9-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8ca9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8ca9-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8ca9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ca9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8ca9-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="c8ca9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8ca9-108">Parameters</span></span>

  - <span data-ttu-id="c8ca9-109">value</span><span class="sxs-lookup"><span data-stu-id="c8ca9-109">value</span></span>  
    <span data-ttu-id="c8ca9-110">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="c8ca9-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="c8ca9-111">Tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8ca9-112">index_début</span><span class="sxs-lookup"><span data-stu-id="c8ca9-112">startIndex</span></span>  
    <span data-ttu-id="c8ca9-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c8ca9-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c8ca9-114">Position de départ dans les octets.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8ca9-115">count</span><span class="sxs-lookup"><span data-stu-id="c8ca9-115">count</span></span>  
    <span data-ttu-id="c8ca9-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c8ca9-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c8ca9-117">Nombre d'octets à décoder.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="c8ca9-118">Raise</span><span class="sxs-lookup"><span data-stu-id="c8ca9-118">err</span></span>  
    <span data-ttu-id="c8ca9-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c8ca9-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c8ca9-120">L’erreur retournée par ESENT.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8ca9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8ca9-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8ca9-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c8ca9-122">Reference</span></span>

[<span data-ttu-id="c8ca9-123">BytesColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="c8ca9-123">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="c8ca9-124">Membres BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="c8ca9-124">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="c8ca9-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c8ca9-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
