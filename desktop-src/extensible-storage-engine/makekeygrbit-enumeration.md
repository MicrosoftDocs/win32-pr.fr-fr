---
description: 'En savoir plus sur : énumération MakeKeyGrbit'
title: Énumération MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112510"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="c56cf-103">Énumération MakeKeyGrbit</span><span class="sxs-lookup"><span data-stu-id="c56cf-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="c56cf-104">Options pour JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="c56cf-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="c56cf-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="c56cf-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c56cf-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c56cf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c56cf-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c56cf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c56cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c56cf-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="c56cf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c56cf-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c56cf-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="c56cf-110">Member name</span></span></th>
<th><span data-ttu-id="c56cf-111">Description</span><span class="sxs-lookup"><span data-stu-id="c56cf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c56cf-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="c56cf-112">None</span></span></td>
<td><span data-ttu-id="c56cf-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="c56cf-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c56cf-114">NewKey</span><span class="sxs-lookup"><span data-stu-id="c56cf-114">NewKey</span></span></td>
<td><span data-ttu-id="c56cf-115">Une nouvelle clé de recherche doit être construite.</span><span class="sxs-lookup"><span data-stu-id="c56cf-115">A new search key should be constructed.</span></span> <span data-ttu-id="c56cf-116">Toute clé de recherche existante est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c56cf-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c56cf-117">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="c56cf-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="c56cf-118">Quand cette option est spécifiée, toutes les autres options sont ignorées, toute clé de recherche précédemment existante est ignorée et le contenu de la mémoire tampon d’entrée est chargé en tant que nouvelle clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="c56cf-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c56cf-119">KeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="c56cf-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="c56cf-120">Si la taille de la mémoire tampon d’entrée est égale à zéro et que la colonne clé actuelle est une colonne de longueur variable, cette option indique que la mémoire tampon d’entrée contient une valeur de longueur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c56cf-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="c56cf-121">Dans le cas contraire, une taille de mémoire tampon d’entrée égale à zéro indiquerait une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="c56cf-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c56cf-122">StrLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-122">StrLimit</span></span></td>
<td><span data-ttu-id="c56cf-123">Cette option indique que la clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c56cf-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="c56cf-125">Cette option indique que la clé de recherche doit être construite de manière à ce que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c56cf-126">FullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="c56cf-127">La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c56cf-128">FullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="c56cf-129">La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c56cf-130">PartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="c56cf-131">La clé de recherche doit être construite de telle sorte que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c56cf-132">PartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="c56cf-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="c56cf-133">La clé de recherche doit être construite de telle sorte que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="c56cf-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c56cf-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c56cf-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c56cf-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c56cf-135">Reference</span></span>

[<span data-ttu-id="c56cf-136">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c56cf-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
