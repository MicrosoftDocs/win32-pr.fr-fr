---
description: 'En savoir plus sur : méthode API. JetResetTableSequential'
title: API. JetResetTableSequential, méthode
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210522"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="badd6-103">API. JetResetTableSequential, méthode</span><span class="sxs-lookup"><span data-stu-id="badd6-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="badd6-104">Notifie le moteur de base de données que l’application n’analyse plus la totalité de l’index sur lequel le curseur est positionné.</span><span class="sxs-lookup"><span data-stu-id="badd6-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="badd6-105">Cet appel inverse une notification envoyée par [JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="badd6-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="badd6-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="badd6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="badd6-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="badd6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="badd6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="badd6-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="badd6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="badd6-109">Parameters</span></span>

  - <span data-ttu-id="badd6-110">sesid</span><span class="sxs-lookup"><span data-stu-id="badd6-110">sesid</span></span>  
    <span data-ttu-id="badd6-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="badd6-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="badd6-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="badd6-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="badd6-113">TableID</span><span class="sxs-lookup"><span data-stu-id="badd6-113">tableid</span></span>  
    <span data-ttu-id="badd6-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="badd6-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="badd6-115">Curseur qui a accès aux données.</span><span class="sxs-lookup"><span data-stu-id="badd6-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="badd6-116">grbit</span><span class="sxs-lookup"><span data-stu-id="badd6-116">grbit</span></span>  
    <span data-ttu-id="badd6-117">Type : [Microsoft. ISAM. esent. Interop. ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="badd6-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="badd6-118">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="badd6-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="badd6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="badd6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="badd6-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="badd6-120">Reference</span></span>

[<span data-ttu-id="badd6-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="badd6-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="badd6-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="badd6-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="badd6-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="badd6-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
