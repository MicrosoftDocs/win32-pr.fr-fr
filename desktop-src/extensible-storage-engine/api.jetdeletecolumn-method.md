---
description: 'En savoir plus sur : méthode API. JetDeleteColumn'
title: API. JetDeleteColumn, méthode
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112602"
---
# <a name="apijetdeletecolumn-method"></a><span data-ttu-id="82f27-103">API. JetDeleteColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="82f27-103">Api.JetDeleteColumn method</span></span>

<span data-ttu-id="82f27-104">Supprime une colonne d’une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="82f27-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="82f27-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82f27-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82f27-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82f27-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82f27-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82f27-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a><span data-ttu-id="82f27-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82f27-108">Parameters</span></span>

  - <span data-ttu-id="82f27-109">sesid</span><span class="sxs-lookup"><span data-stu-id="82f27-109">sesid</span></span>  
    <span data-ttu-id="82f27-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82f27-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="82f27-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="82f27-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="82f27-112">TableID</span><span class="sxs-lookup"><span data-stu-id="82f27-112">tableid</span></span>  
    <span data-ttu-id="82f27-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82f27-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="82f27-114">Curseur sur la table à partir duquel supprimer la colonne.</span><span class="sxs-lookup"><span data-stu-id="82f27-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="82f27-115">colonne</span><span class="sxs-lookup"><span data-stu-id="82f27-115">column</span></span>  
    <span data-ttu-id="82f27-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="82f27-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="82f27-117">Nom de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="82f27-117">The name of the column to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="82f27-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82f27-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82f27-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="82f27-119">Reference</span></span>

[<span data-ttu-id="82f27-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="82f27-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82f27-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="82f27-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82f27-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82f27-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
