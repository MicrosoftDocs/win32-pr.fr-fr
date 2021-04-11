---
description: 'En savoir plus sur : méthode API. JetAttachDatabase'
title: API. JetAttachDatabase, méthode
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0447d4e6c5e8474c4d82340e35a23692096305bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111943"
---
# <a name="apijetattachdatabase-method"></a><span data-ttu-id="c60ad-103">API. JetAttachDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="c60ad-103">Api.JetAttachDatabase method</span></span>

<span data-ttu-id="c60ad-104">Joint un fichier de base de données à utiliser avec une instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="c60ad-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="c60ad-105">Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="c60ad-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="c60ad-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c60ad-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c60ad-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c60ad-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c60ad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c60ad-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c60ad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c60ad-109">Parameters</span></span>

  - <span data-ttu-id="c60ad-110">sesid</span><span class="sxs-lookup"><span data-stu-id="c60ad-110">sesid</span></span>  
    <span data-ttu-id="c60ad-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c60ad-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c60ad-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c60ad-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c60ad-113">database</span><span class="sxs-lookup"><span data-stu-id="c60ad-113">database</span></span>  
    <span data-ttu-id="c60ad-114">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c60ad-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c60ad-115">Base de données à attacher.</span><span class="sxs-lookup"><span data-stu-id="c60ad-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="c60ad-116">grbit</span><span class="sxs-lookup"><span data-stu-id="c60ad-116">grbit</span></span>  
    <span data-ttu-id="c60ad-117">Type : [Microsoft. ISAM. esent. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c60ad-117">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c60ad-118">Options d’attachement.</span><span class="sxs-lookup"><span data-stu-id="c60ad-118">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c60ad-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c60ad-119">Return value</span></span>

<span data-ttu-id="c60ad-120">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c60ad-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="c60ad-121">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="c60ad-121">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c60ad-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c60ad-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c60ad-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c60ad-123">Reference</span></span>

[<span data-ttu-id="c60ad-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="c60ad-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c60ad-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="c60ad-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c60ad-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c60ad-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
