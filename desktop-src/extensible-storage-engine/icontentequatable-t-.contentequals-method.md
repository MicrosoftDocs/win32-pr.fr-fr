---
description: 'En savoir plus sur : IContentEquatable <T> . Méthode ContentEquals'
title: IContentEquatable (T). Méthode ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3b06307f7c4ebc44242e02ee5ae99a182f9ab3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536345"
---
# <a name="icontentequatabletcontentequals-method"></a><span data-ttu-id="8479c-103">IContentEquatable \<T\> . Méthode ContentEquals</span><span class="sxs-lookup"><span data-stu-id="8479c-103">IContentEquatable\<T\>.ContentEquals method</span></span>

<span data-ttu-id="8479c-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="8479c-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="8479c-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8479c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8479c-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8479c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8479c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8479c-107">Syntax</span></span>

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a><span data-ttu-id="8479c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8479c-108">Parameters</span></span>

  - <span data-ttu-id="8479c-109">autre</span><span class="sxs-lookup"><span data-stu-id="8479c-109">other</span></span>  
    <span data-ttu-id="8479c-110">Type : [T](./icontentequatable-t-interface.md)</span><span class="sxs-lookup"><span data-stu-id="8479c-110">Type: [T](./icontentequatable-t-interface.md)</span></span>  
    
    <span data-ttu-id="8479c-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="8479c-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8479c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8479c-112">Return value</span></span>

<span data-ttu-id="8479c-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8479c-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="8479c-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="8479c-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8479c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8479c-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8479c-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8479c-116">Reference</span></span>

[<span data-ttu-id="8479c-117">\<T\>Interface IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="8479c-117">IContentEquatable\<T\> interface</span></span>](./icontentequatable-t-interface.md)

[<span data-ttu-id="8479c-118">\<T\>Membres IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="8479c-118">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="8479c-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8479c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
