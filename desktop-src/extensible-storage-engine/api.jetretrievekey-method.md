---
description: 'En savoir plus sur : méthode API. JetRetrieveKey'
title: API. JetRetrieveKey, méthode
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526309"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="7ae27-103">API. JetRetrieveKey, méthode</span><span class="sxs-lookup"><span data-stu-id="7ae27-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="7ae27-104">Récupère la clé de l’entrée d’index à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="7ae27-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="7ae27-105">Consultez également [RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ae27-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="7ae27-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ae27-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ae27-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7ae27-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae27-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ae27-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7ae27-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae27-109">Parameters</span></span>

  - <span data-ttu-id="7ae27-110">sesid</span><span class="sxs-lookup"><span data-stu-id="7ae27-110">sesid</span></span>  
    <span data-ttu-id="7ae27-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7ae27-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7ae27-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7ae27-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae27-113">TableID</span><span class="sxs-lookup"><span data-stu-id="7ae27-113">tableid</span></span>  
    <span data-ttu-id="7ae27-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7ae27-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7ae27-115">Curseur à partir duquel récupérer la clé.</span><span class="sxs-lookup"><span data-stu-id="7ae27-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae27-116">data</span><span class="sxs-lookup"><span data-stu-id="7ae27-116">data</span></span>  
    <span data-ttu-id="7ae27-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="7ae27-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7ae27-118">Mémoire tampon dans laquelle récupérer la clé.</span><span class="sxs-lookup"><span data-stu-id="7ae27-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae27-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="7ae27-119">dataSize</span></span>  
    <span data-ttu-id="7ae27-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ae27-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7ae27-121">Taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ae27-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae27-122">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="7ae27-122">actualDataSize</span></span>  
    <span data-ttu-id="7ae27-123">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ae27-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7ae27-124">Retourne la taille réelle des données.</span><span class="sxs-lookup"><span data-stu-id="7ae27-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae27-125">grbit</span><span class="sxs-lookup"><span data-stu-id="7ae27-125">grbit</span></span>  
    <span data-ttu-id="7ae27-126">Type : [Microsoft. ISAM. esent. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7ae27-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7ae27-127">Récupérez les options de clé.</span><span class="sxs-lookup"><span data-stu-id="7ae27-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ae27-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae27-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ae27-129">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7ae27-129">Reference</span></span>

[<span data-ttu-id="7ae27-130">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7ae27-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7ae27-131">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7ae27-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7ae27-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7ae27-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
