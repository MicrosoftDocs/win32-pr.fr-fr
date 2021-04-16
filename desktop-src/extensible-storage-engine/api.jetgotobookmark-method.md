---
description: 'En savoir plus sur : méthode API. JetGotoBookmark'
title: API. JetGotoBookmark, méthode
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530202"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="7125a-103">API. JetGotoBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="7125a-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="7125a-104">Positionne un curseur sur une entrée d’index pour l’enregistrement associé au signet spécifié.</span><span class="sxs-lookup"><span data-stu-id="7125a-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="7125a-105">Le signet peut être utilisé avec n’importe quel index défini sur une table.</span><span class="sxs-lookup"><span data-stu-id="7125a-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="7125a-106">Le signet d’un enregistrement peut être récupéré à l’aide de [JetGetBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetgetbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="7125a-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="7125a-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7125a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7125a-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7125a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7125a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7125a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="7125a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7125a-110">Parameters</span></span>

  - <span data-ttu-id="7125a-111">sesid</span><span class="sxs-lookup"><span data-stu-id="7125a-111">sesid</span></span>  
    <span data-ttu-id="7125a-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7125a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7125a-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7125a-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7125a-114">TableID</span><span class="sxs-lookup"><span data-stu-id="7125a-114">tableid</span></span>  
    <span data-ttu-id="7125a-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7125a-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7125a-116">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="7125a-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="7125a-117">signet</span><span class="sxs-lookup"><span data-stu-id="7125a-117">bookmark</span></span>  
    <span data-ttu-id="7125a-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="7125a-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="7125a-119">Signet utilisé pour positionner le curseur.</span><span class="sxs-lookup"><span data-stu-id="7125a-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="7125a-120">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="7125a-120">bookmarkSize</span></span>  
    <span data-ttu-id="7125a-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7125a-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7125a-122">Taille du signet.</span><span class="sxs-lookup"><span data-stu-id="7125a-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="7125a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7125a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7125a-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7125a-124">Reference</span></span>

[<span data-ttu-id="7125a-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7125a-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7125a-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7125a-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7125a-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7125a-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
