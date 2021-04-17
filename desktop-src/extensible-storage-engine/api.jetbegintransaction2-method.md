---
description: 'En savoir plus sur : méthode API. JetBeginTransaction2'
title: API. JetBeginTransaction2, méthode
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524772"
---
# <a name="apijetbegintransaction2-method"></a><span data-ttu-id="10498-103">API. JetBeginTransaction2, méthode</span><span class="sxs-lookup"><span data-stu-id="10498-103">Api.JetBeginTransaction2 method</span></span>

<span data-ttu-id="10498-104">Fait en sorte qu’une session entre dans une transaction ou crée un nouveau point d’enregistrement dans une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="10498-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="10498-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10498-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10498-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10498-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10498-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10498-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="10498-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10498-108">Parameters</span></span>

  - <span data-ttu-id="10498-109">sesid</span><span class="sxs-lookup"><span data-stu-id="10498-109">sesid</span></span>  
    <span data-ttu-id="10498-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="10498-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="10498-111">Session pour laquelle commencer la transaction.</span><span class="sxs-lookup"><span data-stu-id="10498-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="10498-112">grbit</span><span class="sxs-lookup"><span data-stu-id="10498-112">grbit</span></span>  
    <span data-ttu-id="10498-113">Type : [Microsoft. ISAM. esent. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="10498-113">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="10498-114">Options de transaction.</span><span class="sxs-lookup"><span data-stu-id="10498-114">Transaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="10498-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10498-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10498-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="10498-116">Reference</span></span>

[<span data-ttu-id="10498-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="10498-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="10498-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="10498-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="10498-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="10498-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
