---
description: 'En savoir plus sur : énumération LegacyFileNames'
title: Énumération LegacyFileNames (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951279"
---
# <a name="legacyfilenames-enumeration"></a><span data-ttu-id="c87f1-103">Énumération LegacyFileNames</span><span class="sxs-lookup"><span data-stu-id="c87f1-103">LegacyFileNames enumeration</span></span>

<span data-ttu-id="c87f1-104">Options pour LegacyFileNames</span><span class="sxs-lookup"><span data-stu-id="c87f1-104">Options for LegacyFileNames</span></span>

<span data-ttu-id="c87f1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c87f1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c87f1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c87f1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c87f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c87f1-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
```

## <a name="members"></a><span data-ttu-id="c87f1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c87f1-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c87f1-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="c87f1-109">Member name</span></span></th>
<th><span data-ttu-id="c87f1-110">Description</span><span class="sxs-lookup"><span data-stu-id="c87f1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c87f1-111">ESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="c87f1-111">ESE98FileNames</span></span></td>
<td><span data-ttu-id="c87f1-112">Lorsque cette option est présente, le moteur de base de données utilise les conventions d’affectation de noms suivantes pour ses fichiers : o les fichiers journaux des transactions seront utilisés. LOG pour l’extension de fichier, les fichiers de point de contrôle utilisent. CHK pour leur extension de fichier</span><span class="sxs-lookup"><span data-stu-id="c87f1-112">When this option is present then the database engine will use the following naming conventions for its files: o Transaction Log files will use .LOG for their file extension o Checkpoint files will use .CHK for their file extension</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c87f1-113">EightDotThreeSoftCompat</span><span class="sxs-lookup"><span data-stu-id="c87f1-113">EightDotThreeSoftCompat</span></span></td>
<td><span data-ttu-id="c87f1-114">Conservez la syntaxe de nom 8,3 aussi longtemps que possible.</span><span class="sxs-lookup"><span data-stu-id="c87f1-114">Preserve the 8.3 naming syntax for as long as possible.</span></span> <span data-ttu-id="c87f1-115">(cela ne doit pas être modifié, sans vérifier qu’il n’y a pas de fichiers journaux)</span><span class="sxs-lookup"><span data-stu-id="c87f1-115">(this should not be changed, w/o ensuring there are no log files)</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c87f1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c87f1-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c87f1-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c87f1-117">Reference</span></span>

[<span data-ttu-id="c87f1-118">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="c87f1-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
