---
description: 'En savoir plus sur : énumération JET_cbtyp'
title: Énumération JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521425"
---
# <a name="jet_cbtyp-enumeration"></a><span data-ttu-id="69cdc-103">Énumération JET_cbtyp</span><span class="sxs-lookup"><span data-stu-id="69cdc-103">JET_cbtyp enumeration</span></span>

<span data-ttu-id="69cdc-104">Type de progression signalée.</span><span class="sxs-lookup"><span data-stu-id="69cdc-104">Type of progress being reported.</span></span>

<span data-ttu-id="69cdc-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="69cdc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="69cdc-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69cdc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69cdc-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69cdc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69cdc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69cdc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a><span data-ttu-id="69cdc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="69cdc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="69cdc-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="69cdc-110">Member name</span></span></th>
<th><span data-ttu-id="69cdc-111">Description</span><span class="sxs-lookup"><span data-stu-id="69cdc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-112">Null</span><span class="sxs-lookup"><span data-stu-id="69cdc-112">Null</span></span></td>
<td><span data-ttu-id="69cdc-113">Ce rappel est réservé et toujours considéré comme non valide.</span><span class="sxs-lookup"><span data-stu-id="69cdc-113">This callback is reserved and always considered invalid.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-114">Finalize</span><span class="sxs-lookup"><span data-stu-id="69cdc-114">Finalize</span></span></td>
<td><span data-ttu-id="69cdc-115">Une colonne finalisable est passée à zéro.</span><span class="sxs-lookup"><span data-stu-id="69cdc-115">A finalizable column has gone to zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-116">AvantInsertion</span><span class="sxs-lookup"><span data-stu-id="69cdc-116">BeforeInsert</span></span></td>
<td><span data-ttu-id="69cdc-117">Ce rappel se produit juste avant l’insertion d’un nouvel enregistrement dans une table par un appel à JetUpdate.</span><span class="sxs-lookup"><span data-stu-id="69cdc-117">This callback will occur just before a new record is inserted into a table by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-118">Évènement</span><span class="sxs-lookup"><span data-stu-id="69cdc-118">AfterInsert</span></span></td>
<td><span data-ttu-id="69cdc-119">Ce rappel se produit juste après l’insertion d’un nouvel enregistrement dans une table par un appel à JetUpdate mais avant le retour de JetUpdate.</span><span class="sxs-lookup"><span data-stu-id="69cdc-119">This callback will occur just after a new record has been inserted into a table by a call to JetUpdate but before JetUpdate returns.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-120">BeforeReplace</span><span class="sxs-lookup"><span data-stu-id="69cdc-120">BeforeReplace</span></span></td>
<td><span data-ttu-id="69cdc-121">Ce rappel se produit juste avant un enregistrement existant dans une table en cours de modification par un appel à JetUpdate.</span><span class="sxs-lookup"><span data-stu-id="69cdc-121">This callback will occur just prior to an existing record in a table being changed by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-122">AfterReplace</span><span class="sxs-lookup"><span data-stu-id="69cdc-122">AfterReplace</span></span></td>
<td><span data-ttu-id="69cdc-123">Ce rappel se produit juste après qu’un enregistrement existant dans une table a été modifié par un appel à JetUpdate mais avant le retour de JetUpdate.</span><span class="sxs-lookup"><span data-stu-id="69cdc-123">This callback will occur just after an existing record in a table has been changed by a call to JetUpdate but prior to JetUpdate returning.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-124">BeforeDelete</span><span class="sxs-lookup"><span data-stu-id="69cdc-124">BeforeDelete</span></span></td>
<td><span data-ttu-id="69cdc-125">Ce rappel se produit juste avant qu’un enregistrement existant dans une table ne soit supprimé par un appel à JetDelete.</span><span class="sxs-lookup"><span data-stu-id="69cdc-125">This callback will occur just before an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-126">AfterDelete</span><span class="sxs-lookup"><span data-stu-id="69cdc-126">AfterDelete</span></span></td>
<td><span data-ttu-id="69cdc-127">Ce rappel se produit juste après la suppression d’un enregistrement existant dans une table par un appel à JetDelete.</span><span class="sxs-lookup"><span data-stu-id="69cdc-127">This callback will occur just after an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-128">UserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="69cdc-128">UserDefinedDefaultValue</span></span></td>
<td><span data-ttu-id="69cdc-129">Ce rappel se produit lorsque le moteur doit récupérer la valeur par défaut définie par l’utilisateur d’une colonne à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="69cdc-129">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="69cdc-130">Ce rappel est essentiellement une implémentation limitée de JetRetrieveColumn qui est évaluée par l’application.</span><span class="sxs-lookup"><span data-stu-id="69cdc-130">This callback is essentially a limited implementation of JetRetrieveColumn that is evaluated by the application.</span></span> <span data-ttu-id="69cdc-131">Un maximum de valeur de colonne peut être retourné pour une valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69cdc-131">A maximum of one column value can be returned for a user defined default value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-132">OnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="69cdc-132">OnlineDefragCompleted</span></span></td>
<td><span data-ttu-id="69cdc-133">Ce rappel se produit lorsque la défragmentation en ligne d’une base de données telle qu’elle est lancée par JetDefragment s’est arrêtée en raison de l’exécution du processus ou de la limite de temps atteinte.</span><span class="sxs-lookup"><span data-stu-id="69cdc-133">This callback will occur when the online defragmentation of a database as initiated by JetDefragment has stopped due to either the process being completed or the time limit being reached.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cdc-134">FreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="69cdc-134">FreeCursorLS</span></span></td>
<td><span data-ttu-id="69cdc-135">Ce rappel se produit lorsque l’application doit nettoyer le descripteur de contexte pour le stockage local associé à un curseur libéré par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="69cdc-135">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="69cdc-136">Pour plus d’informations, consultez JetSetLS.</span><span class="sxs-lookup"><span data-stu-id="69cdc-136">For more information, see JetSetLS.</span></span> <span data-ttu-id="69cdc-137">Le délégué pour cette raison de rappel est configuré au moyen de JetSetSystemParameter avec JET_paramRuntimeCallback.</span><span class="sxs-lookup"><span data-stu-id="69cdc-137">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cdc-138">FreeTableLS</span><span class="sxs-lookup"><span data-stu-id="69cdc-138">FreeTableLS</span></span></td>
<td><span data-ttu-id="69cdc-139">Ce rappel se produit en raison de la nécessité pour l’application de nettoyer le descripteur de contexte pour le stockage local associé à une table qui est publiée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="69cdc-139">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="69cdc-140">Pour plus d’informations, consultez JetSetLS.</span><span class="sxs-lookup"><span data-stu-id="69cdc-140">For more information, see JetSetLS.</span></span> <span data-ttu-id="69cdc-141">Le délégué pour cette raison de rappel est configuré au moyen de JetSetSystemParameter avec JET_paramRuntimeCallback.</span><span class="sxs-lookup"><span data-stu-id="69cdc-141">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="69cdc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69cdc-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69cdc-143">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="69cdc-143">Reference</span></span>

[<span data-ttu-id="69cdc-144">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69cdc-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
