---
description: 'En savoir plus sur : méthode API. SetColumns'
title: API. SetColumns, méthode
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749476"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="b5e6c-103">API. SetColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="b5e6c-103">Api.SetColumns method</span></span>

<span data-ttu-id="b5e6c-104">Définit des colonnes à partir d’objets ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="b5e6c-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="b5e6c-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5e6c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5e6c-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5e6c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e6c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5e6c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="b5e6c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5e6c-108">Parameters</span></span>

  - <span data-ttu-id="b5e6c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b5e6c-109">sesid</span></span>  
    <span data-ttu-id="b5e6c-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5e6c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b5e6c-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5e6c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5e6c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b5e6c-112">tableid</span></span>  
    <span data-ttu-id="b5e6c-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5e6c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b5e6c-114">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="b5e6c-114">The cursor to update.</span></span> <span data-ttu-id="b5e6c-115">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="b5e6c-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5e6c-116">values</span><span class="sxs-lookup"><span data-stu-id="b5e6c-116">values</span></span>  
    <span data-ttu-id="b5e6c-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="b5e6c-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="b5e6c-118">Valeurs à définir.</span><span class="sxs-lookup"><span data-stu-id="b5e6c-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5e6c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5e6c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5e6c-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b5e6c-120">Reference</span></span>

[<span data-ttu-id="b5e6c-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b5e6c-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b5e6c-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b5e6c-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b5e6c-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b5e6c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
