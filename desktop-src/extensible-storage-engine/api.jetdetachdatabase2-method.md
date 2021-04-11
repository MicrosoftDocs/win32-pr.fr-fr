---
description: 'En savoir plus sur : méthode API. JetDetachDatabase2'
title: API. JetDetachDatabase2, méthode
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44cc8b5d03ba720f1acb7d0e8603bf29906a611e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112595"
---
# <a name="apijetdetachdatabase2-method"></a><span data-ttu-id="579c3-103">API. JetDetachDatabase2, méthode</span><span class="sxs-lookup"><span data-stu-id="579c3-103">Api.JetDetachDatabase2 method</span></span>

<span data-ttu-id="579c3-104">Libère un fichier de base de données qui était précédemment attaché à une session de base de données.</span><span class="sxs-lookup"><span data-stu-id="579c3-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="579c3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="579c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="579c3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="579c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="579c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="579c3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="579c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="579c3-108">Parameters</span></span>

  - <span data-ttu-id="579c3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="579c3-109">sesid</span></span>  
    <span data-ttu-id="579c3-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="579c3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="579c3-111">Session de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="579c3-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="579c3-112">database</span><span class="sxs-lookup"><span data-stu-id="579c3-112">database</span></span>  
    <span data-ttu-id="579c3-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="579c3-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="579c3-114">Base de données à détacher.</span><span class="sxs-lookup"><span data-stu-id="579c3-114">The database to detach.</span></span>

<!-- end list -->

  - <span data-ttu-id="579c3-115">grbit</span><span class="sxs-lookup"><span data-stu-id="579c3-115">grbit</span></span>  
    <span data-ttu-id="579c3-116">Type : [Microsoft. ISAM. esent. Interop. DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="579c3-116">Type: [Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="579c3-117">Options de détachement.</span><span class="sxs-lookup"><span data-stu-id="579c3-117">Detach options.</span></span>

## <a name="see-also"></a><span data-ttu-id="579c3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="579c3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="579c3-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="579c3-119">Reference</span></span>

[<span data-ttu-id="579c3-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="579c3-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="579c3-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="579c3-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="579c3-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="579c3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
