---
description: 'En savoir plus sur : méthode API. RetrieveColumns'
title: API. RetrieveColumns, méthode
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524716"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="ebc14-103">API. RetrieveColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="ebc14-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="ebc14-104">Récupère des colonnes dans les objets ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="ebc14-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="ebc14-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebc14-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebc14-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebc14-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc14-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebc14-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="ebc14-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc14-108">Parameters</span></span>

  - <span data-ttu-id="ebc14-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ebc14-109">sesid</span></span>  
    <span data-ttu-id="ebc14-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ebc14-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ebc14-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ebc14-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebc14-112">TableID</span><span class="sxs-lookup"><span data-stu-id="ebc14-112">tableid</span></span>  
    <span data-ttu-id="ebc14-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ebc14-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ebc14-114">Le curseur récupère les données à partir de.</span><span class="sxs-lookup"><span data-stu-id="ebc14-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="ebc14-115">Le curseur doit être positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebc14-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebc14-116">values</span><span class="sxs-lookup"><span data-stu-id="ebc14-116">values</span></span>  
    <span data-ttu-id="ebc14-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="ebc14-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="ebc14-118">Valeurs à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ebc14-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebc14-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc14-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebc14-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ebc14-120">Reference</span></span>

[<span data-ttu-id="ebc14-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="ebc14-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ebc14-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="ebc14-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ebc14-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ebc14-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
