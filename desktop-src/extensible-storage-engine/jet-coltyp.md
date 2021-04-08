---
description: 'En savoir plus sur : JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868065"
---
# <a name="jet_coltyp"></a><span data-ttu-id="df943-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="df943-103">JET_COLTYP</span></span>


<span data-ttu-id="df943-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="df943-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="df943-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="df943-105">JET_COLTYP</span></span>

<span data-ttu-id="df943-106">Le **JET_COLTYP** groupe de constantes décrit tous les types de colonne possibles qui se trouvent dans une table.</span><span class="sxs-lookup"><span data-stu-id="df943-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df943-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="df943-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="df943-108">Description</span><span class="sxs-lookup"><span data-stu-id="df943-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df943-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="df943-109">JET_coltypNil</span></span><br />
<span data-ttu-id="df943-110">0</span><span class="sxs-lookup"><span data-stu-id="df943-110">0</span></span></p></td>
<td><p><span data-ttu-id="df943-111">Type de colonne non valide.</span><span class="sxs-lookup"><span data-stu-id="df943-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="df943-112">JET_coltypBit</span></span><br />
<span data-ttu-id="df943-113">1</span><span class="sxs-lookup"><span data-stu-id="df943-113">1</span></span></p></td>
<td><p><span data-ttu-id="df943-114">Type de colonne qui autorise trois valeurs : <strong>true</strong>, <strong>false</strong>ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="df943-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="df943-115">Ce type de colonne est d’une longueur d’un octet et sa taille est fixe.</span><span class="sxs-lookup"><span data-stu-id="df943-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="df943-116"><strong>False</strong> trie avant <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="df943-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="df943-117">Notez que la taille de ce type ne correspond pas à la taille du type booléen variant.</span><span class="sxs-lookup"><span data-stu-id="df943-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="df943-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="df943-119">2</span><span class="sxs-lookup"><span data-stu-id="df943-119">2</span></span></p></td>
<td><p><span data-ttu-id="df943-120">Entier non signé sur 1 octet qui peut prendre des valeurs comprises entre 0 (zéro) et 255.</span><span class="sxs-lookup"><span data-stu-id="df943-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="df943-121">JET_coltypShort</span></span><br />
<span data-ttu-id="df943-122">3</span><span class="sxs-lookup"><span data-stu-id="df943-122">3</span></span></p></td>
<td><p><span data-ttu-id="df943-123">Entier signé sur 2 octets qui peut prendre des valeurs comprises entre-32768 et 32767.</span><span class="sxs-lookup"><span data-stu-id="df943-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="df943-124">Les valeurs négatives sont triées avant les valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="df943-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="df943-125">JET_coltypLong</span></span><br />
<span data-ttu-id="df943-126">4</span><span class="sxs-lookup"><span data-stu-id="df943-126">4</span></span></p></td>
<td><p><span data-ttu-id="df943-127">Entier signé sur 4 octets qui peut prendre des valeurs comprises entre-2147483648 et 2147483647.</span><span class="sxs-lookup"><span data-stu-id="df943-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="df943-128">Les valeurs négatives sont triées avant les valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="df943-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="df943-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="df943-130">5</span><span class="sxs-lookup"><span data-stu-id="df943-130">5</span></span></p></td>
<td><p><span data-ttu-id="df943-131">Entier signé de 8 octets qui peut prendre des valeurs comprises entre-9223372036854775808 et 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="df943-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="df943-132">Les valeurs négatives sont triées avant les valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="df943-132">Negative values sort before positive values.</span></span> <span data-ttu-id="df943-133">Ce type de colonne est identique au type de devise variant.</span><span class="sxs-lookup"><span data-stu-id="df943-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="df943-134">Ce type de colonne peut également être utilisé en tant qu’entier signé de 8 octets natif.</span><span class="sxs-lookup"><span data-stu-id="df943-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="df943-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="df943-136">6</span><span class="sxs-lookup"><span data-stu-id="df943-136">6</span></span></p></td>
<td><p><span data-ttu-id="df943-137">Nombre à virgule flottante simple précision (4 octets).</span><span class="sxs-lookup"><span data-stu-id="df943-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="df943-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="df943-139">7</span><span class="sxs-lookup"><span data-stu-id="df943-139">7</span></span></p></td>
<td><p><span data-ttu-id="df943-140">Nombre à virgule flottante double précision (8 octets).</span><span class="sxs-lookup"><span data-stu-id="df943-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="df943-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="df943-142">8</span><span class="sxs-lookup"><span data-stu-id="df943-142">8</span></span></p></td>
<td><p><span data-ttu-id="df943-143">Nombre à virgule flottante double précision (8 octets) qui représente une date en jours fractionnaires depuis l’année 1900.</span><span class="sxs-lookup"><span data-stu-id="df943-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="df943-144">Ce type de colonne est identique au type de date variant.</span><span class="sxs-lookup"><span data-stu-id="df943-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="df943-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="df943-146">9</span><span class="sxs-lookup"><span data-stu-id="df943-146">9</span></span></p></td>
<td><p><span data-ttu-id="df943-147">Colonne binaire fixe ou de longueur variable d’une longueur maximale de 255 octets.</span><span class="sxs-lookup"><span data-stu-id="df943-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="df943-148">Ce type de colonne peut être utilisé pour implémenter un GUID s’il est configuré en tant que colonne binaire de 16 octets de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="df943-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="df943-149">Le seul inconvénient est que l’ordre relatif des valeurs dans un index sur ce type de colonne ne correspond pas à l’ordre relatif du rendu de chaîne de Registre standard d’un GUID ( &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</span><span class="sxs-lookup"><span data-stu-id="df943-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="df943-150">JET_coltypText</span></span><br />
<span data-ttu-id="df943-151">10</span><span class="sxs-lookup"><span data-stu-id="df943-151">10</span></span></p></td>
<td><p><span data-ttu-id="df943-152">Colonne de texte de longueur fixe ou variable qui peut contenir jusqu’à 255 caractères ASCII ou 127 caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="df943-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="df943-153">Toutes les chaînes sont stockées sous la forme d’un nombre de caractères compté.</span><span class="sxs-lookup"><span data-stu-id="df943-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="df943-154">Les chaînes n’ont pas besoin d’être terminées par null.</span><span class="sxs-lookup"><span data-stu-id="df943-154">The strings need not be null terminated.</span></span> <span data-ttu-id="df943-155">En outre, il n’est pas nécessaire que le nombre inclue une marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="df943-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="df943-156">Enfin, les caractères null incorporés peuvent être stockés.</span><span class="sxs-lookup"><span data-stu-id="df943-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="df943-157">Les chaînes ASCII sont toujours traitées comme non sensibles à la casse à des fins de tri et de recherche.</span><span class="sxs-lookup"><span data-stu-id="df943-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="df943-158">En outre, seuls les caractères qui précèdent le premier caractère null (le cas échéant) sont pris en compte pour le tri et la recherche.</span><span class="sxs-lookup"><span data-stu-id="df943-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="df943-159">Les chaînes Unicode utilisent l’API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> pour créer des clés de tri qui sont ensuite utilisées pour le tri et la recherche de ces données.</span><span class="sxs-lookup"><span data-stu-id="df943-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="df943-160">Par défaut, les chaînes Unicode sont considérées comme étant dans les paramètres régionaux anglais (États-Unis) et sont triées et recherchées à l’aide des indicateurs de normalisation suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="df943-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="df943-161">Dans Windows 2000, il est possible de personnaliser ces indicateurs par index pour inclure également NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="df943-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="df943-162">Dans Windows XP et versions ultérieures, il est possible de demander n’importe quelle combinaison des indicateurs de normalisation suivants par index : LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH et SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="df943-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="df943-163">Dans toutes les versions, il est possible de personnaliser les paramètres régionaux par index.</span><span class="sxs-lookup"><span data-stu-id="df943-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="df943-164">Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df943-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="df943-165">Enfin, tous les caractères null rencontrés dans une chaîne Unicode sont complètement ignorés.</span><span class="sxs-lookup"><span data-stu-id="df943-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="df943-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="df943-167">11</span><span class="sxs-lookup"><span data-stu-id="df943-167">11</span></span></p></td>
<td><p><span data-ttu-id="df943-168">Colonne binaire fixe ou de longueur variable d’une longueur maximale de 2147483647 octets.</span><span class="sxs-lookup"><span data-stu-id="df943-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="df943-169">Ce type est considéré comme une valeur longue.</span><span class="sxs-lookup"><span data-stu-id="df943-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="df943-170">Une valeur long est spéciale, car elle peut être volumineuse et être accessible en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="df943-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="df943-171">Sinon, ce type est identique à JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="df943-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="df943-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="df943-173">12</span><span class="sxs-lookup"><span data-stu-id="df943-173">12</span></span></p></td>
<td><p><span data-ttu-id="df943-174">Colonne de texte de longueur fixe ou variable qui peut contenir jusqu’à 2147483647 caractères ASCII ou 1073741823 caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="df943-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="df943-175">Ce type est considéré comme une valeur longue.</span><span class="sxs-lookup"><span data-stu-id="df943-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="df943-176">Une valeur long est spéciale, car elle peut être volumineuse et être accessible en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="df943-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="df943-177">Sinon, ce type est identique à JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="df943-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="df943-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="df943-179">13</span><span class="sxs-lookup"><span data-stu-id="df943-179">13</span></span></p></td>
<td><p><span data-ttu-id="df943-180">Ce type de colonne est obsolète.</span><span class="sxs-lookup"><span data-stu-id="df943-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="df943-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="df943-182">14</span><span class="sxs-lookup"><span data-stu-id="df943-182">14</span></span></p></td>
<td><p><span data-ttu-id="df943-183">Entier non signé sur 4 octets qui peut prendre des valeurs comprises entre 0 (zéro) et 4294967295.</span><span class="sxs-lookup"><span data-stu-id="df943-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="df943-184"><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df943-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="df943-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="df943-186">15</span><span class="sxs-lookup"><span data-stu-id="df943-186">15</span></span></p></td>
<td><p><span data-ttu-id="df943-187">Entier signé de 8 octets qui peut prendre des valeurs comprises entre-9223372036854775808 et 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="df943-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="df943-188">Les valeurs négatives sont triées avant les valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="df943-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="df943-189"><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df943-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="df943-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="df943-191">16</span><span class="sxs-lookup"><span data-stu-id="df943-191">16</span></span></p></td>
<td><p><span data-ttu-id="df943-192">Colonne binaire de 16 octets de longueur fixe qui représente en mode natif le type de données GUID.</span><span class="sxs-lookup"><span data-stu-id="df943-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="df943-193">Les valeurs de colonne GUID sont triées de la même façon que les valeurs qui sont triées en tant que chaînes dans un format standard (par exemple, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span><span class="sxs-lookup"><span data-stu-id="df943-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="df943-194"><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df943-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="df943-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="df943-196">17</span><span class="sxs-lookup"><span data-stu-id="df943-196">17</span></span></p></td>
<td><p><span data-ttu-id="df943-197">Entier non signé sur 2 octets qui peut prendre des valeurs comprises entre 0 et 65535.</span><span class="sxs-lookup"><span data-stu-id="df943-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="df943-198"><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df943-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="df943-199">JET_coltypMax</span></span><br />
<span data-ttu-id="df943-200">18</span><span class="sxs-lookup"><span data-stu-id="df943-200">18</span></span></p></td>
<td><p><span data-ttu-id="df943-201">Constante décrivant le maximum (autrement dit, un au-delà du type de colonne valide le plus grand) pris en charge par le moteur.</span><span class="sxs-lookup"><span data-stu-id="df943-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="df943-202">Cette valeur doit être utilisée avec précaution, car elle changera à mesure que de nouveaux types de colonne seront pris en charge.</span><span class="sxs-lookup"><span data-stu-id="df943-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="df943-203">Par exemple, il a une valeur littérale différente sur Windows 2000 que sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df943-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="df943-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df943-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df943-205"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="df943-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="df943-206">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="df943-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df943-207"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="df943-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="df943-208">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="df943-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df943-209"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="df943-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="df943-210">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="df943-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="df943-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df943-211">See Also</span></span>

[<span data-ttu-id="df943-212">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="df943-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="df943-213">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="df943-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
