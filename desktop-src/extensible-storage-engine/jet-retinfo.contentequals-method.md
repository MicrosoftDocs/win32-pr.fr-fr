---
description: 'En savoir plus sur : JET_RETINFO. Méthode ContentEquals'
title: JET_RETINFO. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103869
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bac25d8184b1dd62e8c622cbdd79df42d4996314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752492"
---
# <a name="jet_retinfocontentequals-method"></a><span data-ttu-id="2d035-103">JET_RETINFO. Méthode ContentEquals</span><span class="sxs-lookup"><span data-stu-id="2d035-103">JET_RETINFO.ContentEquals method</span></span>

<span data-ttu-id="2d035-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="2d035-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="2d035-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d035-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d035-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d035-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d035-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d035-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RETINFO _
) As Boolean
'Usage
Dim instance As JET_RETINFO
Dim other As JET_RETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RETINFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="2d035-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d035-108">Parameters</span></span>

  - <span data-ttu-id="2d035-109">autre</span><span class="sxs-lookup"><span data-stu-id="2d035-109">other</span></span>  
    <span data-ttu-id="2d035-110">Type : [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="2d035-110">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="2d035-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="2d035-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2d035-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d035-112">Return value</span></span>

<span data-ttu-id="2d035-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2d035-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2d035-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="2d035-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="2d035-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="2d035-115">Implements</span></span>

[<span data-ttu-id="2d035-116">IContentEquatable \<T\> . ContentEquals (T)</span><span class="sxs-lookup"><span data-stu-id="2d035-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="2d035-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d035-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d035-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2d035-118">Reference</span></span>

[<span data-ttu-id="2d035-119">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2d035-119">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="2d035-120">Membres JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="2d035-120">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="2d035-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2d035-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
