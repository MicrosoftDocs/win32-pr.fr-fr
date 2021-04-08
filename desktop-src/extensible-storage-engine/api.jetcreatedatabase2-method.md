---
description: 'En savoir plus sur : méthode API. JetCreateDatabase2'
title: API. JetCreateDatabase2, méthode
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749500"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="ada2f-103">API. JetCreateDatabase2, méthode</span><span class="sxs-lookup"><span data-stu-id="ada2f-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="ada2f-104">Crée et attache un fichier de base de données avec une taille de base de données maximale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ada2f-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="ada2f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ada2f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ada2f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ada2f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ada2f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ada2f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ada2f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ada2f-108">Parameters</span></span>

  - <span data-ttu-id="ada2f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ada2f-109">sesid</span></span>  
    <span data-ttu-id="ada2f-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ada2f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ada2f-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ada2f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ada2f-112">database</span><span class="sxs-lookup"><span data-stu-id="ada2f-112">database</span></span>  
    <span data-ttu-id="ada2f-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ada2f-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ada2f-114">Chemin d’accès au fichier de base de données à créer.</span><span class="sxs-lookup"><span data-stu-id="ada2f-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="ada2f-115">maxPages</span><span class="sxs-lookup"><span data-stu-id="ada2f-115">maxPages</span></span>  
    <span data-ttu-id="ada2f-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ada2f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ada2f-117">Taille maximale, en pages de base de données, de la base de données.</span><span class="sxs-lookup"><span data-stu-id="ada2f-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="ada2f-118">Le passage de la valeur 0 signifie qu’il n’y a pas de maximum appliqué.</span><span class="sxs-lookup"><span data-stu-id="ada2f-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="ada2f-119">dbid</span><span class="sxs-lookup"><span data-stu-id="ada2f-119">dbid</span></span>  
    <span data-ttu-id="ada2f-120">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ada2f-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ada2f-121">Retourne le dbid de la nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="ada2f-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="ada2f-122">grbit</span><span class="sxs-lookup"><span data-stu-id="ada2f-122">grbit</span></span>  
    <span data-ttu-id="ada2f-123">Type : [Microsoft. ISAM. esent. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ada2f-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ada2f-124">Options de création de base de données.</span><span class="sxs-lookup"><span data-stu-id="ada2f-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ada2f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ada2f-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ada2f-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ada2f-126">Reference</span></span>

[<span data-ttu-id="ada2f-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="ada2f-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ada2f-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="ada2f-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ada2f-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ada2f-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
