---
description: 'En savoir plus sur : méthode API. JetEnumerateColumns'
title: API. JetEnumerateColumns, méthode
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033914"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="e11ae-103">API. JetEnumerateColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="e11ae-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="e11ae-104">Récupère efficacement un ensemble de colonnes et leurs valeurs à partir de l’enregistrement actuel d’un curseur ou de la mémoire tampon de copie de ce curseur.</span><span class="sxs-lookup"><span data-stu-id="e11ae-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="e11ae-105">Les colonnes et les valeurs récupérées peuvent être restreintes par une liste d’ID de colonne, de nombres itagSequence et d’autres caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="e11ae-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="e11ae-106">Cette API de récupération de colonne est unique dans la mesure où elle retourne des informations dans la mémoire allouée dynamiquement obtenue à l’aide d’un rappel compatible réalloué fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e11ae-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="e11ae-107">Cette nouvelle flexibilité permet une récupération efficace des données de colonne avec des caractéristiques spécifiques (telles que la taille et la multiplicité) qui sont inconnues pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e11ae-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="e11ae-108">Cela élimine le besoin d’utiliser les modes de découverte de JetRetrieveColumn pour déterminer ces caractéristiques afin de configurer un dernier appel à JetRetrieveColumn qui récupérera correctement les données souhaitées.</span><span class="sxs-lookup"><span data-stu-id="e11ae-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="e11ae-109">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="e11ae-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="e11ae-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e11ae-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e11ae-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e11ae-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e11ae-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e11ae-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e11ae-113">Parameters</span></span>

  - <span data-ttu-id="e11ae-114">sesid</span><span class="sxs-lookup"><span data-stu-id="e11ae-114">sesid</span></span>  
    <span data-ttu-id="e11ae-115">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e11ae-116">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e11ae-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-117">TableID</span><span class="sxs-lookup"><span data-stu-id="e11ae-117">tableid</span></span>  
    <span data-ttu-id="e11ae-118">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e11ae-119">Curseur à partir duquel récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="e11ae-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-120">numColumnids</span><span class="sxs-lookup"><span data-stu-id="e11ae-120">numColumnids</span></span>  
    <span data-ttu-id="e11ae-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e11ae-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e11ae-122">Nombre de JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="e11ae-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-123">columnids</span><span class="sxs-lookup"><span data-stu-id="e11ae-123">columnids</span></span>  
    <span data-ttu-id="e11ae-124">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="e11ae-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="e11ae-125">Tableau facultatif d’ID de colonne, chacun avec un tableau facultatif de nombres itagSequence à énumérer.</span><span class="sxs-lookup"><span data-stu-id="e11ae-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-126">numColumnValues</span><span class="sxs-lookup"><span data-stu-id="e11ae-126">numColumnValues</span></span>  
    <span data-ttu-id="e11ae-127">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e11ae-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e11ae-128">Retourne le nombre de valeurs de colonne récupérées.</span><span class="sxs-lookup"><span data-stu-id="e11ae-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-129">columnValues</span><span class="sxs-lookup"><span data-stu-id="e11ae-129">columnValues</span></span>  
    <span data-ttu-id="e11ae-130">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="e11ae-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="e11ae-131">Retourne les valeurs de la colonne énumérée.</span><span class="sxs-lookup"><span data-stu-id="e11ae-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-132">allocator</span><span class="sxs-lookup"><span data-stu-id="e11ae-132">allocator</span></span>  
    <span data-ttu-id="e11ae-133">Type : [Microsoft.ISAM.esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="e11ae-134">Rappel utilisé pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e11ae-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-135">allocatorContext</span><span class="sxs-lookup"><span data-stu-id="e11ae-135">allocatorContext</span></span>  
    <span data-ttu-id="e11ae-136">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e11ae-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e11ae-137">Contexte du rappel d’allocation.</span><span class="sxs-lookup"><span data-stu-id="e11ae-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-138">maxDataSize</span><span class="sxs-lookup"><span data-stu-id="e11ae-138">maxDataSize</span></span>  
    <span data-ttu-id="e11ae-139">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e11ae-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e11ae-140">Définit une limite sur la quantité de données à retourner à partir d’une colonne de texte long ou d’une colonne binaire longue.</span><span class="sxs-lookup"><span data-stu-id="e11ae-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="e11ae-141">Ce paramètre peut être utilisé pour empêcher l’énumération d’une valeur de colonne extrêmement volumineuse.</span><span class="sxs-lookup"><span data-stu-id="e11ae-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="e11ae-142">grbit</span><span class="sxs-lookup"><span data-stu-id="e11ae-142">grbit</span></span>  
    <span data-ttu-id="e11ae-143">Type : [Microsoft. ISAM. esent. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e11ae-144">Récupérez les options.</span><span class="sxs-lookup"><span data-stu-id="e11ae-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e11ae-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e11ae-145">Return value</span></span>

<span data-ttu-id="e11ae-146">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e11ae-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e11ae-147">Avertissement ou réussite.</span><span class="sxs-lookup"><span data-stu-id="e11ae-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e11ae-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e11ae-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e11ae-149">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e11ae-149">Reference</span></span>

[<span data-ttu-id="e11ae-150">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e11ae-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e11ae-151">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e11ae-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e11ae-152">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e11ae-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
