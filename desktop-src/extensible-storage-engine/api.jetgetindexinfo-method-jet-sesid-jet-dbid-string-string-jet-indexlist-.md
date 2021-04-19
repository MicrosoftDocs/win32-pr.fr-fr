---
description: 'En savoir plus sur : méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)'
title: Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515421"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="a0cb9-103">Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="a0cb9-104">**Remarque : cette API est désormais obsolète.**</span><span class="sxs-lookup"><span data-stu-id="a0cb9-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="a0cb9-105">Récupère des informations sur les index d’une table.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="a0cb9-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0cb9-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cb9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0cb9-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="a0cb9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0cb9-109">Parameters</span></span>

  - <span data-ttu-id="a0cb9-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a0cb9-110">sesid</span></span>  
    <span data-ttu-id="a0cb9-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a0cb9-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0cb9-113">dbid</span><span class="sxs-lookup"><span data-stu-id="a0cb9-113">dbid</span></span>  
    <span data-ttu-id="a0cb9-114">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a0cb9-115">Base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0cb9-116">tablename</span><span class="sxs-lookup"><span data-stu-id="a0cb9-116">tablename</span></span>  
    <span data-ttu-id="a0cb9-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a0cb9-118">Nom de la table sur laquelle récupérer les informations d’index.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0cb9-119">ignoré</span><span class="sxs-lookup"><span data-stu-id="a0cb9-119">ignored</span></span>  
    <span data-ttu-id="a0cb9-120">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a0cb9-121">Ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0cb9-122">indexlist</span><span class="sxs-lookup"><span data-stu-id="a0cb9-122">indexlist</span></span>  
    <span data-ttu-id="a0cb9-123">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="a0cb9-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="a0cb9-124">Renseigné avec des informations sur les index de la table.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0cb9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0cb9-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0cb9-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a0cb9-126">Reference</span></span>

[<span data-ttu-id="a0cb9-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="a0cb9-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a0cb9-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="a0cb9-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a0cb9-129">Surcharge JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a0cb9-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="a0cb9-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a0cb9-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
