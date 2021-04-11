---
description: 'En savoir plus sur : méthode API. JetGetCursorInfo'
title: API. JetGetCursorInfo, méthode
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033912"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="b3114-103">API. JetGetCursorInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="b3114-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="b3114-104">Détermine si une mise à jour de l’enregistrement en cours d’un curseur entraîne un conflit d’écriture, en fonction de l’état de mise à jour actuel de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3114-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="b3114-105">Il est possible qu’un conflit d’écriture soit retourné, même si JetGetCursorInfo est retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="b3114-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="b3114-106">parce qu’une autre session peut mettre à jour l’enregistrement avant que la session actuelle puisse mettre à jour le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3114-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="b3114-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3114-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b3114-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3114-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3114-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3114-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b3114-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3114-110">Parameters</span></span>

  - <span data-ttu-id="b3114-111">sesid</span><span class="sxs-lookup"><span data-stu-id="b3114-111">sesid</span></span>  
    <span data-ttu-id="b3114-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3114-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b3114-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b3114-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3114-114">TableID</span><span class="sxs-lookup"><span data-stu-id="b3114-114">tableid</span></span>  
    <span data-ttu-id="b3114-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3114-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b3114-116">Curseur à vérifier.</span><span class="sxs-lookup"><span data-stu-id="b3114-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3114-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3114-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3114-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b3114-118">Reference</span></span>

[<span data-ttu-id="b3114-119">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b3114-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b3114-120">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b3114-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b3114-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b3114-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
