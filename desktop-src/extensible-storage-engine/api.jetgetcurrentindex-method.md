---
description: 'En savoir plus sur : méthode API. JetGetCurrentIndex'
title: API. JetGetCurrentIndex, méthode
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513989"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="8c4ac-103">API. JetGetCurrentIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="8c4ac-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="8c4ac-104">Ddetermines : nom de l’index actuel d’un curseur donné.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="8c4ac-105">Ce nom est également utilisé pour resélectionner ultérieurement cet index comme index actuel à l’aide de [JetSetCurrentIndex (JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span><span class="sxs-lookup"><span data-stu-id="8c4ac-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="8c4ac-106">Elle peut également être utilisée pour découvrir les propriétés de cet index à l’aide de JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="8c4ac-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c4ac-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4ac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c4ac-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="8c4ac-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c4ac-110">Parameters</span></span>

  - <span data-ttu-id="8c4ac-111">sesid</span><span class="sxs-lookup"><span data-stu-id="8c4ac-111">sesid</span></span>  
    <span data-ttu-id="8c4ac-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8c4ac-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c4ac-114">TableID</span><span class="sxs-lookup"><span data-stu-id="8c4ac-114">tableid</span></span>  
    <span data-ttu-id="8c4ac-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8c4ac-116">Curseur pour lequel obtenir le nom d’index.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c4ac-117">indexName</span><span class="sxs-lookup"><span data-stu-id="8c4ac-117">indexName</span></span>  
    <span data-ttu-id="8c4ac-118">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8c4ac-119">Retourne le nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c4ac-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="8c4ac-120">maxNameLength</span></span>  
    <span data-ttu-id="8c4ac-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8c4ac-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8c4ac-122">Longueur maximale du nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-122">The maximum length of the index name.</span></span> <span data-ttu-id="8c4ac-123">Les noms d’index ne peuvent pas dépasser [NameMost](./systemparameters.namemost-field.md) caractères.</span><span class="sxs-lookup"><span data-stu-id="8c4ac-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c4ac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c4ac-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c4ac-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8c4ac-125">Reference</span></span>

[<span data-ttu-id="8c4ac-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="8c4ac-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8c4ac-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="8c4ac-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8c4ac-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8c4ac-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
