---
description: 'En savoir plus sur : méthode API. JetGetDatabaseFileInfo (String, Int32, JET_DbInfo)'
title: API. JetGetDatabaseFileInfo, méthode (String, Int32, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100698
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a7d873d3688d6c18ff01a20c5e5c53809fbcdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514997"
---
# <a name="apijetgetdatabasefileinfo-method-string-int32-jet_dbinfo"></a><span data-ttu-id="6675d-103">API. JetGetDatabaseFileInfo, méthode (String, Int32, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="6675d-103">Api.JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)</span></span>

<span data-ttu-id="6675d-104">Récupère certaines informations sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6675d-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="6675d-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6675d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6675d-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6675d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6675d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6675d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="6675d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6675d-108">Parameters</span></span>

  - <span data-ttu-id="6675d-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="6675d-109">databaseName</span></span>  
    <span data-ttu-id="6675d-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6675d-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6675d-111">Nom de fichier de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6675d-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="6675d-112">value</span><span class="sxs-lookup"><span data-stu-id="6675d-112">value</span></span>  
    <span data-ttu-id="6675d-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6675d-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6675d-114">Valeur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6675d-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="6675d-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="6675d-115">infoLevel</span></span>  
    <span data-ttu-id="6675d-116">Type : [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6675d-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="6675d-117">Données spécifiques à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6675d-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="6675d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6675d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6675d-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6675d-119">Reference</span></span>

[<span data-ttu-id="6675d-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="6675d-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6675d-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="6675d-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6675d-122">Surcharge JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="6675d-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="6675d-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6675d-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
