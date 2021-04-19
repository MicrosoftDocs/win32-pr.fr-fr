---
description: 'En savoir plus sur : JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538712"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="a1605-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="a1605-103">JET_CBTYP</span></span>


<span data-ttu-id="a1605-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a1605-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="a1605-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="a1605-105">JET_CBTYP</span></span>

<span data-ttu-id="a1605-106">Le **JET_CBTYP** groupe de constantes décrit tous les points possibles d’une opération que le moteur de base de données notifiera à une application en appelant la fonction de rappel [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a1605-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="a1605-107">Le moteur de base de données passe une de ces constantes dans le paramètre *cbtyp* de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a1605-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="a1605-108">La signification des autres paramètres passés par le moteur de base de données dans cet appel dépend de la **JET_CBTYP** spécifique passée.</span><span class="sxs-lookup"><span data-stu-id="a1605-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="a1605-109">**Windows XP :**  Le **JET_CBTYP** groupe de constantes est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1605-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1605-110">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="a1605-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="a1605-111">Description</span><span class="sxs-lookup"><span data-stu-id="a1605-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1605-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="a1605-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="a1605-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1605-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="a1605-114">Ce rappel est réservé et toujours considéré comme non valide.</span><span class="sxs-lookup"><span data-stu-id="a1605-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="a1605-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="a1605-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a1605-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="a1605-117">Ce rappel est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a1605-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="a1605-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="a1605-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a1605-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="a1605-120">Ce rappel se produit juste avant l’insertion d’un nouvel enregistrement dans une table par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="a1605-121">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-122">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-123">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-124"><em>sesid</em>: session qui a l’enregistrement à insérer.</span><span class="sxs-lookup"><span data-stu-id="a1605-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-125"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à insérer.</span><span class="sxs-lookup"><span data-stu-id="a1605-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-126"><em>TableID</em>: curseur qui a préparé le nouvel enregistrement à insérer.</span><span class="sxs-lookup"><span data-stu-id="a1605-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="a1605-127">Il est important de noter que la valeur de toutes les colonnes de version ou d’incrémentation automatique peut être incorrecte pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="a1605-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="a1605-128"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-129"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-130"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-131"><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</span><span class="sxs-lookup"><span data-stu-id="a1605-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="a1605-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="a1605-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a1605-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="a1605-134">Ce rappel se produit juste après l’insertion d’un nouvel enregistrement dans une table par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a> mais avant que <a href="gg269288(v=exchg.10).md">JetUpdate</a> retourne à son appelant.</span><span class="sxs-lookup"><span data-stu-id="a1605-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="a1605-135">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-136">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-137">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-138"><em>sesid</em>: session qui a l’enregistrement qui vient d’être inséré.</span><span class="sxs-lookup"><span data-stu-id="a1605-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-139"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être inséré.</span><span class="sxs-lookup"><span data-stu-id="a1605-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-140"><em>TableID</em>: curseur sur la table dans lequel l’enregistrement qui vient d’être inséré.</span><span class="sxs-lookup"><span data-stu-id="a1605-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="a1605-141">Notez que le curseur est toujours positionné sur la même entrée d’index que dans le rappel Before Insert.</span><span class="sxs-lookup"><span data-stu-id="a1605-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="a1605-142">Notez que cette entrée d’index ne peut pas être associée à l’enregistrement en cours d’insertion.</span><span class="sxs-lookup"><span data-stu-id="a1605-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-143"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-144"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-145"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-146"><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="a1605-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="a1605-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a1605-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="a1605-149">Ce rappel se produit juste avant un enregistrement existant dans une table en cours de modification par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="a1605-150">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-151">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-152">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-153"><em>sesid</em>: session dont l’enregistrement doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="a1605-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="a1605-154"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à modifier.</span><span class="sxs-lookup"><span data-stu-id="a1605-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="a1605-155"><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement à modifier.</span><span class="sxs-lookup"><span data-stu-id="a1605-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="a1605-156">Il est important de noter que la valeur de toutes les colonnes de version ou d’incrémentation automatique peut être incorrecte pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="a1605-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="a1605-157"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-158"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-159"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-160"><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</span><span class="sxs-lookup"><span data-stu-id="a1605-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="a1605-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="a1605-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1605-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="a1605-163">Ce rappel se produit juste après qu’un enregistrement existant dans une table a été modifié par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a> mais avant le retour de <a href="gg269288(v=exchg.10).md">JetUpdate</a> à son appelant.</span><span class="sxs-lookup"><span data-stu-id="a1605-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="a1605-164">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-165">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-166">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-167"><em>sesid</em>: session qui a l’enregistrement qui vient d’être modifié.</span><span class="sxs-lookup"><span data-stu-id="a1605-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="a1605-168"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être modifié.</span><span class="sxs-lookup"><span data-stu-id="a1605-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="a1605-169"><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement qui vient d’être modifié.</span><span class="sxs-lookup"><span data-stu-id="a1605-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="a1605-170"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-171"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-172"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-173"><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="a1605-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="a1605-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a1605-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="a1605-176">Ce rappel se produit juste avant qu’un enregistrement existant dans une table ne soit supprimé par un appel à <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="a1605-177">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-178">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-179">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-180"><em>sesid</em>: session qui a l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a1605-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-181"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a1605-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-182"><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a1605-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-183"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-184"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-185"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-186"><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</span><span class="sxs-lookup"><span data-stu-id="a1605-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="a1605-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="a1605-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a1605-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="a1605-189">Ce rappel se produit juste après qu’un enregistrement existant dans une table a été supprimé par un appel à <a href="gg269315(v=exchg.10).md">JetDelete</a> mais avant que <a href="gg269315(v=exchg.10).md">JetDelete</a> retourne à son appelant.</span><span class="sxs-lookup"><span data-stu-id="a1605-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="a1605-190">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="a1605-191">Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-192">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-193"><em>sesid</em>: session qui a l’enregistrement qui vient d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="a1605-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-194"><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="a1605-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-195"><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement qui vient d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="a1605-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="a1605-196"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-197"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-198"><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1605-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-199"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="a1605-200">Si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a1605-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="a1605-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a1605-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="a1605-203">Ce rappel se produit lorsque le moteur doit récupérer la valeur par défaut définie par l’utilisateur d’une colonne à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="a1605-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="a1605-204">Ce rappel est essentiellement une implémentation limitée de <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> qui est évaluée par l’application.</span><span class="sxs-lookup"><span data-stu-id="a1605-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="a1605-205">Un maximum de valeur de colonne peut être retourné pour une valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a1605-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="a1605-206">Le pointeur de fonction pour cette raison de rappel est soit passé à <a href="gg294122(v=exchg.10).md">JetAddColumn</a> au moyen d’une structure de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , soit passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen d’une structure de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> dans une structure de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dans une structure de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="a1605-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="a1605-207">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-208"><em>sesid</em>: la session qui calcule la valeur par défaut définie par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a1605-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="a1605-209"><em>dbid</em>: ID de base de données de la table qui contient la valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a1605-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="a1605-210"><em>TableID</em>: curseur positionné sur l’enregistrement pour lequel la valeur par défaut définie par l’utilisateur est Récupérée</span><span class="sxs-lookup"><span data-stu-id="a1605-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="a1605-211"><em>pvArg1</em>: mémoire tampon de sortie pour la valeur par défaut définie par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a1605-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="a1605-212"><em>pvArg2</em>: en entrée, il s’agit de la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="a1605-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="a1605-213">En sortie, il s’agit de la taille réelle de la valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a1605-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="a1605-214">dans les deux cas, la taille est un entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a1605-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="a1605-215"><em>pvContext</em>: pointeur vers une mémoire tampon contenant les données utilisateur spécifiées dans la structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> lorsque la colonne a été créée ou null si aucun contexte n’a été fourni.</span><span class="sxs-lookup"><span data-stu-id="a1605-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="a1605-216"><em>ulUnused</em>: ID de colonne de la colonne pour laquelle la valeur par défaut définie par l’utilisateur est récupérée.</span><span class="sxs-lookup"><span data-stu-id="a1605-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="a1605-217">Si une erreur est retournée par le rappel, l’opération à l’origine du rappel échouera avec cette erreur.</span><span class="sxs-lookup"><span data-stu-id="a1605-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="a1605-218">Si JET_wrnBufferTruncated est retourné par le rappel, l’opération se poursuit, mais la valeur entière n’est pas récupérée pendant le rappel.</span><span class="sxs-lookup"><span data-stu-id="a1605-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="a1605-219">Si JET_wrnColumnNull est retourné par le rappel, l’opération se poursuit, mais la valeur par défaut définie par l’utilisateur pour la colonne est NULL.</span><span class="sxs-lookup"><span data-stu-id="a1605-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="a1605-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="a1605-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="a1605-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="a1605-222">Ce rappel se produit lorsque la défragmentation en ligne d’une base de données telle qu’elle est lancée par <a href="gg269317(v=exchg.10).md">JetDefragment</a> s’est arrêtée en raison de l’exécution du processus ou de la limite de temps atteinte.</span><span class="sxs-lookup"><span data-stu-id="a1605-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="a1605-223">Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="a1605-224">Pour plus d’informations, consultez <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="a1605-225">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-226"><em>sesid</em>: session utilisée pour effectuer une défragmentation en ligne de la base de données ou JET_sesidNil pour un fichier de streaming.</span><span class="sxs-lookup"><span data-stu-id="a1605-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="a1605-227"><em>dbid</em>: ID de base de données de la base de données en cours de défragmentation ou JET_dbidNil pour un fichier de streaming.</span><span class="sxs-lookup"><span data-stu-id="a1605-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="a1605-228"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-229"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-230"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-231"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-232"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="a1605-233">Si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="a1605-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="a1605-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="a1605-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="a1605-236">Ce rappel se produit lorsque l’application doit nettoyer le descripteur de contexte pour le stockage local associé à un curseur libéré par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a1605-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="a1605-237">Pour plus d’informations, consultez <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="a1605-238">Le pointeur de fonction pour cette raison de rappel est configuré au moyen de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-239">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-240"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-241"><em>dbid</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-242"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-243"><em>pvArg1</em>: descripteur de contexte défini à l’aide de <a href="gg269243(v=exchg.10).md">JetSetLS</a></span><span class="sxs-lookup"><span data-stu-id="a1605-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="a1605-244"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-245"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-246"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="a1605-247">Si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="a1605-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="a1605-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="a1605-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="a1605-250">Ce rappel se produit en raison de la nécessité pour l’application de nettoyer le descripteur de contexte pour le stockage local associé à une table qui est publiée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a1605-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="a1605-251">Pour plus d’informations, consultez <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="a1605-252">Le pointeur de fonction pour cette raison de rappel est configuré au moyen de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="a1605-253">Les paramètres de rappel auront les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1605-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a1605-254"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-255"><em>dbid</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-256"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="a1605-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="a1605-257"><em>pvArg1</em>: descripteur de contexte défini à l’aide de <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="a1605-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="a1605-258"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-259"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="a1605-260"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="a1605-261">Si une erreur est retournée par le rappel, elle sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="a1605-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a1605-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1605-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1605-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1605-264">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1605-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1605-265"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1605-266">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a1605-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1605-267"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a1605-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1605-268">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a1605-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a1605-269">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1605-269">See Also</span></span>

[<span data-ttu-id="a1605-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="a1605-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)
