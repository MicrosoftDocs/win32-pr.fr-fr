---
description: 'En savoir plus sur : méthode API. JetAttachDatabase2'
title: API. JetAttachDatabase2, méthode
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750772"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="39e26-103">API. JetAttachDatabase2, méthode</span><span class="sxs-lookup"><span data-stu-id="39e26-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="39e26-104">Joint un fichier de base de données à utiliser avec une instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="39e26-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="39e26-105">Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="39e26-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="39e26-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39e26-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39e26-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39e26-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39e26-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39e26-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="39e26-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39e26-109">Parameters</span></span>

  - <span data-ttu-id="39e26-110">sesid</span><span class="sxs-lookup"><span data-stu-id="39e26-110">sesid</span></span>  
    <span data-ttu-id="39e26-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="39e26-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="39e26-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="39e26-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="39e26-113">database</span><span class="sxs-lookup"><span data-stu-id="39e26-113">database</span></span>  
    <span data-ttu-id="39e26-114">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="39e26-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="39e26-115">Base de données à attacher.</span><span class="sxs-lookup"><span data-stu-id="39e26-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="39e26-116">maxPages</span><span class="sxs-lookup"><span data-stu-id="39e26-116">maxPages</span></span>  
    <span data-ttu-id="39e26-117">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="39e26-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="39e26-118">Taille maximale, en pages de base de données, de la base de données.</span><span class="sxs-lookup"><span data-stu-id="39e26-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="39e26-119">Le passage de la valeur 0 signifie qu’il n’y a pas de maximum appliqué.</span><span class="sxs-lookup"><span data-stu-id="39e26-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="39e26-120">grbit</span><span class="sxs-lookup"><span data-stu-id="39e26-120">grbit</span></span>  
    <span data-ttu-id="39e26-121">Type : [Microsoft. ISAM. esent. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="39e26-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="39e26-122">Options d’attachement.</span><span class="sxs-lookup"><span data-stu-id="39e26-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="39e26-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39e26-123">Return value</span></span>

<span data-ttu-id="39e26-124">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="39e26-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="39e26-125">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="39e26-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39e26-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39e26-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39e26-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="39e26-127">Reference</span></span>

[<span data-ttu-id="39e26-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="39e26-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="39e26-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="39e26-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="39e26-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="39e26-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
