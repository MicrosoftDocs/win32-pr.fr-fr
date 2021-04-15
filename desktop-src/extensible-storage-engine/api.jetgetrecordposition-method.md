---
description: 'En savoir plus sur : méthode API. JetGetRecordPosition'
title: API. JetGetRecordPosition, méthode
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525606"
---
# <a name="apijetgetrecordposition-method"></a><span data-ttu-id="b12f2-103">API. JetGetRecordPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="b12f2-103">Api.JetGetRecordPosition method</span></span>

<span data-ttu-id="b12f2-104">Retourne la position fractionnaire de l’enregistrement actif dans l’index actuel sous la forme d’une structure [JET_RECPOS](./jet-recpos-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b12f2-104">Returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-class.md) structure.</span></span> <span data-ttu-id="b12f2-105">Voir aussi [JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="b12f2-105">Also see [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span></span>

<span data-ttu-id="b12f2-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b12f2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b12f2-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b12f2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b12f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b12f2-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="b12f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b12f2-109">Parameters</span></span>

  - <span data-ttu-id="b12f2-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b12f2-110">sesid</span></span>  
    <span data-ttu-id="b12f2-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b12f2-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b12f2-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b12f2-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b12f2-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b12f2-113">tableid</span></span>  
    <span data-ttu-id="b12f2-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b12f2-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b12f2-115">Curseur positionné sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b12f2-115">The cursor positioned on the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="b12f2-116">recpos</span><span class="sxs-lookup"><span data-stu-id="b12f2-116">recpos</span></span>  
    <span data-ttu-id="b12f2-117">Type : [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="b12f2-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="b12f2-118">Retourne la position fractionnaire approximative de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b12f2-118">Returns the approximate fractional position of the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="b12f2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b12f2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b12f2-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b12f2-120">Reference</span></span>

[<span data-ttu-id="b12f2-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b12f2-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b12f2-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b12f2-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b12f2-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b12f2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
