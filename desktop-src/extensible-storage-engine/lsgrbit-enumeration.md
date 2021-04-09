---
description: 'En savoir plus sur : énumération LsGrbit'
title: Énumération LsGrbit
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034049"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="f287c-103">Énumération LsGrbit</span><span class="sxs-lookup"><span data-stu-id="f287c-103">LsGrbit enumeration</span></span>

<span data-ttu-id="f287c-104">Options pour [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) et [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="f287c-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="f287c-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="f287c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f287c-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f287c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f287c-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f287c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f287c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f287c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="f287c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f287c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f287c-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f287c-110">Member name</span></span></th>
<th><span data-ttu-id="f287c-111">Description</span><span class="sxs-lookup"><span data-stu-id="f287c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f287c-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="f287c-112">None</span></span></td>
<td><span data-ttu-id="f287c-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="f287c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f287c-114">Réinitialiser</span><span class="sxs-lookup"><span data-stu-id="f287c-114">Reset</span></span></td>
<td><span data-ttu-id="f287c-115">Le descripteur de contexte de l’objet choisi doit être réinitialisé à JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="f287c-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f287c-116">Curseur</span><span class="sxs-lookup"><span data-stu-id="f287c-116">Cursor</span></span></td>
<td><span data-ttu-id="f287c-117">Spécifie que le handle de contexte doit être associé au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="f287c-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f287c-118">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="f287c-118">Table</span></span></td>
<td><span data-ttu-id="f287c-119">Spécifie que le descripteur de contexte doit être associé à la table associée au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="f287c-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="f287c-120">Il est interdit d’utiliser cette option avec le curseur.</span><span class="sxs-lookup"><span data-stu-id="f287c-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f287c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f287c-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f287c-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f287c-122">Reference</span></span>

[<span data-ttu-id="f287c-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f287c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
