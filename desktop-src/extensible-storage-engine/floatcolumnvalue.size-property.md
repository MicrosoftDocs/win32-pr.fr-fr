---
description: 'En savoir plus sur : propriété FloatColumnValue. Size'
title: FloatColumnValue. Size, propriété
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103243
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 259701daaad1027d06bf4c28c52084dae0b062b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516960"
---
# <a name="floatcolumnvaluesize-property"></a><span data-ttu-id="ae2f2-103">FloatColumnValue. Size, propriété</span><span class="sxs-lookup"><span data-stu-id="ae2f2-103">FloatColumnValue.Size property</span></span>

<span data-ttu-id="ae2f2-104">Obtient la taille de la valeur dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="ae2f2-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="ae2f2-105">La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</span><span class="sxs-lookup"><span data-stu-id="ae2f2-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="ae2f2-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae2f2-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae2f2-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="ae2f2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ae2f2-109">Property value</span></span>

<span data-ttu-id="ae2f2-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ae2f2-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ae2f2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae2f2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae2f2-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ae2f2-112">Reference</span></span>

[<span data-ttu-id="ae2f2-113">FloatColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="ae2f2-113">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="ae2f2-114">Membres FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="ae2f2-114">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="ae2f2-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ae2f2-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
