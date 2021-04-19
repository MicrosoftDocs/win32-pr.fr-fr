---
description: 'En savoir plus sur : méthode API. JetDefragment'
title: API. JetDefragment, méthode
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514406"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="635c7-103">API. JetDefragment, méthode</span><span class="sxs-lookup"><span data-stu-id="635c7-103">Api.JetDefragment method</span></span>

<span data-ttu-id="635c7-104">Démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="635c7-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="635c7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="635c7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="635c7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="635c7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="635c7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="635c7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="635c7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="635c7-108">Parameters</span></span>

  - <span data-ttu-id="635c7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="635c7-109">sesid</span></span>  
    <span data-ttu-id="635c7-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="635c7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="635c7-111">Session à utiliser pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="635c7-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="635c7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="635c7-112">dbid</span></span>  
    <span data-ttu-id="635c7-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="635c7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="635c7-114">Base de données à défragmenter.</span><span class="sxs-lookup"><span data-stu-id="635c7-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="635c7-115">tableName</span><span class="sxs-lookup"><span data-stu-id="635c7-115">tableName</span></span>  
    <span data-ttu-id="635c7-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="635c7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="635c7-117">Paramètre inutilisé.</span><span class="sxs-lookup"><span data-stu-id="635c7-117">Unused parameter.</span></span> <span data-ttu-id="635c7-118">La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="635c7-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="635c7-119">mettent</span><span class="sxs-lookup"><span data-stu-id="635c7-119">passes</span></span>  
    <span data-ttu-id="635c7-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="635c7-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="635c7-121">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit le nombre maximal de passes de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="635c7-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="635c7-122">Lors de l’arrêt d’une tâche de défragmentation en ligne, ce paramètre est défini sur le nombre de passes effectuées.</span><span class="sxs-lookup"><span data-stu-id="635c7-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="635c7-123">secondes</span><span class="sxs-lookup"><span data-stu-id="635c7-123">seconds</span></span>  
    <span data-ttu-id="635c7-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="635c7-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="635c7-125">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit la durée maximale de la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="635c7-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="635c7-126">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie est définie sur la durée utilisée pour la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="635c7-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="635c7-127">grbit</span><span class="sxs-lookup"><span data-stu-id="635c7-127">grbit</span></span>  
    <span data-ttu-id="635c7-128">Type : [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="635c7-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="635c7-129">Options de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="635c7-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="635c7-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="635c7-130">Return value</span></span>

<span data-ttu-id="635c7-131">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="635c7-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="635c7-132">Code d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="635c7-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="635c7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="635c7-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="635c7-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="635c7-134">Reference</span></span>

[<span data-ttu-id="635c7-135">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="635c7-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="635c7-136">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="635c7-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="635c7-137">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="635c7-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
