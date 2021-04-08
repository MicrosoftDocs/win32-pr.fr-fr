---
description: 'En savoir plus sur : méthode API. JetGetLock'
title: API. JetGetLock, méthode
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862234"
---
# <a name="apijetgetlock-method"></a><span data-ttu-id="5cb0e-103">API. JetGetLock, méthode</span><span class="sxs-lookup"><span data-stu-id="5cb0e-103">Api.JetGetLock method</span></span>

<span data-ttu-id="5cb0e-104">Réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="5cb0e-105">Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="5cb0e-106">Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="5cb0e-107">Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante va être effectuée.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="5cb0e-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5cb0e-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5cb0e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb0e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cb0e-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5cb0e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cb0e-111">Parameters</span></span>

  - <span data-ttu-id="5cb0e-112">sesid</span><span class="sxs-lookup"><span data-stu-id="5cb0e-112">sesid</span></span>  
    <span data-ttu-id="5cb0e-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5cb0e-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5cb0e-115">TableID</span><span class="sxs-lookup"><span data-stu-id="5cb0e-115">tableid</span></span>  
    <span data-ttu-id="5cb0e-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0e-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5cb0e-117">Curseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-117">The cursor to use.</span></span> <span data-ttu-id="5cb0e-118">Un verrou sera acquis sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="5cb0e-119">grbit</span><span class="sxs-lookup"><span data-stu-id="5cb0e-119">grbit</span></span>  
    <span data-ttu-id="5cb0e-120">Type : [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0e-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5cb0e-121">Options de verrouillage, utilisez cette option pour spécifier le type de verrou à obtenir.</span><span class="sxs-lookup"><span data-stu-id="5cb0e-121">Lock options, use this to specify which type of lock to obtain.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cb0e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cb0e-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5cb0e-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5cb0e-123">Reference</span></span>

[<span data-ttu-id="5cb0e-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="5cb0e-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5cb0e-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="5cb0e-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5cb0e-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5cb0e-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
