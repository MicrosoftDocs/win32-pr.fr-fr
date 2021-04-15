---
description: 'En savoir plus sur : propriété JET_RECSIZE. cbLongValueDataCompressed'
title: JET_RECSIZE. cbLongValueDataCompressed, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113bb741287e85ef6f7132cd299202a0b9c2af31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393384"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a><span data-ttu-id="16a49-103">JET_RECSIZE. cbLongValueDataCompressed, propriété</span><span class="sxs-lookup"><span data-stu-id="16a49-103">JET_RECSIZE.cbLongValueDataCompressed property</span></span>

<span data-ttu-id="16a49-104">Obtient la taille compressée des données utilisateur dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="16a49-104">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="16a49-105">C’est le même que [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) si aucune valeur long séparée n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="16a49-105">This is the same as [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) if no separated long values are compressed.</span></span>

<span data-ttu-id="16a49-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16a49-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="16a49-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16a49-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16a49-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16a49-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="16a49-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="16a49-109">Property value</span></span>

<span data-ttu-id="16a49-110">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="16a49-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="16a49-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a49-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16a49-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="16a49-112">Reference</span></span>

[<span data-ttu-id="16a49-113">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="16a49-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="16a49-114">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="16a49-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="16a49-115">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="16a49-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
