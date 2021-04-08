---
description: 'En savoir plus sur : propriété JET_ENUMCOLUMNID. rgtagSequence'
title: JET_ENUMCOLUMNID. rgtagSequence, propriété
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749860"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="e59d3-103">JET_ENUMCOLUMNID. rgtagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="e59d3-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="e59d3-104">Obtient ou définit le tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée.</span><span class="sxs-lookup"><span data-stu-id="e59d3-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="e59d3-105">Un élément unique est un itagSequence qui est défini dans JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="e59d3-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="e59d3-106">Un itagSequence de 0 (zéro) signifie « Skip ».</span><span class="sxs-lookup"><span data-stu-id="e59d3-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="e59d3-107">Un itagSequence de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e59d3-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="e59d3-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e59d3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e59d3-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e59d3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e59d3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e59d3-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e59d3-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e59d3-111">Property value</span></span>

<span data-ttu-id="e59d3-112">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="e59d3-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e59d3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e59d3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e59d3-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e59d3-114">Reference</span></span>

[<span data-ttu-id="e59d3-115">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e59d3-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="e59d3-116">Membres JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e59d3-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="e59d3-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e59d3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
