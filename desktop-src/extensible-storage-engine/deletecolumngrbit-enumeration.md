---
description: 'En savoir plus sur : énumération DeleteColumnGrbit'
title: Énumération DeleteColumnGrbit
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521427"
---
# <a name="deletecolumngrbit-enumeration"></a><span data-ttu-id="c7129-103">Énumération DeleteColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="c7129-103">DeleteColumnGrbit enumeration</span></span>

<span data-ttu-id="c7129-104">Options pour [JetDeleteColumn2 (JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span><span class="sxs-lookup"><span data-stu-id="c7129-104">Options for [JetDeleteColumn2(JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span></span>

<span data-ttu-id="c7129-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="c7129-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c7129-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7129-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7129-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7129-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7129-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7129-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
```

## <a name="members"></a><span data-ttu-id="c7129-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c7129-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c7129-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="c7129-110">Member name</span></span></th>
<th><span data-ttu-id="c7129-111">Description</span><span class="sxs-lookup"><span data-stu-id="c7129-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c7129-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="c7129-112">None</span></span></td>
<td><span data-ttu-id="c7129-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7129-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c7129-114">IgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="c7129-114">IgnoreTemplateColumns</span></span></td>
<td><span data-ttu-id="c7129-115">L’API doit uniquement tenter de supprimer des colonnes dans la table dérivée.</span><span class="sxs-lookup"><span data-stu-id="c7129-115">The API should only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="c7129-116">Si une colonne de ce nom existe dans la table de base, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="c7129-116">If a column of that name exists in the base table it will be ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c7129-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7129-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7129-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c7129-118">Reference</span></span>

[<span data-ttu-id="c7129-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c7129-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
