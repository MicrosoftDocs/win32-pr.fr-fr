---
description: 'En savoir plus sur : méthode API. JetDeleteIndex'
title: API. JetDeleteIndex, méthode
TOCTitle: 'JetDeleteIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeleteindex(v=EXCHG.10)
ms:contentKeyID: 55100682
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de04966aae4aee3f4ab7b14a846b898f55f887be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525635"
---
# <a name="apijetdeleteindex-method"></a><span data-ttu-id="0c0e1-103">API. JetDeleteIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="0c0e1-103">Api.JetDeleteIndex method</span></span>

<span data-ttu-id="0c0e1-104">Supprime un index d’une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-104">Deletes an index from a database table.</span></span>

<span data-ttu-id="0c0e1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c0e1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c0e1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetDeleteIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetDeleteIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="0c0e1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c0e1-108">Parameters</span></span>

  - <span data-ttu-id="0c0e1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0c0e1-109">sesid</span></span>  
    <span data-ttu-id="0c0e1-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0c0e1-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c0e1-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0c0e1-112">tableid</span></span>  
    <span data-ttu-id="0c0e1-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0c0e1-114">Curseur sur la table à partir duquel supprimer l’index.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-114">A cursor on the table to delete the index from.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c0e1-115">index</span><span class="sxs-lookup"><span data-stu-id="0c0e1-115">index</span></span>  
    <span data-ttu-id="0c0e1-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0c0e1-117">Nom de l’index à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-117">The name of the index to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c0e1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c0e1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c0e1-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0c0e1-119">Reference</span></span>

[<span data-ttu-id="0c0e1-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="0c0e1-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0c0e1-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="0c0e1-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0c0e1-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c0e1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
