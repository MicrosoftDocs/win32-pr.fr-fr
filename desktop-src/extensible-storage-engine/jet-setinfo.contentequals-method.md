---
description: 'En savoir plus sur : JET_SETINFO. Méthode ContentEquals'
title: JET_SETINFO. Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e2e13ead56594c27eee6d269783c01f5b495ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033893"
---
# <a name="jet_setinfocontentequals-method"></a><span data-ttu-id="e108c-103">JET_SETINFO. Méthode ContentEquals</span><span class="sxs-lookup"><span data-stu-id="e108c-103">JET_SETINFO.ContentEquals method</span></span>

<span data-ttu-id="e108c-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="e108c-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="e108c-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e108c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e108c-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e108c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e108c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e108c-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETINFO _
) As Boolean
'Usage
Dim instance As JET_SETINFO
Dim other As JET_SETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETINFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="e108c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e108c-108">Parameters</span></span>

  - <span data-ttu-id="e108c-109">autre</span><span class="sxs-lookup"><span data-stu-id="e108c-109">other</span></span>  
    <span data-ttu-id="e108c-110">Type : [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e108c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="e108c-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="e108c-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e108c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e108c-112">Return value</span></span>

<span data-ttu-id="e108c-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e108c-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e108c-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="e108c-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="e108c-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="e108c-115">Implements</span></span>

[<span data-ttu-id="e108c-116">IContentEquatable \<T\> . ContentEquals (T)</span><span class="sxs-lookup"><span data-stu-id="e108c-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="e108c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e108c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e108c-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e108c-118">Reference</span></span>

[<span data-ttu-id="e108c-119">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e108c-119">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="e108c-120">Membres JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e108c-120">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="e108c-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e108c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
