---
description: 'En savoir plus sur : propriété JET_RECORDLIST. TableID'
title: JET_RECORDLIST. TableId, propriété
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103838
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_tableid
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9140bc662592f20c2c54606666ab76099326fd56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530694"
---
# <a name="jet_recordlisttableid-property"></a><span data-ttu-id="9843b-103">JET_RECORDLIST. TableId, propriété</span><span class="sxs-lookup"><span data-stu-id="9843b-103">JET_RECORDLIST.tableid property</span></span>

<span data-ttu-id="9843b-104">Obtient l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9843b-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="9843b-105">Elle doit être fermée lorsque la table n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9843b-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="9843b-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9843b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9843b-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9843b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9843b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9843b-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="9843b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9843b-109">Property value</span></span>

<span data-ttu-id="9843b-110">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9843b-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9843b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9843b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9843b-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9843b-112">Reference</span></span>

[<span data-ttu-id="9843b-113">Classe JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="9843b-113">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="9843b-114">Membres JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="9843b-114">JET_RECORDLIST members</span></span>](./jet-recordlist-members.md)

[<span data-ttu-id="9843b-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9843b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
