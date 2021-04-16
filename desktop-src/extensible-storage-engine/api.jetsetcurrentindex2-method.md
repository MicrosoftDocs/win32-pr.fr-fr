---
description: 'En savoir plus sur : méthode API. JetSetCurrentIndex2'
title: API. JetSetCurrentIndex2, méthode
TOCTitle: 'JetSetCurrentIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex2(v=EXCHG.10)
ms:contentKeyID: 55100798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e08e1fe5027641348259381d74b34ce16b034e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393484"
---
# <a name="apijetsetcurrentindex2-method"></a><span data-ttu-id="4a9e7-103">API. JetSetCurrentIndex2, méthode</span><span class="sxs-lookup"><span data-stu-id="4a9e7-103">Api.JetSetCurrentIndex2 method</span></span>

<span data-ttu-id="4a9e7-104">Définit l’index actuel d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="4a9e7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a9e7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9e7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a9e7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbitApi.JetSetCurrentIndex2(sesid, _
    tableid, index, grbit)
```

``` csharp
public static void JetSetCurrentIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4a9e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a9e7-108">Parameters</span></span>

  - <span data-ttu-id="4a9e7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4a9e7-109">sesid</span></span>  
    <span data-ttu-id="4a9e7-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4a9e7-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9e7-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4a9e7-112">tableid</span></span>  
    <span data-ttu-id="4a9e7-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4a9e7-114">Curseur sur lequel définir l’index.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9e7-115">index</span><span class="sxs-lookup"><span data-stu-id="4a9e7-115">index</span></span>  
    <span data-ttu-id="4a9e7-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4a9e7-117">Nom de l’index à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-117">The name of the index to be selected.</span></span> <span data-ttu-id="4a9e7-118">Si la valeur est null ou vide, l’index primaire est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9e7-119">grbit</span><span class="sxs-lookup"><span data-stu-id="4a9e7-119">grbit</span></span>  
    <span data-ttu-id="4a9e7-120">Type : [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4a9e7-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4a9e7-121">Définissez les options d’index.</span><span class="sxs-lookup"><span data-stu-id="4a9e7-121">Set index options.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a9e7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a9e7-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a9e7-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4a9e7-123">Reference</span></span>

[<span data-ttu-id="4a9e7-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="4a9e7-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4a9e7-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="4a9e7-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4a9e7-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4a9e7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
