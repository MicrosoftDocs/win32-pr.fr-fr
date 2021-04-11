---
description: 'En savoir plus sur : méthode VistaApi. JetGetColumnInfo'
title: Méthode VistaApi. JetGetColumnInfo (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113586"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="1fb94-103">Méthode VistaApi. JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1fb94-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="1fb94-104">Récupère des informations sur une colonne dans une table.</span><span class="sxs-lookup"><span data-stu-id="1fb94-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="1fb94-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fb94-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1fb94-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fb94-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb94-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fb94-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="1fb94-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fb94-108">Parameters</span></span>

  - <span data-ttu-id="1fb94-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1fb94-109">sesid</span></span>  
    <span data-ttu-id="1fb94-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fb94-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1fb94-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1fb94-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fb94-112">dbid</span><span class="sxs-lookup"><span data-stu-id="1fb94-112">dbid</span></span>  
    <span data-ttu-id="1fb94-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fb94-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1fb94-114">Base de données qui contient la table.</span><span class="sxs-lookup"><span data-stu-id="1fb94-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fb94-115">tablename</span><span class="sxs-lookup"><span data-stu-id="1fb94-115">tablename</span></span>  
    <span data-ttu-id="1fb94-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1fb94-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1fb94-117">Nom de la table contenant la colonne.</span><span class="sxs-lookup"><span data-stu-id="1fb94-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fb94-118">columnid</span><span class="sxs-lookup"><span data-stu-id="1fb94-118">columnid</span></span>  
    <span data-ttu-id="1fb94-119">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fb94-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1fb94-120">ID de la colonne.</span><span class="sxs-lookup"><span data-stu-id="1fb94-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fb94-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="1fb94-121">columnbase</span></span>  
    <span data-ttu-id="1fb94-122">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="1fb94-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="1fb94-123">Renseigné avec des informations sur les colonnes de la table.</span><span class="sxs-lookup"><span data-stu-id="1fb94-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fb94-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fb94-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fb94-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1fb94-125">Reference</span></span>

[<span data-ttu-id="1fb94-126">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="1fb94-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="1fb94-127">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="1fb94-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="1fb94-128">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="1fb94-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
