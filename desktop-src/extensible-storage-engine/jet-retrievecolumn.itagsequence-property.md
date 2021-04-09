---
description: 'En savoir plus sur : propriété JET_RETRIEVECOLUMN. itagSequence'
title: JET_RETRIEVECOLUMN. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103882
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f2885d5bf467d282ef97172323a8de44980ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867137"
---
# <a name="jet_retrievecolumnitagsequence-property"></a><span data-ttu-id="55e72-103">JET_RETRIEVECOLUMN. itagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="55e72-103">JET_RETRIEVECOLUMN.itagSequence property</span></span>

<span data-ttu-id="55e72-104">Obtient ou définit le numéro de séquence des valeurs contenues dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="55e72-104">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="55e72-105">Si itagSequence est égal à 0, le nombre d’instances d’une colonne à valeurs multiples est retourné à la place des données de colonne.</span><span class="sxs-lookup"><span data-stu-id="55e72-105">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span>

<span data-ttu-id="55e72-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55e72-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55e72-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55e72-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55e72-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55e72-108">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="55e72-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="55e72-109">Property value</span></span>

<span data-ttu-id="55e72-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55e72-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="55e72-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e72-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55e72-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="55e72-112">Reference</span></span>

[<span data-ttu-id="55e72-113">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="55e72-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="55e72-114">Membres JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="55e72-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="55e72-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55e72-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
