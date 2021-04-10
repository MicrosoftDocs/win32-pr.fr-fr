---
description: 'En savoir plus sur : méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)'
title: Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Single)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100877
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e57a42a46b9247133c1427f3ae270645f6133523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111923"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-single"></a><span data-ttu-id="e7de2-103">Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</span><span class="sxs-lookup"><span data-stu-id="e7de2-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</span></span>

<span data-ttu-id="e7de2-104">Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e7de2-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="e7de2-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7de2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7de2-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7de2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7de2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7de2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Single _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As SingleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    float data
)
```

#### <a name="parameters"></a><span data-ttu-id="e7de2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7de2-108">Parameters</span></span>

  - <span data-ttu-id="e7de2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e7de2-109">sesid</span></span>  
    <span data-ttu-id="e7de2-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7de2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e7de2-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e7de2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7de2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e7de2-112">tableid</span></span>  
    <span data-ttu-id="e7de2-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7de2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e7de2-114">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="e7de2-114">The cursor to update.</span></span> <span data-ttu-id="e7de2-115">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="e7de2-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7de2-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e7de2-116">columnid</span></span>  
    <span data-ttu-id="e7de2-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7de2-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e7de2-118">ColumnID à définir.</span><span class="sxs-lookup"><span data-stu-id="e7de2-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7de2-119">data</span><span class="sxs-lookup"><span data-stu-id="e7de2-119">data</span></span>  
    <span data-ttu-id="e7de2-120">Type : [System. Single](/dotnet/api/system.single)</span><span class="sxs-lookup"><span data-stu-id="e7de2-120">Type: [System.Single](/dotnet/api/system.single)</span></span>  
    
    <span data-ttu-id="e7de2-121">Données à définir.</span><span class="sxs-lookup"><span data-stu-id="e7de2-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7de2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7de2-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7de2-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e7de2-123">Reference</span></span>

[<span data-ttu-id="e7de2-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e7de2-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e7de2-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e7de2-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e7de2-126">Surcharge SetColumn</span><span class="sxs-lookup"><span data-stu-id="e7de2-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="e7de2-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e7de2-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
