---
description: 'En savoir plus sur : structure JET_OBJECTLIST'
title: Structure JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319982"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="fa813-103">Structure JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="fa813-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="fa813-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fa813-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="fa813-105">Structure JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="fa813-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="fa813-106">La structure **JET_OBJECTLIST** parcourt une table temporaire qui a été créée avec [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="fa813-107">Chaque ligne de la table temporaire décrit un objet dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fa813-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="fa813-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fa813-108">Members</span></span>

<span data-ttu-id="fa813-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="fa813-109">**cbStruct**</span></span>

<span data-ttu-id="fa813-110">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="fa813-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="fa813-111">L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="fa813-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="fa813-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="fa813-112">**tableid**</span></span>

<span data-ttu-id="fa813-113">Identificateur de table de la table temporaire qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="fa813-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="fa813-114">L’appelant doit contenir le code qui va fermer la table.</span><span class="sxs-lookup"><span data-stu-id="fa813-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="fa813-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="fa813-115">**cRecord**</span></span>

<span data-ttu-id="fa813-116">Nombre d’enregistrements dans la table temporaire qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="fa813-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="fa813-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="fa813-117">**columnidcontainername**</span></span>

<span data-ttu-id="fa813-118">Identificateur de colonne du nom du type de conteneur.</span><span class="sxs-lookup"><span data-stu-id="fa813-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="fa813-119">Les seuls conteneurs actuellement pris en charge sont les tables.</span><span class="sxs-lookup"><span data-stu-id="fa813-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="fa813-120">Cette colonne est une [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="fa813-121">**columnidobjectname**</span></span>

<span data-ttu-id="fa813-122">Identificateur de colonne du nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa813-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="fa813-123">Cette colonne est une [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-124">**columnidobjtyp**</span><span class="sxs-lookup"><span data-stu-id="fa813-124">**columnidobjtyp**</span></span>

<span data-ttu-id="fa813-125">Identificateur de colonne du type de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa813-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="fa813-126">Les seuls conteneurs actuellement pris en charge sont des tables, ce qui signifie que ce champ sera JET_objtypTable.</span><span class="sxs-lookup"><span data-stu-id="fa813-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="fa813-127">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-128">**columniddtCreate**</span><span class="sxs-lookup"><span data-stu-id="fa813-128">**columniddtCreate**</span></span>

<span data-ttu-id="fa813-129">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="fa813-129">Obsolete.</span></span> <span data-ttu-id="fa813-130">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa813-130">Do not use.</span></span>

<span data-ttu-id="fa813-131">**columniddtUpdate**</span><span class="sxs-lookup"><span data-stu-id="fa813-131">**columniddtUpdate**</span></span>

<span data-ttu-id="fa813-132">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="fa813-132">Obsolete.</span></span> <span data-ttu-id="fa813-133">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa813-133">Do not use.</span></span>

<span data-ttu-id="fa813-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="fa813-134">**columnidgrbit**</span></span>

<span data-ttu-id="fa813-135">Identificateur de colonne des **grbits** applicables à l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa813-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="fa813-136">Pour obtenir la liste des **grbits** applicables, consultez [JET_TABLECREATE](./jet-tablecreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="fa813-137">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="fa813-138">**columnidflags**</span></span>

<span data-ttu-id="fa813-139">Identificateur de colonne des indicateurs applicables à l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa813-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="fa813-140">Pour obtenir la liste des indicateurs applicables, consultez [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="fa813-141">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-142">**columnidcRecord**</span><span class="sxs-lookup"><span data-stu-id="fa813-142">**columnidcRecord**</span></span>

<span data-ttu-id="fa813-143">Identificateur de colonne du nombre d’enregistrements qui sont présents dans la table nommée dans **columnidobjectname**.</span><span class="sxs-lookup"><span data-stu-id="fa813-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="fa813-144">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="fa813-145">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="fa813-145">**columnidcPage**</span></span>

<span data-ttu-id="fa813-146">Identificateur de colonne du nombre de pages que l’objet utilise.</span><span class="sxs-lookup"><span data-stu-id="fa813-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="fa813-147">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fa813-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="fa813-148">Notes</span><span class="sxs-lookup"><span data-stu-id="fa813-148">Remarks</span></span>

<span data-ttu-id="fa813-149">Chaque ligne de la table temporaire correspond à un objet dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fa813-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="fa813-150">Lorsque la table temporaire est créée avec le paramètre *InfoLevel* dans la fonction [JetGetObjectInfo](./jetgetobjectinfo-function.md) définie sur JET_ObjInfoListNoStats, les colonnes identifiées par **columnidcRecord** et **columnidcPage** ne contiennent pas d’informations significatives.</span><span class="sxs-lookup"><span data-stu-id="fa813-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="fa813-151">Actuellement, seules les informations sur les tables se trouvent dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="fa813-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="fa813-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa813-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa813-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fa813-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fa813-154">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="fa813-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa813-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fa813-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fa813-156">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fa813-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa813-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fa813-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fa813-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fa813-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fa813-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa813-159">See Also</span></span>

[<span data-ttu-id="fa813-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="fa813-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="fa813-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fa813-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="fa813-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fa813-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fa813-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fa813-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fa813-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fa813-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fa813-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fa813-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fa813-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fa813-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="fa813-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="fa813-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="fa813-168">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="fa813-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
