---
description: 'En savoir plus sur : énumération RollbackTransactionGrbit'
title: Énumération RollbackTransactionGrbit
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521218"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="ab927-103">Énumération RollbackTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="ab927-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="ab927-104">Options pour JetRollbackTransaction.</span><span class="sxs-lookup"><span data-stu-id="ab927-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="ab927-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="ab927-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ab927-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab927-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab927-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab927-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab927-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab927-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="ab927-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ab927-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ab927-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="ab927-110">Member name</span></span></th>
<th><span data-ttu-id="ab927-111">Description</span><span class="sxs-lookup"><span data-stu-id="ab927-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab927-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="ab927-112">None</span></span></td>
<td><span data-ttu-id="ab927-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab927-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab927-114">RollbackAll</span><span class="sxs-lookup"><span data-stu-id="ab927-114">RollbackAll</span></span></td>
<td><span data-ttu-id="ab927-115">Cette option demande que toutes les modifications apportées à l’état de la base de données au cours de tous les points d’enregistrement soient annulées.</span><span class="sxs-lookup"><span data-stu-id="ab927-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="ab927-116">Par conséquent, la session va quitter la transaction.</span><span class="sxs-lookup"><span data-stu-id="ab927-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ab927-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab927-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab927-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ab927-118">Reference</span></span>

[<span data-ttu-id="ab927-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ab927-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
