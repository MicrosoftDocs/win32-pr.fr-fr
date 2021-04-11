---
description: 'En savoir plus sur : méthode API. JetGetLS'
title: API. JetGetLS, méthode
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201335"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="8795b-103">API. JetGetLS, méthode</span><span class="sxs-lookup"><span data-stu-id="8795b-103">Api.JetGetLS method</span></span>

<span data-ttu-id="8795b-104">Permet à l’application de récupérer le descripteur de contexte appelé stockage local qui est associé à un curseur ou la table associée à ce curseur.</span><span class="sxs-lookup"><span data-stu-id="8795b-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="8795b-105">Ce descripteur de contexte doit avoir été défini précédemment à l’aide [de JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="8795b-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="8795b-106">JetGetLS peut également être utilisé pour extraire simultanément le descripteur de contexte actuel d’un curseur ou d’une table et réinitialiser ce handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="8795b-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="8795b-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8795b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8795b-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8795b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8795b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8795b-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8795b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8795b-110">Parameters</span></span>

  - <span data-ttu-id="8795b-111">sesid</span><span class="sxs-lookup"><span data-stu-id="8795b-111">sesid</span></span>  
    <span data-ttu-id="8795b-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8795b-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8795b-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8795b-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8795b-114">TableID</span><span class="sxs-lookup"><span data-stu-id="8795b-114">tableid</span></span>  
    <span data-ttu-id="8795b-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8795b-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8795b-116">Curseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8795b-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8795b-117">ls</span><span class="sxs-lookup"><span data-stu-id="8795b-117">ls</span></span>  
    <span data-ttu-id="8795b-118">Type : [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8795b-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="8795b-119">Retourne le handle de contexte récupéré.</span><span class="sxs-lookup"><span data-stu-id="8795b-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="8795b-120">grbit</span><span class="sxs-lookup"><span data-stu-id="8795b-120">grbit</span></span>  
    <span data-ttu-id="8795b-121">Type : [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8795b-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8795b-122">Récupérez les options.</span><span class="sxs-lookup"><span data-stu-id="8795b-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8795b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8795b-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8795b-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8795b-124">Reference</span></span>

[<span data-ttu-id="8795b-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="8795b-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8795b-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="8795b-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8795b-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8795b-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
