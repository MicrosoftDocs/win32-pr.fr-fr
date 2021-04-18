---
description: 'En savoir plus sur : propriété JET_SETCOLUMN. itagSequence'
title: JET_SETCOLUMN. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7870f6e29cf8f6810c6aa41049868fbceb370dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519267"
---
# <a name="jet_setcolumnitagsequence-property"></a><span data-ttu-id="533c9-103">JET_SETCOLUMN. itagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="533c9-103">JET_SETCOLUMN.itagSequence property</span></span>

<span data-ttu-id="533c9-104">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir.</span><span class="sxs-lookup"><span data-stu-id="533c9-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="533c9-105">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="533c9-105">The array of values is one-based.</span></span> <span data-ttu-id="533c9-106">La première valeur est Sequence 1, et non 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="533c9-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="533c9-107">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme itagSequence si cette valeur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="533c9-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="533c9-108">La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="533c9-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="533c9-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="533c9-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="533c9-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="533c9-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="533c9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="533c9-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="533c9-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="533c9-112">Property value</span></span>

<span data-ttu-id="533c9-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="533c9-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="533c9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="533c9-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="533c9-115">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="533c9-115">Reference</span></span>

[<span data-ttu-id="533c9-116">Classe JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="533c9-116">JET_SETCOLUMN class</span></span>](./jet-setcolumn-class.md)

[<span data-ttu-id="533c9-117">Membres JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="533c9-117">JET_SETCOLUMN members</span></span>](./jet-setcolumn-members.md)

[<span data-ttu-id="533c9-118">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="533c9-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
