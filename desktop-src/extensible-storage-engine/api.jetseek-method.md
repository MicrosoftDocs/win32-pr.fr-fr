---
description: 'En savoir plus sur : méthode API. JetSeek'
title: API. JetSeek, méthode
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953039"
---
# <a name="apijetseek-method"></a><span data-ttu-id="c4b71-103">API. JetSeek, méthode</span><span class="sxs-lookup"><span data-stu-id="c4b71-103">Api.JetSeek method</span></span>

<span data-ttu-id="c4b71-104">Positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c4b71-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="c4b71-105">Une clé de recherche doit avoir été préalablement construite à l’aide de [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="c4b71-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="c4b71-106">Consultez également [TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span><span class="sxs-lookup"><span data-stu-id="c4b71-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="c4b71-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4b71-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4b71-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c4b71-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b71-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4b71-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c4b71-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4b71-110">Parameters</span></span>

  - <span data-ttu-id="c4b71-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c4b71-111">sesid</span></span>  
    <span data-ttu-id="c4b71-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4b71-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c4b71-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c4b71-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4b71-114">TableID</span><span class="sxs-lookup"><span data-stu-id="c4b71-114">tableid</span></span>  
    <span data-ttu-id="c4b71-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4b71-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c4b71-116">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="c4b71-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4b71-117">grbit</span><span class="sxs-lookup"><span data-stu-id="c4b71-117">grbit</span></span>  
    <span data-ttu-id="c4b71-118">Type : [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c4b71-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c4b71-119">Options de recherche.</span><span class="sxs-lookup"><span data-stu-id="c4b71-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c4b71-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4b71-120">Return value</span></span>

<span data-ttu-id="c4b71-121">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c4b71-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="c4b71-122">AVERTISSEMENT ESENT.</span><span class="sxs-lookup"><span data-stu-id="c4b71-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c4b71-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4b71-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4b71-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c4b71-124">Reference</span></span>

[<span data-ttu-id="c4b71-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="c4b71-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c4b71-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="c4b71-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c4b71-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c4b71-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
