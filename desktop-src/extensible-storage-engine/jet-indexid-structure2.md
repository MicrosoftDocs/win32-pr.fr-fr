---
description: 'En savoir plus sur : structure JET_INDEXID'
title: Structure JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536865"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="0e15d-103">Structure JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0e15d-103">JET_INDEXID structure</span></span>

<span data-ttu-id="0e15d-104">Contient un ID d’index.</span><span class="sxs-lookup"><span data-stu-id="0e15d-104">Holds an index ID.</span></span> <span data-ttu-id="0e15d-105">Un ID d’index est un indicateur utilisé pour accélérer la sélection de l’index actuel à l’aide de JetSetCurrentIndex.</span><span class="sxs-lookup"><span data-stu-id="0e15d-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="0e15d-106">Elle est particulièrement utile lorsqu’il existe un très grand nombre d’index sur une table.</span><span class="sxs-lookup"><span data-stu-id="0e15d-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="0e15d-107">L’ID d’index peut être récupéré à l’aide de JetGetIndexInfo ou JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="0e15d-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="0e15d-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e15d-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e15d-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e15d-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e15d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e15d-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="0e15d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0e15d-111">Remarks</span></span>

<span data-ttu-id="0e15d-112">L’attribut Pack est nécessaire, car la version C++ est définie en tant que tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="0e15d-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="0e15d-113">Si le \# compilateur C insère le remplissage habituel entre le cbStruct uint et le IntPtr, la structure finit par être trop grande.</span><span class="sxs-lookup"><span data-stu-id="0e15d-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="0e15d-114">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="0e15d-114">Thread safety</span></span>

<span data-ttu-id="0e15d-115">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0e15d-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0e15d-116">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0e15d-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e15d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e15d-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e15d-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0e15d-118">Reference</span></span>

[<span data-ttu-id="0e15d-119">Membres JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0e15d-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="0e15d-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0e15d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
