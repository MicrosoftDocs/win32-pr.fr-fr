---
description: 'En savoir plus sur : énumération TermGrbit'
title: Énumération TermGrbit
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759087"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="418e0-103">Énumération TermGrbit</span><span class="sxs-lookup"><span data-stu-id="418e0-103">TermGrbit enumeration</span></span>

<span data-ttu-id="418e0-104">Options pour [JetTerm2 (JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="418e0-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="418e0-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="418e0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="418e0-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="418e0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="418e0-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="418e0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="418e0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="418e0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="418e0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="418e0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="418e0-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="418e0-110">Member name</span></span></th>
<th><span data-ttu-id="418e0-111">Description</span><span class="sxs-lookup"><span data-stu-id="418e0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="418e0-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="418e0-112">None</span></span></td>
<td><span data-ttu-id="418e0-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="418e0-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="418e0-114">Terminé</span><span class="sxs-lookup"><span data-stu-id="418e0-114">Complete</span></span></td>
<td><span data-ttu-id="418e0-115">Demande que l’instance soit arrêtée proprement.</span><span class="sxs-lookup"><span data-stu-id="418e0-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="418e0-116">Tout travail de nettoyage facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est immédiatement effectué.</span><span class="sxs-lookup"><span data-stu-id="418e0-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="418e0-117">Changement</span><span class="sxs-lookup"><span data-stu-id="418e0-117">Abrupt</span></span></td>
<td><span data-ttu-id="418e0-118">Demande que l’instance soit arrêtée aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="418e0-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="418e0-119">Tout travail facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est abandonné.</span><span class="sxs-lookup"><span data-stu-id="418e0-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="418e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="418e0-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="418e0-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="418e0-121">Reference</span></span>

[<span data-ttu-id="418e0-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="418e0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="418e0-123">Dirt</span><span class="sxs-lookup"><span data-stu-id="418e0-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
