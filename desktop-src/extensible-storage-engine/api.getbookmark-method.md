---
description: 'En savoir plus sur : méthode API. GetBookmark'
title: API. GetBookmark, méthode
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524795"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="56ebb-103">API. GetBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="56ebb-103">Api.GetBookmark method</span></span>

<span data-ttu-id="56ebb-104">Récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="56ebb-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="56ebb-105">Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de JetGotoBookmark.</span><span class="sxs-lookup"><span data-stu-id="56ebb-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="56ebb-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56ebb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56ebb-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56ebb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56ebb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56ebb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="56ebb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56ebb-109">Parameters</span></span>

  - <span data-ttu-id="56ebb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="56ebb-110">sesid</span></span>  
    <span data-ttu-id="56ebb-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="56ebb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="56ebb-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="56ebb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="56ebb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="56ebb-113">tableid</span></span>  
    <span data-ttu-id="56ebb-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="56ebb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="56ebb-115">Curseur à partir duquel récupérer le signet.</span><span class="sxs-lookup"><span data-stu-id="56ebb-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="56ebb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56ebb-116">Return value</span></span>

<span data-ttu-id="56ebb-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="56ebb-117">Type: \[\]</span></span>  
<span data-ttu-id="56ebb-118">Signet de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="56ebb-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56ebb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56ebb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56ebb-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="56ebb-120">Reference</span></span>

[<span data-ttu-id="56ebb-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="56ebb-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="56ebb-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="56ebb-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="56ebb-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="56ebb-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
