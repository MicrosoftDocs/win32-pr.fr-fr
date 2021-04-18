---
description: 'En savoir plus sur : méthode API. GetColumnDictionary'
title: API. GetColumnDictionary, méthode
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515960"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="eaae3-103">API. GetColumnDictionary, méthode</span><span class="sxs-lookup"><span data-stu-id="eaae3-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="eaae3-104">Crée un dictionnaire qui mappe les noms de colonnes à leurs ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="eaae3-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="eaae3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eaae3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eaae3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eaae3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eaae3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaae3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="eaae3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaae3-108">Parameters</span></span>

  - <span data-ttu-id="eaae3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="eaae3-109">sesid</span></span>  
    <span data-ttu-id="eaae3-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eaae3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="eaae3-111">Sesid à utiliser.</span><span class="sxs-lookup"><span data-stu-id="eaae3-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="eaae3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="eaae3-112">tableid</span></span>  
    <span data-ttu-id="eaae3-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="eaae3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="eaae3-114">Table pour laquelle récupérer les informations.</span><span class="sxs-lookup"><span data-stu-id="eaae3-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eaae3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eaae3-115">Return value</span></span>

<span data-ttu-id="eaae3-116">Type : [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="eaae3-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="eaae3-117">Un dictionnaire qui mappe des noms de colonnes à des ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="eaae3-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eaae3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaae3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eaae3-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="eaae3-119">Reference</span></span>

[<span data-ttu-id="eaae3-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="eaae3-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="eaae3-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="eaae3-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="eaae3-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eaae3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
