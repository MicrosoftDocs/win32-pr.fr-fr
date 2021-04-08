---
description: 'En savoir plus sur : structure JET_OBJECTINFO'
title: Structure JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034911"
---
# <a name="jet_objectinfo-structure"></a><span data-ttu-id="fbd8c-103">Structure JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fbd8c-103">JET_OBJECTINFO Structure</span></span>


<span data-ttu-id="fbd8c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fbd8c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectinfo-structure"></a><span data-ttu-id="fbd8c-105">Structure JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fbd8c-105">JET_OBJECTINFO Structure</span></span>

<span data-ttu-id="fbd8c-106">La structure **JET_OBJECTINFO** contient des informations sur un objet.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-106">The **JET_OBJECTINFO** structure holds information about an object.</span></span> <span data-ttu-id="fbd8c-107">Les tables sont les seuls types d’objets actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-107">Tables are the only object types that are currently supported.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a><span data-ttu-id="fbd8c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fbd8c-108">Members</span></span>

<span data-ttu-id="fbd8c-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-109">**cbStruct**</span></span>

<span data-ttu-id="fbd8c-110">Taille, en octets, de la structure **JET_OBJECTINFO** .</span><span class="sxs-lookup"><span data-stu-id="fbd8c-110">The size, in bytes, of the **JET_OBJECTINFO** structure.</span></span>

<span data-ttu-id="fbd8c-111">**objtyp**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-111">**objtyp**</span></span>

<span data-ttu-id="fbd8c-112">Contient le [JET_OBJTYP](./jet-objtyp.md) de la structure.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-112">Holds the [JET_OBJTYP](./jet-objtyp.md) of the structure.</span></span> <span data-ttu-id="fbd8c-113">Actuellement, seules les tables sont retournées (autrement dit, JET_objtypTable).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-113">Currently only tables will be returned (that is, JET_objtypTable).</span></span>

<span data-ttu-id="fbd8c-114">**dtCreate**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-114">**dtCreate**</span></span>

<span data-ttu-id="fbd8c-115">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-115">Obsolete.</span></span> <span data-ttu-id="fbd8c-116">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-116">Do not use.</span></span>

<span data-ttu-id="fbd8c-117">**dtUpdate**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-117">**dtUpdate**</span></span>

<span data-ttu-id="fbd8c-118">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-118">Obsolete.</span></span> <span data-ttu-id="fbd8c-119">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-119">Do not use.</span></span>

<span data-ttu-id="fbd8c-120">**grbit**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-120">**grbit**</span></span>

<span data-ttu-id="fbd8c-121">Groupe de bits qui contiennent les options disponibles pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-121">A group of bits that contain the options that are available for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbd8c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbd8c-122">Value</span></span></p></th>
<th><p><span data-ttu-id="fbd8c-123">Signification</span><span class="sxs-lookup"><span data-stu-id="fbd8c-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-124">JET_bitTableInfoBookmark</span><span class="sxs-lookup"><span data-stu-id="fbd8c-124">JET_bitTableInfoBookmark</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-125">La table peut avoir des signets.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-125">The table can have bookmarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbd8c-126">JET_bitTableInfoRollback</span><span class="sxs-lookup"><span data-stu-id="fbd8c-126">JET_bitTableInfoRollback</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-127">La table peut être restaurée.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-127">The table can be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-128">JET_bitTableInfoUpdatable</span><span class="sxs-lookup"><span data-stu-id="fbd8c-128">JET_bitTableInfoUpdatable</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-129">La table peut être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-129">The table can be updated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fbd8c-130">**flags**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-130">**flags**</span></span>

