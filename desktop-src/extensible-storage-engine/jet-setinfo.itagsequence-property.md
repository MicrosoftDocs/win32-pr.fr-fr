---
description: 'En savoir plus sur : propriété JET_SETINFO. itagSequence'
title: JET_SETINFO. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112526"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="53aa6-103">JET_SETINFO. itagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="53aa6-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="53aa6-104">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir.</span><span class="sxs-lookup"><span data-stu-id="53aa6-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="53aa6-105">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="53aa6-105">The array of values is one-based.</span></span> <span data-ttu-id="53aa6-106">La première valeur est Sequence 1, et non 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="53aa6-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="53aa6-107">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme itagSequence si cette valeur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="53aa6-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="53aa6-108">La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="53aa6-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="53aa6-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53aa6-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53aa6-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53aa6-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53aa6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53aa6-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="53aa6-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="53aa6-112">Property value</span></span>

<span data-ttu-id="53aa6-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53aa6-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="53aa6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53aa6-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53aa6-115">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="53aa6-115">Reference</span></span>

[<span data-ttu-id="53aa6-116">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="53aa6-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="53aa6-117">Membres JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="53aa6-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="53aa6-118">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53aa6-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
