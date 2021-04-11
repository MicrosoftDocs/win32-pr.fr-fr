---
description: 'En savoir plus sur : propriété BytesColumnValue. Size'
title: BytesColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101188
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36f6aee31c5fdb61ac124904d07ee59f39728be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203533"
---
# <a name="bytescolumnvaluesize-property"></a><span data-ttu-id="33b70-103">BytesColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="33b70-103">BytesColumnValue.Size property</span></span>

<span data-ttu-id="33b70-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="33b70-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="33b70-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="33b70-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="33b70-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33b70-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33b70-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33b70-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33b70-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33b70-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="33b70-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="33b70-109">Property value</span></span>

<span data-ttu-id="33b70-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="33b70-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="33b70-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33b70-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33b70-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="33b70-112">Reference</span></span>

[<span data-ttu-id="33b70-113">BytesColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="33b70-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="33b70-114">Membres BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="33b70-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="33b70-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="33b70-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
