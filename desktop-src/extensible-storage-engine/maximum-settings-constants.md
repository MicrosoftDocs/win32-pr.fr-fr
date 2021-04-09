---
description: 'En savoir plus sur : constantes de paramètres maximum'
title: Nombre maximal de constantes de paramètres
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862890"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="f6ad7-103">Nombre maximal de constantes de paramètres</span><span class="sxs-lookup"><span data-stu-id="f6ad7-103">Maximum Settings Constants</span></span>


<span data-ttu-id="f6ad7-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f6ad7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="f6ad7-105">Nombre maximal de constantes de paramètres</span><span class="sxs-lookup"><span data-stu-id="f6ad7-105">Maximum Settings Constants</span></span>

<span data-ttu-id="f6ad7-106">Ces constantes fournissent les paramètres maximaux autorisés sur les éléments d’une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6ad7-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="f6ad7-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="f6ad7-108">Description</span><span class="sxs-lookup"><span data-stu-id="f6ad7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f6ad7-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="f6ad7-110">3</span><span class="sxs-lookup"><span data-stu-id="f6ad7-110">3</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-111">Définit la longueur du préfixe utilisé pour nommer les fichiers utilisés par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="f6ad7-112">Cette longueur s’applique au nom défini pour le paramètre système <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="f6ad7-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="f6ad7-114">15</span><span class="sxs-lookup"><span data-stu-id="f6ad7-114">15</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-115">Définit la longueur maximale de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="f6ad7-117">256</span><span class="sxs-lookup"><span data-stu-id="f6ad7-117">256</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-118">Taille maximale par défaut d’un signet.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="f6ad7-119">Cela est valide lorsque la taille de la clé reste la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="f6ad7-121">2000</span><span class="sxs-lookup"><span data-stu-id="f6ad7-121">2000</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-122">Taille maximale d’un signet quand esent est configuré pour avoir les plus grandes clés possibles.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="f6ad7-123"><strong>Windows 7 :</strong> JET_cbBookmarkMostMost est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="f6ad7-125">64</span><span class="sxs-lookup"><span data-stu-id="f6ad7-125">64</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-126">Longueur maximale d’un objet, d’une colonne, d’un index ou d’un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="f6ad7-127"><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 128.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="f6ad7-129">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-129">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-130">Longueur maximale d’une &quot; construction Name.Name.Name... &quot; .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="f6ad7-131"><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 510.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="f6ad7-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="f6ad7-133">82</span><span class="sxs-lookup"><span data-stu-id="f6ad7-133">82</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-134">Ce nombre peut être utilisé pour calculer la quantité maximale d’un objet BLOB qui peut être stocké par le moteur de base de données sur une page de base de données unique.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="f6ad7-135">La formule est Max Size = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="f6ad7-136">Cette valeur est désormais obsolète.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-136">This value is now obsolete.</span></span> <span data-ttu-id="f6ad7-137">La taille du segment de valeur longue doit être extraite avec le paramètre JET_paramLVChunkSizeMost.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="f6ad7-139">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-139">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-140">Taille maximale des données de colonne de valeur non longue.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="f6ad7-142">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-142">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-143">Taille maximale d’une colonne par défaut de valeur longue (LongBinary ou LongText).</span><span class="sxs-lookup"><span data-stu-id="f6ad7-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="f6ad7-145">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-145">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-146">Taille maximale par défaut d’une clé de tri ou d’index.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="f6ad7-148">2000</span><span class="sxs-lookup"><span data-stu-id="f6ad7-148">2000</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-149">Taille maximale configurable d’une clé de tri ou d’index pour toute taille de page.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="f6ad7-150">(Voir JET_INDEXCREATE2. cbKeyMost)</span><span class="sxs-lookup"><span data-stu-id="f6ad7-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="f6ad7-151"><strong>Windows 7 :</strong> JET_cbKeyMostMost est introduite dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="f6ad7-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="f6ad7-153">500</span><span class="sxs-lookup"><span data-stu-id="f6ad7-153">500</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-154">Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 2048 octets.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="f6ad7-155">Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="f6ad7-156"><strong>Windows Vista :</strong> JET_cbKeyMost2KBytePage est introduite dans le système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="f6ad7-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="f6ad7-158">1 000</span><span class="sxs-lookup"><span data-stu-id="f6ad7-158">1000</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-159">Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 4096 octets.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="f6ad7-160">Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="f6ad7-161"><strong>Windows Vista :</strong> JET_cbKeyMost4KBytePage est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="f6ad7-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="f6ad7-163">2000</span><span class="sxs-lookup"><span data-stu-id="f6ad7-163">2000</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-164">Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 8192 octets.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="f6ad7-165">Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="f6ad7-166"><strong>Windows Vista :  </strong> JET_cbKeyMost8KBytePage est introduit dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6ad7-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="f6ad7-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="f6ad7-168">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-168">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-169">Taille maximale autorisée minimale pour une clé d’index.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="f6ad7-170">Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="f6ad7-171"><strong>Windows Vista :  </strong> JET_cbKeyMostMin est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="f6ad7-173">256</span><span class="sxs-lookup"><span data-stu-id="f6ad7-173">256</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-174">Taille de clé maximale lorsque la clé est formée à l’aide d’un <em>Grbit</em>Limit, tel que JET_bitStrLimit, qui est utilisé dans la fonction <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="f6ad7-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="f6ad7-176">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-176">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-177">Taille maximale de l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-177">The maximum size of the primary index.</span></span> <span data-ttu-id="f6ad7-178">Cela est désormais obsolète.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="f6ad7-180">255</span><span class="sxs-lookup"><span data-stu-id="f6ad7-180">255</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-181">Taille maximale de l’index secondaire.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="f6ad7-182">Cela est désormais obsolète.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="f6ad7-184">12</span><span class="sxs-lookup"><span data-stu-id="f6ad7-184">12</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-185">Nombre maximal de composants dans une clé de tri ou d’index.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="f6ad7-186"><strong>Windows Vista :  </strong> Dans Windows Vista et les versions ultérieures de Windows, la valeur est 16.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-187">JET_ccolMost</span></span><br />
<span data-ttu-id="f6ad7-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="f6ad7-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-189">Nombre maximal de colonnes autorisées dans une table.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="f6ad7-190"><strong>Windows XP :  </strong> La valeur 0x0000fee0 est utilisée dans Windows XP et versions ultérieures et versions ultérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="f6ad7-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="f6ad7-191"><strong>Windows 2000 :  </strong> La valeur 0x00007ffe est utilisée dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="f6ad7-193">0x0000007F</span><span class="sxs-lookup"><span data-stu-id="f6ad7-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-194">Nombre maximal de colonnes fixes autorisées dans une table, actuellement 127.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="f6ad7-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f6ad7-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-197">Nombre maximal de colonnes de longueur variable qui peuvent être contenues dans une table, actuellement 128.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="f6ad7-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="f6ad7-199">(JET_ccolMost-0x000000FF)</span><span class="sxs-lookup"><span data-stu-id="f6ad7-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="f6ad7-200">Nombre maximal de colonnes avec balises pouvant être contenues dans une table, actuellement 64993.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f6ad7-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6ad7-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f6ad7-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ad7-203">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ad7-204"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f6ad7-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ad7-205">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ad7-206"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f6ad7-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ad7-207">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f6ad7-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

