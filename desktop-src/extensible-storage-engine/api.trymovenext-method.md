---
description: 'En savoir plus sur : méthode API. TryMoveNext'
title: API. TryMoveNext, méthode
TOCTitle: 'TryMoveNext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveNext(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovenext(v=EXCHG.10)
ms:contentKeyID: 55100887
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b4b4e1f296e5549ba3823f698cdcb5cc9f9f42a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112574"
---
# <a name="apitrymovenext-method"></a><span data-ttu-id="82714-103">API. TryMoveNext, méthode</span><span class="sxs-lookup"><span data-stu-id="82714-103">Api.TryMoveNext method</span></span>

<span data-ttu-id="82714-104">Essayez de vous déplacer vers l’enregistrement suivant dans la table.</span><span class="sxs-lookup"><span data-stu-id="82714-104">Try to move to the next record in the table.</span></span> <span data-ttu-id="82714-105">Si aucun enregistrement suivant n’est présent, la valeur false est retournée, si une erreur différente est rencontrée, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="82714-105">If there is not a next record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="82714-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82714-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82714-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82714-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82714-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82714-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveNext ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveNext(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveNext(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="82714-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82714-109">Parameters</span></span>

  - <span data-ttu-id="82714-110">sesid</span><span class="sxs-lookup"><span data-stu-id="82714-110">sesid</span></span>  
    <span data-ttu-id="82714-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82714-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="82714-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="82714-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="82714-113">TableID</span><span class="sxs-lookup"><span data-stu-id="82714-113">tableid</span></span>  
    <span data-ttu-id="82714-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82714-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="82714-115">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="82714-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="82714-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82714-116">Return value</span></span>

<span data-ttu-id="82714-117">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="82714-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="82714-118">True si le déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="82714-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82714-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82714-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82714-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="82714-120">Reference</span></span>

[<span data-ttu-id="82714-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="82714-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82714-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="82714-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82714-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82714-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
