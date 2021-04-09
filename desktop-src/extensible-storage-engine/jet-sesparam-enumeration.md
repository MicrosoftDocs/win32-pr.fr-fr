---
description: 'En savoir plus sur : énumération JET_sesparam'
title: Énumération JET_sesparam (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112534"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="8aa00-103">Énumération JET_sesparam</span><span class="sxs-lookup"><span data-stu-id="8aa00-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="8aa00-104">Paramètres de session ESENT.</span><span class="sxs-lookup"><span data-stu-id="8aa00-104">ESENT session parameters.</span></span>

<span data-ttu-id="8aa00-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8aa00-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8aa00-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8aa00-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa00-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8aa00-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="8aa00-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8aa00-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8aa00-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="8aa00-109">Member name</span></span></th>
<th><span data-ttu-id="8aa00-110">Description</span><span class="sxs-lookup"><span data-stu-id="8aa00-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8aa00-111">Base</span><span class="sxs-lookup"><span data-stu-id="8aa00-111">Base</span></span></td>
<td><span data-ttu-id="8aa00-112">Ce paramètre n’est pas destiné à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="8aa00-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8aa00-113">CommitDefault</span><span class="sxs-lookup"><span data-stu-id="8aa00-113">CommitDefault</span></span></td>
<td><span data-ttu-id="8aa00-114">Ce paramètre définit grbits pour la validation.</span><span class="sxs-lookup"><span data-stu-id="8aa00-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="8aa00-115">Il fonctionne de la même façon que le paramètre système JET_param. CommitDefault lorsqu’il est utilisé avec une instance et un sesid.</span><span class="sxs-lookup"><span data-stu-id="8aa00-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8aa00-116">CommitGenericContext</span><span class="sxs-lookup"><span data-stu-id="8aa00-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="8aa00-117">Ce paramètre définit un contexte de validation spécifique à l’utilisateur qui sera placé dans le journal des transactions lors de la validation au niveau 0.</span><span class="sxs-lookup"><span data-stu-id="8aa00-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8aa00-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aa00-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8aa00-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8aa00-119">Reference</span></span>

[<span data-ttu-id="8aa00-120">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="8aa00-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
