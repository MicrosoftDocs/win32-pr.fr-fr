---
description: 'En savoir plus sur : méthode API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)'
title: Méthode API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_OBJECTLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100728
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9564b0eb2dc8a5bee2e65b729164f39a19d349fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750764"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objectlist"></a><span data-ttu-id="87633-103">Méthode API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</span><span class="sxs-lookup"><span data-stu-id="87633-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)</span></span>

<span data-ttu-id="87633-104">Récupère des informations sur les objets de base de données.</span><span class="sxs-lookup"><span data-stu-id="87633-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="87633-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87633-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87633-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="87633-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87633-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87633-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef objectlist As JET_OBJECTLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objectlist As JET_OBJECTLISTApi.JetGetObjectInfo(sesid, dbid, _
    objectlist)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out JET_OBJECTLIST objectlist
)
```

#### <a name="parameters"></a><span data-ttu-id="87633-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87633-108">Parameters</span></span>

  - <span data-ttu-id="87633-109">sesid</span><span class="sxs-lookup"><span data-stu-id="87633-109">sesid</span></span>  
    <span data-ttu-id="87633-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87633-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="87633-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="87633-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="87633-112">dbid</span><span class="sxs-lookup"><span data-stu-id="87633-112">dbid</span></span>  
    <span data-ttu-id="87633-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="87633-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="87633-114">Base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="87633-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="87633-115">ObjectList</span><span class="sxs-lookup"><span data-stu-id="87633-115">objectlist</span></span>  
    <span data-ttu-id="87633-116">Type : [Microsoft.ISAM.esent.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="87633-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span></span>  
    
    <span data-ttu-id="87633-117">Renseigné avec des informations sur les objets dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="87633-117">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="87633-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87633-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87633-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="87633-119">Reference</span></span>

[<span data-ttu-id="87633-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="87633-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="87633-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="87633-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="87633-122">Surcharge JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="87633-122">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="87633-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="87633-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
