---
description: 'En savoir plus sur : méthode API. TryMoveLast'
title: API. TryMoveLast, méthode
TOCTitle: 'TryMoveLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovelast(v=EXCHG.10)
ms:contentKeyID: 55100933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab1e0495d3fbea490f7b1be6cc67e45d97bc89d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115015"
---
# <a name="apitrymovelast-method"></a><span data-ttu-id="a81d4-103">API. TryMoveLast, méthode</span><span class="sxs-lookup"><span data-stu-id="a81d4-103">Api.TryMoveLast method</span></span>

<span data-ttu-id="a81d4-104">Essayez de vous déplacer vers le dernier enregistrement de la table.</span><span class="sxs-lookup"><span data-stu-id="a81d4-104">Try to move to the last record in the table.</span></span> <span data-ttu-id="a81d4-105">Si la table est vide, la valeur false est retournée. Si une autre erreur se produit, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="a81d4-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="a81d4-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a81d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a81d4-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a81d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a81d4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a81d4-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveLast(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a81d4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a81d4-109">Parameters</span></span>

  - <span data-ttu-id="a81d4-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a81d4-110">sesid</span></span>  
    <span data-ttu-id="a81d4-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a81d4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a81d4-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a81d4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a81d4-113">TableID</span><span class="sxs-lookup"><span data-stu-id="a81d4-113">tableid</span></span>  
    <span data-ttu-id="a81d4-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a81d4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a81d4-115">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="a81d4-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a81d4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a81d4-116">Return value</span></span>

<span data-ttu-id="a81d4-117">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a81d4-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a81d4-118">True si le déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="a81d4-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a81d4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a81d4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a81d4-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a81d4-120">Reference</span></span>

[<span data-ttu-id="a81d4-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="a81d4-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a81d4-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="a81d4-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a81d4-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a81d4-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
