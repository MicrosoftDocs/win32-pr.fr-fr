---
description: 'En savoir plus sur : énumération ObjectInfoFlags'
title: Énumération ObjectInfoFlags
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865622"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="898ed-103">Énumération ObjectInfoFlags</span><span class="sxs-lookup"><span data-stu-id="898ed-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="898ed-104">Indicateurs pour les objets ESENT (tables).</span><span class="sxs-lookup"><span data-stu-id="898ed-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="898ed-105">Utilisé dans [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="898ed-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="898ed-106">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="898ed-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="898ed-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="898ed-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="898ed-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="898ed-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="898ed-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="898ed-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="898ed-110">Membres</span><span class="sxs-lookup"><span data-stu-id="898ed-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="898ed-111">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="898ed-111">Member name</span></span></th>
<th><span data-ttu-id="898ed-112">Description</span><span class="sxs-lookup"><span data-stu-id="898ed-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="898ed-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="898ed-113">None</span></span></td>
<td><span data-ttu-id="898ed-114">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="898ed-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="898ed-115">Système</span><span class="sxs-lookup"><span data-stu-id="898ed-115">System</span></span></td>
<td><span data-ttu-id="898ed-116">L’objet est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="898ed-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="898ed-117">TableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="898ed-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="898ed-118">La DDL de la table est fixe.</span><span class="sxs-lookup"><span data-stu-id="898ed-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="898ed-119">TableTemplate</span><span class="sxs-lookup"><span data-stu-id="898ed-119">TableTemplate</span></span></td>
<td><span data-ttu-id="898ed-120">La DDL de la table peut être héritée.</span><span class="sxs-lookup"><span data-stu-id="898ed-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="898ed-121">TableDerived</span><span class="sxs-lookup"><span data-stu-id="898ed-121">TableDerived</span></span></td>
<td><span data-ttu-id="898ed-122">La DDL de la table est héritée d’une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="898ed-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="898ed-123">TableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="898ed-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="898ed-124">Colonnes fixes ou variables dans les tables dérivées (afin que les colonnes fixes ou variables puissent être ajoutées ultérieurement au modèle).</span><span class="sxs-lookup"><span data-stu-id="898ed-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="898ed-125">Utilisé conjointement avec TableTemplate.</span><span class="sxs-lookup"><span data-stu-id="898ed-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="898ed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="898ed-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="898ed-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="898ed-127">Reference</span></span>

[<span data-ttu-id="898ed-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="898ed-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
