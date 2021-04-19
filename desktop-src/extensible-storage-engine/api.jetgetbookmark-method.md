---
description: 'En savoir plus sur : méthode API. JetGetBookmark'
title: API. JetGetBookmark, méthode
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514594"
---
# <a name="apijetgetbookmark-method"></a><span data-ttu-id="6aa78-103">API. JetGetBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="6aa78-103">Api.JetGetBookmark method</span></span>

<span data-ttu-id="6aa78-104">Récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="6aa78-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="6aa78-105">Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de [JetGotoBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetgotobookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="6aa78-105">This bookmark can then be used to reposition that cursor back to the same record using [JetGotoBookmark(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetgotobookmark-method.md).</span></span> <span data-ttu-id="6aa78-106">Le signet ne doit pas dépasser [BookmarkMost](./systemparameters.bookmarkmost-property.md) octets.</span><span class="sxs-lookup"><span data-stu-id="6aa78-106">The bookmark will be no longer than [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span></span> <span data-ttu-id="6aa78-107">Consultez également [GetBookmark (JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="6aa78-107">Also see [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span></span>

<span data-ttu-id="6aa78-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6aa78-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6aa78-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6aa78-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa78-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aa78-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="6aa78-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aa78-111">Parameters</span></span>

  - <span data-ttu-id="6aa78-112">sesid</span><span class="sxs-lookup"><span data-stu-id="6aa78-112">sesid</span></span>  
    <span data-ttu-id="6aa78-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6aa78-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6aa78-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6aa78-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6aa78-115">TableID</span><span class="sxs-lookup"><span data-stu-id="6aa78-115">tableid</span></span>  
    <span data-ttu-id="6aa78-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6aa78-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6aa78-117">Curseur à partir duquel récupérer le signet.</span><span class="sxs-lookup"><span data-stu-id="6aa78-117">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6aa78-118">signet</span><span class="sxs-lookup"><span data-stu-id="6aa78-118">bookmark</span></span>  
    <span data-ttu-id="6aa78-119">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="6aa78-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="6aa78-120">Mémoire tampon devant contenir le signet.</span><span class="sxs-lookup"><span data-stu-id="6aa78-120">Buffer to contain the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="6aa78-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="6aa78-121">bookmarkSize</span></span>  
    <span data-ttu-id="6aa78-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6aa78-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6aa78-123">Taille de la mémoire tampon du signet.</span><span class="sxs-lookup"><span data-stu-id="6aa78-123">Size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="6aa78-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="6aa78-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="6aa78-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6aa78-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6aa78-126">Retourne la taille réelle du signet.</span><span class="sxs-lookup"><span data-stu-id="6aa78-126">Returns the actual size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="6aa78-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aa78-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6aa78-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6aa78-128">Reference</span></span>

[<span data-ttu-id="6aa78-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="6aa78-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6aa78-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="6aa78-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6aa78-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6aa78-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
