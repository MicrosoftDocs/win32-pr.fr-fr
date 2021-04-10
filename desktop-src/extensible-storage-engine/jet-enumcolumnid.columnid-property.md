---
description: 'En savoir plus sur : propriété JET_ENUMCOLUMNID. ColumnId'
title: JET_ENUMCOLUMNID. ColumnId, propriété
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112099"
---
# <a name="jet_enumcolumnidcolumnid-property"></a><span data-ttu-id="1a43e-103">JET_ENUMCOLUMNID. ColumnId, propriété</span><span class="sxs-lookup"><span data-stu-id="1a43e-103">JET_ENUMCOLUMNID.columnid property</span></span>

<span data-ttu-id="1a43e-104">Obtient ou définit l’ID ColumnID à énumérer.</span><span class="sxs-lookup"><span data-stu-id="1a43e-104">Gets or sets the columnid ID to enumerate.</span></span>

<span data-ttu-id="1a43e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a43e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a43e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a43e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a43e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a43e-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1a43e-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1a43e-108">Property value</span></span>

<span data-ttu-id="1a43e-109">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a43e-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="remarks"></a><span data-ttu-id="1a43e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1a43e-110">Remarks</span></span>

<span data-ttu-id="1a43e-111">Si l’ID de colonne est 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans le tableau de sortie des structures de JET_ENUMCOLUMN est généré avec un état de colonne de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="1a43e-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of JET_ENUMCOLUMN structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a43e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a43e-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a43e-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1a43e-113">Reference</span></span>

[<span data-ttu-id="1a43e-114">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="1a43e-114">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="1a43e-115">Membres JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="1a43e-115">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="1a43e-116">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a43e-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
