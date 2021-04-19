---
description: 'En savoir plus sur : méthode API. JetDefragment2'
title: API. JetDefragment2, méthode
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513197"
---
# <a name="apijetdefragment2-method"></a><span data-ttu-id="1dc56-103">API. JetDefragment2, méthode</span><span class="sxs-lookup"><span data-stu-id="1dc56-103">Api.JetDefragment2 method</span></span>

<span data-ttu-id="1dc56-104">Démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="1dc56-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="1dc56-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1dc56-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1dc56-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc56-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1dc56-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1dc56-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dc56-108">Parameters</span></span>

  - <span data-ttu-id="1dc56-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1dc56-109">sesid</span></span>  
    <span data-ttu-id="1dc56-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1dc56-111">Session à utiliser pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="1dc56-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-112">dbid</span><span class="sxs-lookup"><span data-stu-id="1dc56-112">dbid</span></span>  
    <span data-ttu-id="1dc56-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1dc56-114">Base de données à défragmenter.</span><span class="sxs-lookup"><span data-stu-id="1dc56-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-115">tableName</span><span class="sxs-lookup"><span data-stu-id="1dc56-115">tableName</span></span>  
    <span data-ttu-id="1dc56-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1dc56-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1dc56-117">Paramètre inutilisé.</span><span class="sxs-lookup"><span data-stu-id="1dc56-117">Unused parameter.</span></span> <span data-ttu-id="1dc56-118">La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="1dc56-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-119">mettent</span><span class="sxs-lookup"><span data-stu-id="1dc56-119">passes</span></span>  
    <span data-ttu-id="1dc56-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1dc56-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1dc56-121">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit le nombre maximal de passes de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="1dc56-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="1dc56-122">Lors de l’arrêt d’une tâche de défragmentation en ligne, ce paramètre est défini sur le nombre de passes effectuées.</span><span class="sxs-lookup"><span data-stu-id="1dc56-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-123">secondes</span><span class="sxs-lookup"><span data-stu-id="1dc56-123">seconds</span></span>  
    <span data-ttu-id="1dc56-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1dc56-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1dc56-125">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit la durée maximale de la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="1dc56-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="1dc56-126">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie est définie sur la durée utilisée pour la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="1dc56-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-127">rappel</span><span class="sxs-lookup"><span data-stu-id="1dc56-127">callback</span></span>  
    <span data-ttu-id="1dc56-128">Type : [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-128">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="1dc56-129">Fonction de rappel utilisée par Defrag pour signaler la progression.</span><span class="sxs-lookup"><span data-stu-id="1dc56-129">Callback function that defrag uses to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dc56-130">grbit</span><span class="sxs-lookup"><span data-stu-id="1dc56-130">grbit</span></span>  
    <span data-ttu-id="1dc56-131">Type : [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-131">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1dc56-132">Options de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="1dc56-132">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1dc56-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1dc56-133">Return value</span></span>

<span data-ttu-id="1dc56-134">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1dc56-134">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="1dc56-135">Code d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="1dc56-135">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="1dc56-136">Notes</span><span class="sxs-lookup"><span data-stu-id="1dc56-136">Remarks</span></span>

<span data-ttu-id="1dc56-137">Le rappel passé à JetDefragment2 peut être exécuté de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1dc56-137">The callback passed to JetDefragment2 can be executed asynchronously.</span></span> <span data-ttu-id="1dc56-138">Le GC ne sait pas que le code non managé a une référence au rappel. il est donc important de s’assurer que le rappel n’est pas collecté.</span><span class="sxs-lookup"><span data-stu-id="1dc56-138">The GC doesn't know that the unmanaged code has a reference to the callback so it is important to make sure the callback isn't collected.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dc56-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dc56-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1dc56-140">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1dc56-140">Reference</span></span>

[<span data-ttu-id="1dc56-141">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="1dc56-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1dc56-142">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="1dc56-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1dc56-143">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1dc56-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
