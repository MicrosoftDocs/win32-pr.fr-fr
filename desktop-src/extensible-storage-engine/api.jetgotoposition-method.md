---
description: 'En savoir plus sur : méthode API. JetGotoPosition'
title: API. JetGotoPosition, méthode
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5917e729d1a9ae5ae0a3715d6a2a2a81f45f75e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518353"
---
# <a name="apijetgotoposition-method"></a><span data-ttu-id="cb812-103">API. JetGotoPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="cb812-103">Api.JetGotoPosition method</span></span>

<span data-ttu-id="cb812-104">Déplace un curseur vers un nouvel emplacement qui est une fraction de la façon dont l’index actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb812-104">Moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="cb812-105">Voir aussi [JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="cb812-105">Also see [JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span></span>

<span data-ttu-id="cb812-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb812-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb812-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb812-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb812-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb812-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="cb812-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb812-109">Parameters</span></span>

  - <span data-ttu-id="cb812-110">sesid</span><span class="sxs-lookup"><span data-stu-id="cb812-110">sesid</span></span>  
    <span data-ttu-id="cb812-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb812-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cb812-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cb812-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb812-113">TableID</span><span class="sxs-lookup"><span data-stu-id="cb812-113">tableid</span></span>  
    <span data-ttu-id="cb812-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb812-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cb812-115">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="cb812-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb812-116">recpos</span><span class="sxs-lookup"><span data-stu-id="cb812-116">recpos</span></span>  
    <span data-ttu-id="cb812-117">Type : [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="cb812-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="cb812-118">Position approximative à laquelle se déplacer.</span><span class="sxs-lookup"><span data-stu-id="cb812-118">The approximate position to move to.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb812-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb812-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb812-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cb812-120">Reference</span></span>

[<span data-ttu-id="cb812-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="cb812-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cb812-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="cb812-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cb812-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cb812-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
