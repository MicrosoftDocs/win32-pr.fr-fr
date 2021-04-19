---
description: 'En savoir plus sur : propriété JET_DBINFOMISC. bkinfoDiffPrev'
title: JET_DBINFOMISC. bkinfoDiffPrev, propriété
TOCTitle: 'bkinfoDiffPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfodiffprev(v=EXCHG.10)
ms:contentKeyID: 39513441
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoDiffPrev
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd152d1dffbc4cf956129dfd886186dda0b33084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516455"
---
# <a name="jet_dbinfomiscbkinfodiffprev-property"></a><span data-ttu-id="e01c7-103">JET_DBINFOMISC. bkinfoDiffPrev, propriété</span><span class="sxs-lookup"><span data-stu-id="e01c7-103">JET_DBINFOMISC.bkinfoDiffPrev property</span></span>

<span data-ttu-id="e01c7-104">Obtient des informations sur la dernière sauvegarde différentielle réussie.</span><span class="sxs-lookup"><span data-stu-id="e01c7-104">Gets information about the last successful differential backup.</span></span> <span data-ttu-id="e01c7-105">Réinitialisez lorsque [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="e01c7-105">Reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="e01c7-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e01c7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e01c7-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e01c7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e01c7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e01c7-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoDiffPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoDiffPrev
```

``` csharp
public JET_BKINFO bkinfoDiffPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="e01c7-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e01c7-109">Property value</span></span>

<span data-ttu-id="e01c7-110">Type : [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e01c7-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e01c7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e01c7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e01c7-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e01c7-112">Reference</span></span>

[<span data-ttu-id="e01c7-113">Classe JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="e01c7-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="e01c7-114">Membres JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="e01c7-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="e01c7-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e01c7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
