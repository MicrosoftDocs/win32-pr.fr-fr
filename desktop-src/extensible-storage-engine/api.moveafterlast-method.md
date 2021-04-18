---
description: 'En savoir plus sur : méthode API. MoveAfterLast'
title: API. MoveAfterLast, méthode
TOCTitle: 'MoveAfterLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveAfterLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.moveafterlast(v=EXCHG.10)
ms:contentKeyID: 55100851
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37d3e4eae32c9540f3ee469e4b782c893aa15c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523050"
---
# <a name="apimoveafterlast-method"></a><span data-ttu-id="f6e03-103">API. MoveAfterLast, méthode</span><span class="sxs-lookup"><span data-stu-id="f6e03-103">Api.MoveAfterLast method</span></span>

<span data-ttu-id="f6e03-104">Positionnez le curseur après le dernier enregistrement de la table.</span><span class="sxs-lookup"><span data-stu-id="f6e03-104">Position the cursor after the last record in the table.</span></span> <span data-ttu-id="f6e03-105">Un déplacement suivant place le curseur sur le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f6e03-105">A subsequent move previous will position the cursor on the last record.</span></span>

<span data-ttu-id="f6e03-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6e03-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6e03-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6e03-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e03-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6e03-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveAfterLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveAfterLast(sesid, tableid)
```

``` csharp
public static void MoveAfterLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="f6e03-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6e03-109">Parameters</span></span>

  - <span data-ttu-id="f6e03-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f6e03-110">sesid</span></span>  
    <span data-ttu-id="f6e03-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6e03-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f6e03-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f6e03-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6e03-113">TableID</span><span class="sxs-lookup"><span data-stu-id="f6e03-113">tableid</span></span>  
    <span data-ttu-id="f6e03-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6e03-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f6e03-115">Table à positionner.</span><span class="sxs-lookup"><span data-stu-id="f6e03-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6e03-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6e03-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6e03-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f6e03-117">Reference</span></span>

[<span data-ttu-id="f6e03-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="f6e03-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f6e03-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="f6e03-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f6e03-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f6e03-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
