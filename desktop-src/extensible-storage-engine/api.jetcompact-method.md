---
description: 'En savoir plus sur : méthode API. JetCompact'
title: API. JetCompact, méthode
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951058"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="d24e2-103">API. JetCompact, méthode</span><span class="sxs-lookup"><span data-stu-id="d24e2-103">Api.JetCompact method</span></span>

<span data-ttu-id="d24e2-104">Effectue une copie d’une base de données existante.</span><span class="sxs-lookup"><span data-stu-id="d24e2-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="d24e2-105">La copie est compactée dans un état optimal pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d24e2-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="d24e2-106">Les données dans les données copiées seront empaquetées en fonction des mesures choisies pour les index lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="d24e2-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="d24e2-107">De cette façon, les données compactées peuvent être stockées aussi denses que possible.</span><span class="sxs-lookup"><span data-stu-id="d24e2-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="d24e2-108">Les données compactées peuvent également réserver de l’espace pour la croissance des enregistrements ou les insertions d’index suivantes.</span><span class="sxs-lookup"><span data-stu-id="d24e2-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="d24e2-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d24e2-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d24e2-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d24e2-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d24e2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d24e2-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d24e2-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d24e2-112">Parameters</span></span>

  - <span data-ttu-id="d24e2-113">sesid</span><span class="sxs-lookup"><span data-stu-id="d24e2-113">sesid</span></span>  
    <span data-ttu-id="d24e2-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d24e2-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d24e2-115">Session à utiliser pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="d24e2-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="d24e2-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="d24e2-116">sourceDatabase</span></span>  
    <span data-ttu-id="d24e2-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d24e2-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d24e2-118">Base de données source qui sera compactée.</span><span class="sxs-lookup"><span data-stu-id="d24e2-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="d24e2-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="d24e2-119">destinationDatabase</span></span>  
    <span data-ttu-id="d24e2-120">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d24e2-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d24e2-121">Nom à utiliser pour la base de données compactée.</span><span class="sxs-lookup"><span data-stu-id="d24e2-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="d24e2-122">statusCallback</span><span class="sxs-lookup"><span data-stu-id="d24e2-122">statusCallback</span></span>  
    <span data-ttu-id="d24e2-123">Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="d24e2-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="d24e2-124">Fonction de rappel qui peut être appelée régulièrement via l’opération de compactage de la base de données pour signaler la progression.</span><span class="sxs-lookup"><span data-stu-id="d24e2-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="d24e2-125">ignoré</span><span class="sxs-lookup"><span data-stu-id="d24e2-125">ignored</span></span>  
    <span data-ttu-id="d24e2-126">Type : [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="d24e2-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="d24e2-127">Ce paramètre est ignoré et doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="d24e2-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="d24e2-128">grbit</span><span class="sxs-lookup"><span data-stu-id="d24e2-128">grbit</span></span>  
    <span data-ttu-id="d24e2-129">Type : [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d24e2-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d24e2-130">Options de compactage.</span><span class="sxs-lookup"><span data-stu-id="d24e2-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="d24e2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d24e2-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d24e2-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d24e2-132">Reference</span></span>

[<span data-ttu-id="d24e2-133">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d24e2-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d24e2-134">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d24e2-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d24e2-135">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d24e2-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
