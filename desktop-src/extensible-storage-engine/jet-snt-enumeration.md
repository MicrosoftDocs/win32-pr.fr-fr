---
description: 'En savoir plus sur : énumération JET_SNT'
title: Énumération JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515606"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="6c514-103">Énumération JET_SNT</span><span class="sxs-lookup"><span data-stu-id="6c514-103">JET_SNT enumeration</span></span>

<span data-ttu-id="6c514-104">Type de progression signalée.</span><span class="sxs-lookup"><span data-stu-id="6c514-104">Type of progress being reported.</span></span>

<span data-ttu-id="6c514-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c514-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c514-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c514-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c514-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c514-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="6c514-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6c514-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6c514-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="6c514-109">Member name</span></span></th>
<th><span data-ttu-id="6c514-110">Description</span><span class="sxs-lookup"><span data-stu-id="6c514-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6c514-111">Début</span><span class="sxs-lookup"><span data-stu-id="6c514-111">Begin</span></span></td>
<td><span data-ttu-id="6c514-112">Rappel pour le début d’une opération.</span><span class="sxs-lookup"><span data-stu-id="6c514-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6c514-113">Progress</span><span class="sxs-lookup"><span data-stu-id="6c514-113">Progress</span></span></td>
<td><span data-ttu-id="6c514-114">Rappel de la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6c514-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6c514-115">Terminé</span><span class="sxs-lookup"><span data-stu-id="6c514-115">Complete</span></span></td>
<td><span data-ttu-id="6c514-116">Rappel pour l’achèvement d’une opération.</span><span class="sxs-lookup"><span data-stu-id="6c514-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6c514-117">Échec</span><span class="sxs-lookup"><span data-stu-id="6c514-117">Fail</span></span></td>
<td><span data-ttu-id="6c514-118">Rappel de l’échec au cours de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6c514-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6c514-119">RecoveryStep</span><span class="sxs-lookup"><span data-stu-id="6c514-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="6c514-120">Rappel pour le contrôle de récupération.</span><span class="sxs-lookup"><span data-stu-id="6c514-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="6c514-121">Utilisé pour le traitement interne dans les versions du système d’exploitation Windows antérieures à Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c514-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="6c514-122">Cette valeur ne s’applique pas aux versions de Windows à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c514-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6c514-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c514-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c514-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6c514-124">Reference</span></span>

[<span data-ttu-id="6c514-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6c514-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
