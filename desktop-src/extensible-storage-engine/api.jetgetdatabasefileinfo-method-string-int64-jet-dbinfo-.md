---
description: 'En savoir plus sur : méthode API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)'
title: API. JetGetDatabaseFileInfo, méthode (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
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
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112583"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="228d1-103">API. JetGetDatabaseFileInfo, méthode (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="228d1-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="228d1-104">Récupère certaines informations sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="228d1-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="228d1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="228d1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="228d1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="228d1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="228d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="228d1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="228d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="228d1-108">Parameters</span></span>

  - <span data-ttu-id="228d1-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="228d1-109">databaseName</span></span>  
    <span data-ttu-id="228d1-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="228d1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="228d1-111">Nom de fichier de la base de données.</span><span class="sxs-lookup"><span data-stu-id="228d1-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="228d1-112">value</span><span class="sxs-lookup"><span data-stu-id="228d1-112">value</span></span>  
    <span data-ttu-id="228d1-113">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="228d1-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="228d1-114">Valeur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="228d1-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="228d1-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="228d1-115">infoLevel</span></span>  
    <span data-ttu-id="228d1-116">Type : [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="228d1-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="228d1-117">Données spécifiques à récupérer.</span><span class="sxs-lookup"><span data-stu-id="228d1-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="228d1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="228d1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="228d1-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="228d1-119">Reference</span></span>

[<span data-ttu-id="228d1-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="228d1-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="228d1-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="228d1-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="228d1-122">Surcharge JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="228d1-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="228d1-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="228d1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
