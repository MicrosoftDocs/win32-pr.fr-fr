---
description: 'En savoir plus sur : énumération GetRecordSizeGrbit'
title: Énumération GetRecordSizeGrbit
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544744"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="fc35f-103">Énumération GetRecordSizeGrbit</span><span class="sxs-lookup"><span data-stu-id="fc35f-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="fc35f-104">Options pour [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="fc35f-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="fc35f-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="fc35f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="fc35f-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fc35f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fc35f-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fc35f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fc35f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc35f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="fc35f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fc35f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="fc35f-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="fc35f-110">Member name</span></span></th>
<th><span data-ttu-id="fc35f-111">Description</span><span class="sxs-lookup"><span data-stu-id="fc35f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fc35f-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="fc35f-112">None</span></span></td>
<td><span data-ttu-id="fc35f-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc35f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fc35f-114">InCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="fc35f-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="fc35f-115">Récupérez la taille de l’enregistrement qui se trouve dans le tampon de copie préparé ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fc35f-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="fc35f-116">Dans le cas contraire, l’TableID doit être positionné sur un enregistrement et cet enregistrement sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc35f-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fc35f-117">RunningTotal</span><span class="sxs-lookup"><span data-stu-id="fc35f-117">RunningTotal</span></span></td>
<td><span data-ttu-id="fc35f-118">Le JET_RECSIZE n’est pas mis à zéro avant de remplir le contenu, ce qui agit efficacement comme une accumulation des statistiques pour plusieurs enregistrements visités ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fc35f-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fc35f-119">Local</span><span class="sxs-lookup"><span data-stu-id="fc35f-119">Local</span></span></td>
<td><span data-ttu-id="fc35f-120">Ignore les valeurs longues non intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="fc35f-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="fc35f-121">Seul l’enregistrement local de la page sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc35f-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="fc35f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc35f-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc35f-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fc35f-123">Reference</span></span>

[<span data-ttu-id="fc35f-124">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fc35f-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
