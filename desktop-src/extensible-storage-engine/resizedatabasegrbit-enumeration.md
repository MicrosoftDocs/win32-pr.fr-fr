---
description: 'En savoir plus sur : énumération ResizeDatabaseGrbit'
title: Énumération ResizeDatabaseGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532124"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="82e20-103">Énumération ResizeDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="82e20-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="82e20-104">Options pour [JetResizeDatabase (JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="82e20-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="82e20-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="82e20-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="82e20-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82e20-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="82e20-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82e20-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82e20-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82e20-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="82e20-109">Membres</span><span class="sxs-lookup"><span data-stu-id="82e20-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="82e20-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="82e20-110">Member name</span></span></th>
<th><span data-ttu-id="82e20-111">Description</span><span class="sxs-lookup"><span data-stu-id="82e20-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82e20-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="82e20-112">None</span></span></td>
<td><span data-ttu-id="82e20-113">Aucune option.</span><span class="sxs-lookup"><span data-stu-id="82e20-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82e20-114">OnlyGrow</span><span class="sxs-lookup"><span data-stu-id="82e20-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="82e20-115">Développez uniquement la base de données.</span><span class="sxs-lookup"><span data-stu-id="82e20-115">Only grow the database.</span></span> <span data-ttu-id="82e20-116">Si l’appel Resize réduit la base de données, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="82e20-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="82e20-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82e20-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82e20-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="82e20-118">Reference</span></span>

[<span data-ttu-id="82e20-119">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="82e20-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
