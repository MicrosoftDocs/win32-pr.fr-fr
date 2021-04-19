---
description: 'En savoir plus sur : méthode API. JetCreateDatabase'
title: API. JetCreateDatabase, méthode
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515827"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="91df7-103">API. JetCreateDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="91df7-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="91df7-104">Crée et attache un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="91df7-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="91df7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="91df7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="91df7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="91df7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="91df7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91df7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="91df7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91df7-108">Parameters</span></span>

  - <span data-ttu-id="91df7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="91df7-109">sesid</span></span>  
    <span data-ttu-id="91df7-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="91df7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="91df7-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="91df7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="91df7-112">database</span><span class="sxs-lookup"><span data-stu-id="91df7-112">database</span></span>  
    <span data-ttu-id="91df7-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="91df7-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="91df7-114">Chemin d’accès au fichier de base de données à créer.</span><span class="sxs-lookup"><span data-stu-id="91df7-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="91df7-115">se connecter</span><span class="sxs-lookup"><span data-stu-id="91df7-115">connect</span></span>  
    <span data-ttu-id="91df7-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="91df7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="91df7-117">Le paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="91df7-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="91df7-118">dbid</span><span class="sxs-lookup"><span data-stu-id="91df7-118">dbid</span></span>  
    <span data-ttu-id="91df7-119">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="91df7-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="91df7-120">Retourne le dbid de la nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="91df7-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="91df7-121">grbit</span><span class="sxs-lookup"><span data-stu-id="91df7-121">grbit</span></span>  
    <span data-ttu-id="91df7-122">Type : [Microsoft. ISAM. esent. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="91df7-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="91df7-123">Options de création de base de données.</span><span class="sxs-lookup"><span data-stu-id="91df7-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="91df7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91df7-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91df7-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="91df7-125">Reference</span></span>

[<span data-ttu-id="91df7-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="91df7-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="91df7-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="91df7-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="91df7-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="91df7-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
