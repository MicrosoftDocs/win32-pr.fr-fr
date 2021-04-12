---
description: 'En savoir plus sur : méthode API. JetRollback'
title: API. JetRollback, méthode
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318198"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="dac9c-103">API. JetRollback, méthode</span><span class="sxs-lookup"><span data-stu-id="dac9c-103">Api.JetRollback method</span></span>

<span data-ttu-id="dac9c-104">Annule les modifications apportées à l’état de la base de données et retourne au dernier point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dac9c-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="dac9c-105">JetRollback ferme également tous les curseurs ouverts pendant le point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dac9c-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="dac9c-106">Si le point d’enregistrement le plus à l’extérieur est annulé, la session va quitter la transaction.</span><span class="sxs-lookup"><span data-stu-id="dac9c-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="dac9c-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dac9c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dac9c-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dac9c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dac9c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac9c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dac9c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac9c-110">Parameters</span></span>

  - <span data-ttu-id="dac9c-111">sesid</span><span class="sxs-lookup"><span data-stu-id="dac9c-111">sesid</span></span>  
    <span data-ttu-id="dac9c-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dac9c-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dac9c-113">Session pour laquelle la transaction doit être restaurée.</span><span class="sxs-lookup"><span data-stu-id="dac9c-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="dac9c-114">grbit</span><span class="sxs-lookup"><span data-stu-id="dac9c-114">grbit</span></span>  
    <span data-ttu-id="dac9c-115">Type : [Microsoft. ISAM. esent. Interop. RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dac9c-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dac9c-116">Options de restauration.</span><span class="sxs-lookup"><span data-stu-id="dac9c-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="dac9c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac9c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dac9c-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="dac9c-118">Reference</span></span>

[<span data-ttu-id="dac9c-119">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="dac9c-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dac9c-120">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="dac9c-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dac9c-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dac9c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
