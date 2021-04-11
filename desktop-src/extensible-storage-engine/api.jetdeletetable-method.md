---
description: 'En savoir plus sur : méthode API. JetDeleteTable'
title: API. JetDeleteTable, méthode
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b4128ae81484343bec7fb4f52a736db149f0eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112599"
---
# <a name="apijetdeletetable-method"></a><span data-ttu-id="c6708-103">API. JetDeleteTable, méthode</span><span class="sxs-lookup"><span data-stu-id="c6708-103">Api.JetDeleteTable method</span></span>

<span data-ttu-id="c6708-104">Supprime une table d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="c6708-104">Deletes a table from a database.</span></span>

<span data-ttu-id="c6708-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c6708-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c6708-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c6708-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c6708-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6708-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a><span data-ttu-id="c6708-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6708-108">Parameters</span></span>

  - <span data-ttu-id="c6708-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c6708-109">sesid</span></span>  
    <span data-ttu-id="c6708-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6708-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c6708-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c6708-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6708-112">dbid</span><span class="sxs-lookup"><span data-stu-id="c6708-112">dbid</span></span>  
    <span data-ttu-id="c6708-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6708-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c6708-114">Base de données à partir de laquelle supprimer la table.</span><span class="sxs-lookup"><span data-stu-id="c6708-114">The database to delete the table from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6708-115">table</span><span class="sxs-lookup"><span data-stu-id="c6708-115">table</span></span>  
    <span data-ttu-id="c6708-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c6708-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c6708-117">Nom de la table à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c6708-117">The name of the table to delete.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6708-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6708-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c6708-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c6708-119">Reference</span></span>

[<span data-ttu-id="c6708-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="c6708-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c6708-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="c6708-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c6708-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c6708-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
