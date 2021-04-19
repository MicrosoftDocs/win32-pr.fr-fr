---
description: 'En savoir plus sur : énumération ObjectInfoGrbit'
title: Énumération ObjectInfoGrbit
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519934"
---
# <a name="objectinfogrbit-enumeration"></a><span data-ttu-id="2c98c-103">Énumération ObjectInfoGrbit</span><span class="sxs-lookup"><span data-stu-id="2c98c-103">ObjectInfoGrbit enumeration</span></span>

<span data-ttu-id="2c98c-104">Options de table, utilisées dans [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="2c98c-104">Table options, used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="2c98c-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="2c98c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="2c98c-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2c98c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2c98c-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2c98c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2c98c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c98c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
```

## <a name="members"></a><span data-ttu-id="2c98c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2c98c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2c98c-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="2c98c-110">Member name</span></span></th>
<th><span data-ttu-id="2c98c-111">Description</span><span class="sxs-lookup"><span data-stu-id="2c98c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2c98c-112">Signet</span><span class="sxs-lookup"><span data-stu-id="2c98c-112">Bookmark</span></span></td>
<td><span data-ttu-id="2c98c-113">La table peut avoir des signets.</span><span class="sxs-lookup"><span data-stu-id="2c98c-113">The table can have bookmarks.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2c98c-114">Restauration</span><span class="sxs-lookup"><span data-stu-id="2c98c-114">Rollback</span></span></td>
<td><span data-ttu-id="2c98c-115">La table peut être restaurée.</span><span class="sxs-lookup"><span data-stu-id="2c98c-115">The table can be rolled back.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2c98c-116">Peut être mise à jour</span><span class="sxs-lookup"><span data-stu-id="2c98c-116">Updatable</span></span></td>
<td><span data-ttu-id="2c98c-117">La table peut être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2c98c-117">The table can be updated.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2c98c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c98c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c98c-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2c98c-119">Reference</span></span>

[<span data-ttu-id="2c98c-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2c98c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
