---
description: 'En savoir plus sur : méthode API. TryGetLock'
title: API. TryGetLock, méthode
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ecd4e0e66226d438b4e5a78b2397f5637154096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210521"
---
# <a name="apitrygetlock-method"></a><span data-ttu-id="029f4-103">API. TryGetLock, méthode</span><span class="sxs-lookup"><span data-stu-id="029f4-103">Api.TryGetLock method</span></span>

<span data-ttu-id="029f4-104">Réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture.</span><span class="sxs-lookup"><span data-stu-id="029f4-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="029f4-105">Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes.</span><span class="sxs-lookup"><span data-stu-id="029f4-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="029f4-106">Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="029f4-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="029f4-107">Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante va être effectuée.</span><span class="sxs-lookup"><span data-stu-id="029f4-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="029f4-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="029f4-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="029f4-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="029f4-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="029f4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="029f4-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="029f4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="029f4-111">Parameters</span></span>

  - <span data-ttu-id="029f4-112">sesid</span><span class="sxs-lookup"><span data-stu-id="029f4-112">sesid</span></span>  
    <span data-ttu-id="029f4-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="029f4-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="029f4-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="029f4-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="029f4-115">TableID</span><span class="sxs-lookup"><span data-stu-id="029f4-115">tableid</span></span>  
    <span data-ttu-id="029f4-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="029f4-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="029f4-117">Curseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="029f4-117">The cursor to use.</span></span> <span data-ttu-id="029f4-118">Un verrou sera acquis sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="029f4-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="029f4-119">grbit</span><span class="sxs-lookup"><span data-stu-id="029f4-119">grbit</span></span>  
    <span data-ttu-id="029f4-120">Type : [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="029f4-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="029f4-121">Options de verrouillage, utilisez cette option pour spécifier le type de verrou à obtenir.</span><span class="sxs-lookup"><span data-stu-id="029f4-121">Lock options, use this to specify which type of lock to obtain.</span></span>

#### <a name="return-value"></a><span data-ttu-id="029f4-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="029f4-122">Return value</span></span>

<span data-ttu-id="029f4-123">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="029f4-123">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="029f4-124">True si le verrou a été obtenu ; sinon, false.</span><span class="sxs-lookup"><span data-stu-id="029f4-124">True if the lock was obtained, false otherwise.</span></span> <span data-ttu-id="029f4-125">Une exception est levée si une erreur inattendue est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="029f4-125">An exception is thrown if an unexpected error is encountered.</span></span>  

## <a name="see-also"></a><span data-ttu-id="029f4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="029f4-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="029f4-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="029f4-127">Reference</span></span>

[<span data-ttu-id="029f4-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="029f4-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="029f4-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="029f4-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="029f4-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="029f4-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
