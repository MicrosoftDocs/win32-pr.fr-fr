---
description: 'En savoir plus sur : propriété UInt64ColumnValue. Size'
title: UInt64ColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8102b08ce8a48bb23a3618fe5829c354f200ff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865597"
---
# <a name="uint64columnvaluesize-property"></a><span data-ttu-id="7d243-103">UInt64ColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="7d243-103">UInt64ColumnValue.Size property</span></span>

<span data-ttu-id="7d243-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="7d243-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="7d243-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="7d243-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="7d243-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d243-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d243-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d243-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d243-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d243-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="7d243-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7d243-109">Property value</span></span>

<span data-ttu-id="7d243-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7d243-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d243-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d243-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d243-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7d243-112">Reference</span></span>

[<span data-ttu-id="7d243-113">UInt64ColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="7d243-113">UInt64ColumnValue class</span></span>](./uint64columnvalue-class.md)

[<span data-ttu-id="7d243-114">Membres UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7d243-114">UInt64ColumnValue members</span></span>](./uint64columnvalue-members.md)

[<span data-ttu-id="7d243-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7d243-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
