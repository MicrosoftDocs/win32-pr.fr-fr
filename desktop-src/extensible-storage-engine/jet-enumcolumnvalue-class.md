---
description: 'En savoir plus sur : classe JET_ENUMCOLUMNVALUE'
title: Classe JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543074"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="e7a56-103">Classe JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e7a56-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="e7a56-104">Énumère les valeurs de colonne d’un enregistrement à l’aide de la fonction JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="e7a56-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="e7a56-105">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) retourne un tableau de structures de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="e7a56-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="e7a56-106">Le tableau est retourné dans la mémoire qui a été allouée à l’aide du rappel fourni à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e7a56-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e7a56-107">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="e7a56-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="e7a56-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="e7a56-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="e7a56-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e7a56-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="e7a56-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7a56-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7a56-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7a56-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a56-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7a56-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="e7a56-113">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="e7a56-113">Thread safety</span></span>

<span data-ttu-id="e7a56-114">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e7a56-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e7a56-115">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e7a56-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7a56-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a56-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7a56-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e7a56-117">Reference</span></span>

[<span data-ttu-id="e7a56-118">Membres JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e7a56-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="e7a56-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e7a56-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
