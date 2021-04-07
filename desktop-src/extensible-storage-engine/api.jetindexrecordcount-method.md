---
description: 'En savoir plus sur : méthode API. JetIndexRecordCount'
title: API. JetIndexRecordCount, méthode
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759429"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="44c0b-103">API. JetIndexRecordCount, méthode</span><span class="sxs-lookup"><span data-stu-id="44c0b-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="44c0b-104">Compte le nombre d’entrées dans l’index actuel à partir de la position actuelle vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="44c0b-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="44c0b-105">La position actuelle est incluse dans le nombre.</span><span class="sxs-lookup"><span data-stu-id="44c0b-105">The current position is included in the count.</span></span> <span data-ttu-id="44c0b-106">Le nombre peut être supérieur au nombre total d’enregistrements dans la table si l’index actuel est sur une colonne à valeurs multiples et que les instances de la colonne ont des valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="44c0b-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="44c0b-107">Si la table est vide, la valeur 0 est retournée pour le nombre.</span><span class="sxs-lookup"><span data-stu-id="44c0b-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="44c0b-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44c0b-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44c0b-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44c0b-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44c0b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c0b-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="44c0b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44c0b-111">Parameters</span></span>

  - <span data-ttu-id="44c0b-112">sesid</span><span class="sxs-lookup"><span data-stu-id="44c0b-112">sesid</span></span>  
    <span data-ttu-id="44c0b-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44c0b-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="44c0b-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="44c0b-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="44c0b-115">TableID</span><span class="sxs-lookup"><span data-stu-id="44c0b-115">tableid</span></span>  
    <span data-ttu-id="44c0b-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44c0b-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="44c0b-117">Curseur dans lequel compter les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="44c0b-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="44c0b-118">numRecords</span><span class="sxs-lookup"><span data-stu-id="44c0b-118">numRecords</span></span>  
    <span data-ttu-id="44c0b-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="44c0b-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="44c0b-120">Retourne le nombre d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="44c0b-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="44c0b-121">maxRecordsToCount</span><span class="sxs-lookup"><span data-stu-id="44c0b-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="44c0b-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="44c0b-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="44c0b-123">Nombre maximal d’enregistrements à compter.</span><span class="sxs-lookup"><span data-stu-id="44c0b-123">The maximum number of records to count.</span></span> <span data-ttu-id="44c0b-124">La valeur 0 indique que le nombre est illimité.</span><span class="sxs-lookup"><span data-stu-id="44c0b-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="44c0b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c0b-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44c0b-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="44c0b-126">Reference</span></span>

[<span data-ttu-id="44c0b-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="44c0b-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="44c0b-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="44c0b-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="44c0b-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="44c0b-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
