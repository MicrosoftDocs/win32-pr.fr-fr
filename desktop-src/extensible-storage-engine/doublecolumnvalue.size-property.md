---
description: 'En savoir plus sur : propriété DoubleColumnValue. Size'
title: DoubleColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.DoubleColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.doublecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f3f2951f697c3091fa3f31893e4bf2b5ade8c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531742"
---
# <a name="doublecolumnvaluesize-property"></a><span data-ttu-id="14f99-103">DoubleColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="14f99-103">DoubleColumnValue.Size property</span></span>

<span data-ttu-id="14f99-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="14f99-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="14f99-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="14f99-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="14f99-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14f99-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14f99-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14f99-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14f99-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14f99-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="14f99-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="14f99-109">Property value</span></span>

<span data-ttu-id="14f99-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="14f99-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="14f99-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14f99-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14f99-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="14f99-112">Reference</span></span>

[<span data-ttu-id="14f99-113">DoubleColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="14f99-113">DoubleColumnValue class</span></span>](./doublecolumnvalue-class.md)

[<span data-ttu-id="14f99-114">Membres DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="14f99-114">DoubleColumnValue members</span></span>](./doublecolumnvalue-members.md)

[<span data-ttu-id="14f99-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="14f99-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