<span data-ttu-id="fbd8c-131">Champ de bits qui contient zéro, un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-131">A bit field that contains zero or more of the following flags.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbd8c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbd8c-132">Value</span></span></p></th>
<th><p><span data-ttu-id="fbd8c-133">Signification</span><span class="sxs-lookup"><span data-stu-id="fbd8c-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-134">JET_bitObjectSystem</span><span class="sxs-lookup"><span data-stu-id="fbd8c-134">JET_bitObjectSystem</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-135">La table est une table système et est réservée à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-135">The table is a System Table and is for internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbd8c-136">JET_bitObjectTableDerived</span><span class="sxs-lookup"><span data-stu-id="fbd8c-136">JET_bitObjectTableDerived</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-137">Table héritée DDL d’une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-137">The table inherited DDL from a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-138">JET_bitObjectTableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="fbd8c-138">JET_bitObjectTableFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-139">Le DDL pour la table ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-139">The DDL for the table cannot be modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbd8c-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="fbd8c-140">JET_bitObjectTableNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-141">Utilisé conjointement avec JET_bitObjectTableTemplate pour interdire les colonnes fixes ou variables dans les tables dérivées (afin que les colonnes fixes ou variables puissent être ajoutées ultérieurement au modèle).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-141">Used in conjunction with JET_bitObjectTableTemplate to disallow fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span></p>
<p><span data-ttu-id="fbd8c-142"><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-142"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-143">JET_bitObjectTableTemplate</span><span class="sxs-lookup"><span data-stu-id="fbd8c-143">JET_bitObjectTableTemplate</span></span></p></td>
<td><p><span data-ttu-id="fbd8c-144">La table est une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-144">The table is a template table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fbd8c-145">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-145">**cRecord**</span></span>

<span data-ttu-id="fbd8c-146">Nombre d’enregistrements dans la table.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-146">The number of records in the table.</span></span>

<span data-ttu-id="fbd8c-147">Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-147">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

<span data-ttu-id="fbd8c-148">**cPage**</span><span class="sxs-lookup"><span data-stu-id="fbd8c-148">**cPage**</span></span>

<span data-ttu-id="fbd8c-149">Nombre de pages utilisées par la table.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-149">The number of pages that are being used by the table.</span></span>

<span data-ttu-id="fbd8c-150">Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-150">This value is retrieved only if **JET_OBJECTINFO** was passed to [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="fbd8c-151">Notes</span><span class="sxs-lookup"><span data-stu-id="fbd8c-151">Remarks</span></span>

<span data-ttu-id="fbd8c-152">Une structure **JET_OBJECTINFOe** est remplie par un appel à [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo](./jetgettableinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-152">A **JET_OBJECTINFO** structure gets populated by a call to [JetGetObjectInfo](./jetgetobjectinfo-function.md) or [JetGetTableInfo](./jetgettableinfo-function.md).</span></span> <span data-ttu-id="fbd8c-153">Si l’appel d’API échoue, le contenu de la structure n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-153">If the API call does not succeed, the contents of the structure are undefined.</span></span>

<span data-ttu-id="fbd8c-154">Le cas échéant, les statistiques de table incluent le nombre d’enregistrements et le nombre de pages qui se trouvent dans l’index cluster (autrement dit, l’index contenant les données de l’enregistrement).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-154">If applicable, the table statistics include the number of records and the number of pages that are in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="fbd8c-155">Les statistiques d’index sont accessibles séparément par nom, à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbd8c-155">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="fbd8c-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbd8c-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fbd8c-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fbd8c-158">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbd8c-159"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fbd8c-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fbd8c-160">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbd8c-161"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fbd8c-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fbd8c-162">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fbd8c-162">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fbd8c-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbd8c-163">See Also</span></span>

[<span data-ttu-id="fbd8c-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fbd8c-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fbd8c-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fbd8c-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fbd8c-166">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="fbd8c-166">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="fbd8c-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fbd8c-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fbd8c-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fbd8c-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fbd8c-169">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="fbd8c-169">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="fbd8c-170">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="fbd8c-170">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="fbd8c-171">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="fbd8c-171">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="fbd8c-172">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="fbd8c-172">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
