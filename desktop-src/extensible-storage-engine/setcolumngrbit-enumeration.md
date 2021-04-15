---
description: 'En savoir plus sur : énumération SetColumnGrbit'
title: Énumération SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485225"
---
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="efb2f-103">Énumération SetColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="efb2f-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="efb2f-104">Options pour JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="efb2f-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="efb2f-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="efb2f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="efb2f-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="efb2f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="efb2f-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="efb2f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="efb2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efb2f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a><span data-ttu-id="efb2f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="efb2f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="efb2f-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="efb2f-110">Member name</span></span></th>
<th><span data-ttu-id="efb2f-111">Description</span><span class="sxs-lookup"><span data-stu-id="efb2f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efb2f-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="efb2f-112">None</span></span></td>
<td><span data-ttu-id="efb2f-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="efb2f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efb2f-114">AppendLV</span><span class="sxs-lookup"><span data-stu-id="efb2f-114">AppendLV</span></span></td>
<td><span data-ttu-id="efb2f-115">Cette option est utilisée pour ajouter des données à une colonne de type JET_coltypLongText ou JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="efb2f-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="efb2f-116">Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant ibLongValue dans psetinfo.</span><span class="sxs-lookup"><span data-stu-id="efb2f-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="efb2f-117">Toutefois, il est plus simple d’utiliser ce Grbit dans la mesure où la taille de la valeur de colonne existante n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="efb2f-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efb2f-118">OverwriteLV</span><span class="sxs-lookup"><span data-stu-id="efb2f-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="efb2f-119">Cette option est utilisée pour remplacer la valeur de type long existante par les données qui viennent d’être fournies.</span><span class="sxs-lookup"><span data-stu-id="efb2f-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="efb2f-120">Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="efb2f-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efb2f-121">RevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="efb2f-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="efb2f-122">Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="efb2f-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="efb2f-123">Elle fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes.</span><span class="sxs-lookup"><span data-stu-id="efb2f-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="efb2f-124">Toutes les valeurs de colonnes existantes sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="efb2f-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efb2f-125">SeparateLV</span><span class="sxs-lookup"><span data-stu-id="efb2f-125">SeparateLV</span></span></td>
<td><span data-ttu-id="efb2f-126">Cette option est utilisée pour forcer une valeur longue, les colonnes de type JET_coltyp. LongText ou JET_coltyp. LongBinary, à stocker séparément du reste des données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efb2f-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="efb2f-127">Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes.</span><span class="sxs-lookup"><span data-stu-id="efb2f-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="efb2f-128">Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long.</span><span class="sxs-lookup"><span data-stu-id="efb2f-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="efb2f-129">Notez que les valeurs longues de 4 octets de taille inférieure ne peuvent pas être forcées à être séparées.</span><span class="sxs-lookup"><span data-stu-id="efb2f-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="efb2f-130">Dans ce cas, l’option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="efb2f-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efb2f-131">SizeLV</span><span class="sxs-lookup"><span data-stu-id="efb2f-131">SizeLV</span></span></td>
<td><span data-ttu-id="efb2f-132">Cette option est utilisée pour interpréter la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le ColumnID donné et, le cas échéant, le numéro de séquence dans psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="efb2f-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="efb2f-133">Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0.</span><span class="sxs-lookup"><span data-stu-id="efb2f-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="efb2f-134">Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</span><span class="sxs-lookup"><span data-stu-id="efb2f-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efb2f-135">UniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="efb2f-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="efb2f-136">Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes.</span><span class="sxs-lookup"><span data-stu-id="efb2f-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="efb2f-137">Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="efb2f-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="efb2f-138">Si cette option est spécifiée, AppendLV, OverwriteLV et SizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="efb2f-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efb2f-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="efb2f-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="efb2f-140">Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes.</span><span class="sxs-lookup"><span data-stu-id="efb2f-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="efb2f-141">Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="efb2f-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="efb2f-142">Si cette option est spécifiée, AppendLV, OverwriteLV et SizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="efb2f-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="efb2f-143">ZeroLength</span><span class="sxs-lookup"><span data-stu-id="efb2f-143">ZeroLength</span></span></td>
<td><span data-ttu-id="efb2f-144">Cette option est utilisée pour définir une valeur de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="efb2f-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="efb2f-145">Normalement, une valeur de colonne est définie sur NULL en passant un cbMax de 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="efb2f-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="efb2f-146">Toutefois, pour certains types, comme JET_coltyp. Texte, une valeur de colonne peut avoir une longueur de 0 (zéro) au lieu de NULL, et cette option est utilisée pour différencier les valeurs NULL et 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="efb2f-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="efb2f-147">IntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="efb2f-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="efb2f-148">Essayez de stocker les colonnes de valeur longue dans l’enregistrement, même si elles dépassent la taille de séparation par défaut.</span><span class="sxs-lookup"><span data-stu-id="efb2f-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="efb2f-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb2f-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="efb2f-150">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="efb2f-150">Reference</span></span>

[<span data-ttu-id="efb2f-151">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="efb2f-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="efb2f-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="efb2f-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="efb2f-153">Non compressé</span><span class="sxs-lookup"><span data-stu-id="efb2f-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
