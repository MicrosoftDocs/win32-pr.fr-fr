---
description: 'En savoir plus sur : méthode Windows8Api. JetSetCursorFilter'
title: Méthode Windows8Api. JetSetCursorFilter (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514251"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="b0187-103">Méthode Windows8Api. JetSetCursorFilter</span><span class="sxs-lookup"><span data-stu-id="b0187-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="b0187-104">Définissez un tableau de filtres simples pour [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span><span class="sxs-lookup"><span data-stu-id="b0187-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="b0187-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0187-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="b0187-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0187-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0187-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0187-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b0187-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0187-108">Parameters</span></span>

  - <span data-ttu-id="b0187-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b0187-109">sesid</span></span>  
    <span data-ttu-id="b0187-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0187-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b0187-111">Session à utiliser pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="b0187-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0187-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b0187-112">tableid</span></span>  
    <span data-ttu-id="b0187-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0187-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b0187-114">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="b0187-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0187-115">filtres</span><span class="sxs-lookup"><span data-stu-id="b0187-115">filters</span></span>  
    <span data-ttu-id="b0187-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="b0187-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="b0187-117">Filtres d’enregistrement simples.</span><span class="sxs-lookup"><span data-stu-id="b0187-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0187-118">grbit</span><span class="sxs-lookup"><span data-stu-id="b0187-118">grbit</span></span>  
    <span data-ttu-id="b0187-119">Tapez : [Microsoft. ISAM. esent. Interop. Windows8. CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b0187-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b0187-120">Options de déplacement.</span><span class="sxs-lookup"><span data-stu-id="b0187-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0187-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0187-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0187-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b0187-122">Reference</span></span>

[<span data-ttu-id="b0187-123">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="b0187-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="b0187-124">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="b0187-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="b0187-125">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="b0187-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
