---
description: 'En savoir plus sur : propriété ColumnValue. Size'
title: ColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101207
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20893eba6516b53045463ce664cdb77ae7e9b768
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034112"
---
# <a name="columnvaluesize-property"></a><span data-ttu-id="53209-103">ColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="53209-103">ColumnValue.Size property</span></span>

<span data-ttu-id="53209-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="53209-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="53209-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="53209-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="53209-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53209-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53209-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53209-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53209-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53209-108">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected abstract int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="53209-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="53209-109">Property value</span></span>

<span data-ttu-id="53209-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53209-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="53209-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53209-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53209-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="53209-112">Reference</span></span>

[<span data-ttu-id="53209-113">ColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="53209-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="53209-114">Membres ColumnValue</span><span class="sxs-lookup"><span data-stu-id="53209-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="53209-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53209-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
