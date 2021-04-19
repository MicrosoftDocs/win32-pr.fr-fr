---
description: 'En savoir plus sur : champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault'
title: Champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534302"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a><span data-ttu-id="872ae-103">Champ Server2003Grbits. EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="872ae-103">Server2003Grbits.EnumerateIgnoreUserDefinedDefault field</span></span>

<span data-ttu-id="872ae-104">Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="872ae-104">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="872ae-105">Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="872ae-105">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span>

<span data-ttu-id="872ae-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="872ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="872ae-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="872ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="872ae-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="872ae-108">Syntax</span></span>

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a><span data-ttu-id="872ae-109">Notes</span><span class="sxs-lookup"><span data-stu-id="872ae-109">Remarks</span></span>

<span data-ttu-id="872ae-110">Cette option est disponible uniquement pour les systèmes d’exploitation Windows Server 2003 SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="872ae-110">This option is only available for Windows Server 2003 SP1 and later operating systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="872ae-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="872ae-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="872ae-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="872ae-112">Reference</span></span>

[<span data-ttu-id="872ae-113">Server2003Grbits, classe</span><span class="sxs-lookup"><span data-stu-id="872ae-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="872ae-114">Membres Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="872ae-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="872ae-115">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="872ae-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
