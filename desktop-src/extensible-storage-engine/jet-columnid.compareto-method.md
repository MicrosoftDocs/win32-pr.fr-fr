---
description: 'En savoir plus sur : méthode JET_COLUMNID. CompareTo'
title: JET_COLUMNID. CompareTo, méthode
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114059"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="31361-103">JET_COLUMNID. CompareTo, méthode</span><span class="sxs-lookup"><span data-stu-id="31361-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="31361-104">Compare ce ColumnID à un autre ColumnID et détermine si cette instance est antérieure, identique ou postérieure à l’autre instance.</span><span class="sxs-lookup"><span data-stu-id="31361-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="31361-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31361-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31361-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31361-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31361-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31361-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="31361-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31361-108">Parameters</span></span>

  - <span data-ttu-id="31361-109">autre</span><span class="sxs-lookup"><span data-stu-id="31361-109">other</span></span>  
    <span data-ttu-id="31361-110">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31361-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="31361-111">ColumnID à comparer à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="31361-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31361-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31361-112">Return value</span></span>

<span data-ttu-id="31361-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="31361-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="31361-114">Nombre signé indiquant les positions relatives de cette instance et du paramètre de valeur.</span><span class="sxs-lookup"><span data-stu-id="31361-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="31361-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="31361-115">Implements</span></span>

[<span data-ttu-id="31361-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="31361-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="31361-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31361-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31361-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="31361-118">Reference</span></span>

[<span data-ttu-id="31361-119">Structure JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="31361-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="31361-120">Membres JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="31361-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="31361-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="31361-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
