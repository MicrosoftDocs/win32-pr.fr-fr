---
description: 'En savoir plus sur : méthode API. JetSetLS'
title: API. JetSetLS, méthode
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209986"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="674b8-103">API. JetSetLS, méthode</span><span class="sxs-lookup"><span data-stu-id="674b8-103">Api.JetSetLS method</span></span>

<span data-ttu-id="674b8-104">Permet à l’application d’associer un handle de contexte appelé stockage local avec un curseur ou la table associée à ce curseur.</span><span class="sxs-lookup"><span data-stu-id="674b8-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="674b8-105">Ce descripteur de contexte peut être utilisé par l’application pour stocker les données auxiliaires associées à un curseur ou une table.</span><span class="sxs-lookup"><span data-stu-id="674b8-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="674b8-106">L’application est notifiée ultérieurement à l’aide d’un rappel d’exécution lorsque le handle de contexte doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="674b8-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="674b8-107">Cela permet d’associer l’État alloué dynamiquement à un curseur ou une table.</span><span class="sxs-lookup"><span data-stu-id="674b8-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="674b8-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="674b8-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="674b8-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="674b8-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="674b8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="674b8-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="674b8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="674b8-111">Parameters</span></span>

  - <span data-ttu-id="674b8-112">sesid</span><span class="sxs-lookup"><span data-stu-id="674b8-112">sesid</span></span>  
    <span data-ttu-id="674b8-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="674b8-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="674b8-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="674b8-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="674b8-115">TableID</span><span class="sxs-lookup"><span data-stu-id="674b8-115">tableid</span></span>  
    <span data-ttu-id="674b8-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="674b8-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="674b8-117">Curseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="674b8-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="674b8-118">ls</span><span class="sxs-lookup"><span data-stu-id="674b8-118">ls</span></span>  
    <span data-ttu-id="674b8-119">Type : [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="674b8-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="674b8-120">Handle de contexte à associer à la session ou au curseur.</span><span class="sxs-lookup"><span data-stu-id="674b8-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="674b8-121">grbit</span><span class="sxs-lookup"><span data-stu-id="674b8-121">grbit</span></span>  
    <span data-ttu-id="674b8-122">Type : [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="674b8-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="674b8-123">Définissez les options.</span><span class="sxs-lookup"><span data-stu-id="674b8-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="674b8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="674b8-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="674b8-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="674b8-125">Reference</span></span>

[<span data-ttu-id="674b8-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="674b8-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="674b8-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="674b8-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="674b8-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="674b8-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
