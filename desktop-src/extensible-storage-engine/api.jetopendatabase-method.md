---
description: 'En savoir plus sur : méthode API. JetOpenDatabase'
title: API. JetOpenDatabase, méthode
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210533"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="061cc-103">API. JetOpenDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="061cc-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="061cc-104">Ouvre une base de données précédemment attachée avec [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), à utiliser avec une session de base de données.</span><span class="sxs-lookup"><span data-stu-id="061cc-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="061cc-105">Cette fonction peut être appelée plusieurs fois pour la même base de données.</span><span class="sxs-lookup"><span data-stu-id="061cc-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="061cc-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="061cc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="061cc-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="061cc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="061cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="061cc-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="061cc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="061cc-109">Parameters</span></span>

  - <span data-ttu-id="061cc-110">sesid</span><span class="sxs-lookup"><span data-stu-id="061cc-110">sesid</span></span>  
    <span data-ttu-id="061cc-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="061cc-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="061cc-112">Session qui ouvre la base de données.</span><span class="sxs-lookup"><span data-stu-id="061cc-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="061cc-113">database</span><span class="sxs-lookup"><span data-stu-id="061cc-113">database</span></span>  
    <span data-ttu-id="061cc-114">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="061cc-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="061cc-115">Base de données à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="061cc-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="061cc-116">se connecter</span><span class="sxs-lookup"><span data-stu-id="061cc-116">connect</span></span>  
    <span data-ttu-id="061cc-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="061cc-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="061cc-118">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="061cc-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="061cc-119">dbid</span><span class="sxs-lookup"><span data-stu-id="061cc-119">dbid</span></span>  
    <span data-ttu-id="061cc-120">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="061cc-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="061cc-121">Retourne le dbid de la base de données attachée.</span><span class="sxs-lookup"><span data-stu-id="061cc-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="061cc-122">grbit</span><span class="sxs-lookup"><span data-stu-id="061cc-122">grbit</span></span>  
    <span data-ttu-id="061cc-123">Type : [Microsoft. ISAM. esent. Interop. OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="061cc-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="061cc-124">Options de base de données ouvertes.</span><span class="sxs-lookup"><span data-stu-id="061cc-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="061cc-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="061cc-125">Return value</span></span>

<span data-ttu-id="061cc-126">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="061cc-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="061cc-127">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="061cc-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="061cc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="061cc-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="061cc-129">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="061cc-129">Reference</span></span>

[<span data-ttu-id="061cc-130">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="061cc-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="061cc-131">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="061cc-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="061cc-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="061cc-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
