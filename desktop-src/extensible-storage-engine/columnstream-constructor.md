---
description: 'En savoir plus sur : constructeur ColumnStream'
title: Constructeur ColumnStream
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 498fed2daf2cad5903d9597689a80eadca7bd569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951404"
---
# <a name="columnstream-constructor"></a><span data-ttu-id="25a93-103">Constructeur ColumnStream</span><span class="sxs-lookup"><span data-stu-id="25a93-103">ColumnStream constructor</span></span>

<span data-ttu-id="25a93-104">Initialise une nouvelle instance de la classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="25a93-104">Initializes a new instance of the ColumnStream class.</span></span>

<span data-ttu-id="25a93-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25a93-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25a93-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25a93-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25a93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25a93-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="25a93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25a93-108">Parameters</span></span>

  - <span data-ttu-id="25a93-109">sesid</span><span class="sxs-lookup"><span data-stu-id="25a93-109">sesid</span></span>  
    <span data-ttu-id="25a93-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25a93-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25a93-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="25a93-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25a93-112">TableID</span><span class="sxs-lookup"><span data-stu-id="25a93-112">tableid</span></span>  
    <span data-ttu-id="25a93-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25a93-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="25a93-114">Curseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="25a93-114">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25a93-115">columnid</span><span class="sxs-lookup"><span data-stu-id="25a93-115">columnid</span></span>  
    <span data-ttu-id="25a93-116">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25a93-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="25a93-117">ColumnID de la colonne à partir duquel définir/récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="25a93-117">The columnid of the column to set/retrieve data from.</span></span>

## <a name="see-also"></a><span data-ttu-id="25a93-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25a93-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25a93-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="25a93-119">Reference</span></span>

[<span data-ttu-id="25a93-120">ColumnStream, classe</span><span class="sxs-lookup"><span data-stu-id="25a93-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="25a93-121">Membres ColumnStream</span><span class="sxs-lookup"><span data-stu-id="25a93-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="25a93-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="25a93-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
