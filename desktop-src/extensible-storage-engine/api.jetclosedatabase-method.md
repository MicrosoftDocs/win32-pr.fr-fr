---
description: 'En savoir plus sur : méthode API. JetCloseDatabase'
title: API. JetCloseDatabase, méthode
TOCTitle: 'JetCloseDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosedatabase(v=EXCHG.10)
ms:contentKeyID: 55100662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39d830c34f2d772730d7ea1c65ec4adf3c3d4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525642"
---
# <a name="apijetclosedatabase-method"></a><span data-ttu-id="9aa9e-103">API. JetCloseDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="9aa9e-103">Api.JetCloseDatabase method</span></span>

<span data-ttu-id="9aa9e-104">Ferme un fichier de base de données qui a été ouvert précédemment avec [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) ou créé avec [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="9aa9e-104">Closes a database file that was previously opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) or created with [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="9aa9e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9aa9e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9aa9e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    grbit As CloseDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim grbit As CloseDatabaseGrbitApi.JetCloseDatabase(sesid, dbid, _
    grbit)
```

``` csharp
public static void JetCloseDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    CloseDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9aa9e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9aa9e-108">Parameters</span></span>

  - <span data-ttu-id="9aa9e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9aa9e-109">sesid</span></span>  
    <span data-ttu-id="9aa9e-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9aa9e-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9aa9e-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9aa9e-112">dbid</span></span>  
    <span data-ttu-id="9aa9e-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9aa9e-114">Base de données à fermer.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-114">The database to close.</span></span>

<!-- end list -->

  - <span data-ttu-id="9aa9e-115">grbit</span><span class="sxs-lookup"><span data-stu-id="9aa9e-115">grbit</span></span>  
    <span data-ttu-id="9aa9e-116">Type : [Microsoft. ISAM. esent. Interop. CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-116">Type: [Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9aa9e-117">Options de fermeture.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-117">Close options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9aa9e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aa9e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9aa9e-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9aa9e-119">Reference</span></span>

[<span data-ttu-id="9aa9e-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="9aa9e-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9aa9e-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="9aa9e-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9aa9e-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9aa9e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
