---
description: 'En savoir plus sur : propriété ByteColumnValue. Size'
title: ByteColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94679812f0bdebd043bda3596fceffad6eb2fd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531743"
---
# <a name="bytecolumnvaluesize-property"></a><span data-ttu-id="cb143-103">ByteColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="cb143-103">ByteColumnValue.Size property</span></span>

<span data-ttu-id="cb143-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="cb143-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="cb143-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="cb143-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="cb143-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb143-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb143-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb143-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb143-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb143-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="cb143-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb143-109">Property value</span></span>

<span data-ttu-id="cb143-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cb143-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb143-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb143-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb143-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cb143-112">Reference</span></span>

[<span data-ttu-id="cb143-113">ByteColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="cb143-113">ByteColumnValue class</span></span>](./bytecolumnvalue-class.md)

[<span data-ttu-id="cb143-114">Membres ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="cb143-114">ByteColumnValue members</span></span>](./bytecolumnvalue-members.md)

[<span data-ttu-id="cb143-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cb143-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
