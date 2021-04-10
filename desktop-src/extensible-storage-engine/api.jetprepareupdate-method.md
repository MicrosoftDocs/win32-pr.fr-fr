---
description: 'En savoir plus sur : méthode API. JetPrepareUpdate'
title: API. JetPrepareUpdate, méthode
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210525"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="bf0c9-103">API. JetPrepareUpdate, méthode</span><span class="sxs-lookup"><span data-stu-id="bf0c9-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="bf0c9-104">Préparez un curseur pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bf0c9-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="bf0c9-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf0c9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf0c9-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf0c9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf0c9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="bf0c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf0c9-108">Parameters</span></span>

  - <span data-ttu-id="bf0c9-109">sesid</span><span class="sxs-lookup"><span data-stu-id="bf0c9-109">sesid</span></span>  
    <span data-ttu-id="bf0c9-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf0c9-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bf0c9-111">Session qui démarre la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bf0c9-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf0c9-112">TableID</span><span class="sxs-lookup"><span data-stu-id="bf0c9-112">tableid</span></span>  
    <span data-ttu-id="bf0c9-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf0c9-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bf0c9-114">Curseur pour lequel la mise à jour doit être démarrée.</span><span class="sxs-lookup"><span data-stu-id="bf0c9-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf0c9-115">préparation</span><span class="sxs-lookup"><span data-stu-id="bf0c9-115">prep</span></span>  
    <span data-ttu-id="bf0c9-116">Type : [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bf0c9-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="bf0c9-117">Type de mise à jour à préparer.</span><span class="sxs-lookup"><span data-stu-id="bf0c9-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf0c9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf0c9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf0c9-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="bf0c9-119">Reference</span></span>

[<span data-ttu-id="bf0c9-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="bf0c9-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bf0c9-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="bf0c9-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bf0c9-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bf0c9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
