---
description: 'En savoir plus sur : méthode API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)'
title: Méthode API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100705
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e690dbb2a4b82698440b3be3c483bb46b2eca8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862238"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnbase"></a><span data-ttu-id="7777b-103">Méthode API. JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="7777b-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</span></span>

<span data-ttu-id="7777b-104">Récupère des informations sur une colonne dans une table.</span><span class="sxs-lookup"><span data-stu-id="7777b-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="7777b-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7777b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7777b-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7777b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7777b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7777b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnbase As JET_COLUMNBASEApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="7777b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7777b-108">Parameters</span></span>

  - <span data-ttu-id="7777b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7777b-109">sesid</span></span>  
    <span data-ttu-id="7777b-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7777b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7777b-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7777b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7777b-112">dbid</span><span class="sxs-lookup"><span data-stu-id="7777b-112">dbid</span></span>  
    <span data-ttu-id="7777b-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7777b-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7777b-114">Base de données qui contient la table.</span><span class="sxs-lookup"><span data-stu-id="7777b-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7777b-115">tablename</span><span class="sxs-lookup"><span data-stu-id="7777b-115">tablename</span></span>  
    <span data-ttu-id="7777b-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7777b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7777b-117">Nom de la table contenant la colonne.</span><span class="sxs-lookup"><span data-stu-id="7777b-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="7777b-118">columnName</span><span class="sxs-lookup"><span data-stu-id="7777b-118">columnName</span></span>  
    <span data-ttu-id="7777b-119">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7777b-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7777b-120">Nom de la colonne.</span><span class="sxs-lookup"><span data-stu-id="7777b-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="7777b-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="7777b-121">columnbase</span></span>  
    <span data-ttu-id="7777b-122">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="7777b-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="7777b-123">Renseigné avec des informations sur les colonnes de la table.</span><span class="sxs-lookup"><span data-stu-id="7777b-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="7777b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7777b-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7777b-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7777b-125">Reference</span></span>

[<span data-ttu-id="7777b-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7777b-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7777b-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7777b-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7777b-128">Surcharge JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="7777b-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="7777b-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7777b-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
