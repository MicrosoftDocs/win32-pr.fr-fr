---
description: 'En savoir plus sur : énumération SetCurrentIndexGrbit'
title: Énumération SetCurrentIndexGrbit
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513011"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="efe74-103">Énumération SetCurrentIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="efe74-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="efe74-104">Options pour [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) et [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="efe74-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="efe74-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="efe74-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="efe74-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="efe74-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="efe74-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="efe74-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="efe74-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe74-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="efe74-109">Membres</span><span class="sxs-lookup"><span data-stu-id="efe74-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="efe74-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="efe74-110">Member name</span></span></th>
<th><span data-ttu-id="efe74-111">Description</span><span class="sxs-lookup"><span data-stu-id="efe74-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efe74-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="efe74-112">None</span></span></td>
<td><span data-ttu-id="efe74-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="efe74-113">Default options.</span></span> <span data-ttu-id="efe74-114">Il est identique à MoveFirst.</span><span class="sxs-lookup"><span data-stu-id="efe74-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efe74-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="efe74-115">MoveFirst</span></span></td>
<td><span data-ttu-id="efe74-116">Indique que le curseur doit être positionné sur la première entrée de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="efe74-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="efe74-117">Si l’index actuel est sélectionné, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="efe74-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efe74-118">Nomove</span><span class="sxs-lookup"><span data-stu-id="efe74-118">NoMove</span></span></td>
<td><span data-ttu-id="efe74-119">Indique que le curseur doit être positionné sur l’entrée d’index du nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</span><span class="sxs-lookup"><span data-stu-id="efe74-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="efe74-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efe74-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="efe74-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="efe74-121">Reference</span></span>

[<span data-ttu-id="efe74-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="efe74-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
