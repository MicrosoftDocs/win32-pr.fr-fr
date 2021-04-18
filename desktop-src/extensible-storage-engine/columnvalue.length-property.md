---
description: 'En savoir plus sur : propriété ColumnValue. Length'
title: ColumnValue. Length, propriété
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520195"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="36b9a-103">ColumnValue. Length, propriété</span><span class="sxs-lookup"><span data-stu-id="36b9a-103">ColumnValue.Length property</span></span>

<span data-ttu-id="36b9a-104">Obtient la longueur d’octet d’une valeur de colonne, qui est égale à zéro si la colonne est null, sinon elle correspond à la taille des colonnes de taille fixe et représente la longueur réelle en octets pour les colonnes de taille variable (c’est-à-dire binaire et chaîne).</span><span class="sxs-lookup"><span data-stu-id="36b9a-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="36b9a-105">Pour les chaînes, la longueur est déterminée en supposant deux octets par caractère.</span><span class="sxs-lookup"><span data-stu-id="36b9a-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="36b9a-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36b9a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36b9a-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36b9a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36b9a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36b9a-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="36b9a-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="36b9a-109">Property value</span></span>

<span data-ttu-id="36b9a-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="36b9a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="36b9a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36b9a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36b9a-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="36b9a-112">Reference</span></span>

[<span data-ttu-id="36b9a-113">ColumnValue, classe</span><span class="sxs-lookup"><span data-stu-id="36b9a-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="36b9a-114">Membres ColumnValue</span><span class="sxs-lookup"><span data-stu-id="36b9a-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="36b9a-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36b9a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
