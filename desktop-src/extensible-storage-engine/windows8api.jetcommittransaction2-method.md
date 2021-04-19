---
description: 'En savoir plus sur : méthode Windows8Api. JetCommitTransaction2'
title: Méthode Windows8Api. JetCommitTransaction2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531824"
---
# <a name="windows8apijetcommittransaction2-method"></a><span data-ttu-id="581b3-103">Méthode Windows8Api. JetCommitTransaction2</span><span class="sxs-lookup"><span data-stu-id="581b3-103">Windows8Api.JetCommitTransaction2 method</span></span>

<span data-ttu-id="581b3-104">Valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent.</span><span class="sxs-lookup"><span data-stu-id="581b3-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="581b3-105">Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="581b3-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="581b3-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="581b3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="581b3-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="581b3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="581b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="581b3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a><span data-ttu-id="581b3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="581b3-109">Parameters</span></span>

  - <span data-ttu-id="581b3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="581b3-110">sesid</span></span>  
    <span data-ttu-id="581b3-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="581b3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="581b3-112">Session pour laquelle valider la transaction.</span><span class="sxs-lookup"><span data-stu-id="581b3-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="581b3-113">grbit</span><span class="sxs-lookup"><span data-stu-id="581b3-113">grbit</span></span>  
    <span data-ttu-id="581b3-114">Type : [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="581b3-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="581b3-115">Options de validation.</span><span class="sxs-lookup"><span data-stu-id="581b3-115">Commit options.</span></span>

<!-- end list -->

  - <span data-ttu-id="581b3-116">durableCommit</span><span class="sxs-lookup"><span data-stu-id="581b3-116">durableCommit</span></span>  
    <span data-ttu-id="581b3-117">Type : [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="581b3-117">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="581b3-118">Durée de validation de la transaction paresseuse.</span><span class="sxs-lookup"><span data-stu-id="581b3-118">Duration to commit lazy transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="581b3-119">commitId</span><span class="sxs-lookup"><span data-stu-id="581b3-119">commitId</span></span>  
    <span data-ttu-id="581b3-120">Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="581b3-120">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="581b3-121">ID de validation associé à cet enregistrement de validation.</span><span class="sxs-lookup"><span data-stu-id="581b3-121">Commit-id associated with this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="581b3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="581b3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="581b3-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="581b3-123">Reference</span></span>

[<span data-ttu-id="581b3-124">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="581b3-124">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="581b3-125">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="581b3-125">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="581b3-126">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="581b3-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
