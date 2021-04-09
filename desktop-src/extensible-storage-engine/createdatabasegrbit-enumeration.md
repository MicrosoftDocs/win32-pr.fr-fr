---
description: 'En savoir plus sur : énumération CreateDatabaseGrbit'
title: Énumération CreateDatabaseGrbit
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034110"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="4cd98-103">Énumération CreateDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="4cd98-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="4cd98-104">Options pour [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="4cd98-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="4cd98-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="4cd98-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="4cd98-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4cd98-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4cd98-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4cd98-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd98-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cd98-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="4cd98-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4cd98-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4cd98-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="4cd98-110">Member name</span></span></th>
<th><span data-ttu-id="4cd98-111">Description</span><span class="sxs-lookup"><span data-stu-id="4cd98-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4cd98-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="4cd98-112">None</span></span></td>
<td><span data-ttu-id="4cd98-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cd98-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4cd98-114">OverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="4cd98-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="4cd98-115">Par défaut, si JetCreateDatabase est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée.</span><span class="sxs-lookup"><span data-stu-id="4cd98-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="4cd98-116">OverwriteExisting modifie ce comportement et l’ancienne base de données est remplacée par une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="4cd98-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4cd98-117">RecoveryOff</span><span class="sxs-lookup"><span data-stu-id="4cd98-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="4cd98-118">Désactive la journalisation.</span><span class="sxs-lookup"><span data-stu-id="4cd98-118">Turns off logging.</span></span> <span data-ttu-id="4cd98-119">La définition de ce bit perd la possibilité de relire les fichiers journaux et de récupérer la base de données à un État utilisable cohérent après un incident.</span><span class="sxs-lookup"><span data-stu-id="4cd98-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4cd98-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cd98-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4cd98-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4cd98-121">Reference</span></span>

[<span data-ttu-id="4cd98-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4cd98-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
