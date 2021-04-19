---
description: 'En savoir plus sur : JET_INDEXCREATE. Méthode ContentEquals'
title: JET_INDEXCREATE. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_INDEXCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103543
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5c61d37cde77137d465aac6791e81a7e5d594e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536781"
---
# <a name="jet_indexcreatecontentequals-method"></a><span data-ttu-id="aabb7-103">JET_INDEXCREATE. Méthode ContentEquals</span><span class="sxs-lookup"><span data-stu-id="aabb7-103">JET_INDEXCREATE.ContentEquals method</span></span>

<span data-ttu-id="aabb7-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="aabb7-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="aabb7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aabb7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aabb7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aabb7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aabb7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aabb7-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_INDEXCREATE _
) As Boolean
'Usage
Dim instance As JET_INDEXCREATE
Dim other As JET_INDEXCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_INDEXCREATE other
)
```

#### <a name="parameters"></a><span data-ttu-id="aabb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aabb7-108">Parameters</span></span>

  - <span data-ttu-id="aabb7-109">autre</span><span class="sxs-lookup"><span data-stu-id="aabb7-109">other</span></span>  
    <span data-ttu-id="aabb7-110">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXCREATE](./jet-indexcreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="aabb7-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXCREATE](./jet-indexcreate-class.md)</span></span>  
    
    <span data-ttu-id="aabb7-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="aabb7-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aabb7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aabb7-112">Return value</span></span>

<span data-ttu-id="aabb7-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="aabb7-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="aabb7-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="aabb7-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="aabb7-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="aabb7-115">Implements</span></span>

[<span data-ttu-id="aabb7-116">IContentEquatable \<T\> . ContentEquals (T)</span><span class="sxs-lookup"><span data-stu-id="aabb7-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="aabb7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aabb7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aabb7-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="aabb7-118">Reference</span></span>

[<span data-ttu-id="aabb7-119">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="aabb7-119">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="aabb7-120">Membres JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="aabb7-120">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="aabb7-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aabb7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
