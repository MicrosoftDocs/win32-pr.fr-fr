---
description: 'En savoir plus sur : méthode API. JetDelete'
title: API. JetDelete, méthode
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862242"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="b28ba-103">API. JetDelete, méthode</span><span class="sxs-lookup"><span data-stu-id="b28ba-103">Api.JetDelete method</span></span>

<span data-ttu-id="b28ba-104">Supprime l’enregistrement en cours dans une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="b28ba-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="b28ba-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b28ba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b28ba-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b28ba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b28ba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b28ba-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b28ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b28ba-108">Parameters</span></span>

  - <span data-ttu-id="b28ba-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b28ba-109">sesid</span></span>  
    <span data-ttu-id="b28ba-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b28ba-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b28ba-111">Session qui a ouvert le curseur.</span><span class="sxs-lookup"><span data-stu-id="b28ba-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="b28ba-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b28ba-112">tableid</span></span>  
    <span data-ttu-id="b28ba-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b28ba-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b28ba-114">Curseur sur une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="b28ba-114">The cursor on a database table.</span></span> <span data-ttu-id="b28ba-115">La ligne actuelle sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="b28ba-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="b28ba-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b28ba-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b28ba-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b28ba-117">Reference</span></span>

[<span data-ttu-id="b28ba-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b28ba-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b28ba-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b28ba-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b28ba-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b28ba-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
