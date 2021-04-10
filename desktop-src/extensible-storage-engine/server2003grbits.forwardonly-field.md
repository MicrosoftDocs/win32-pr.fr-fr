---
description: 'En savoir plus sur : champ Server2003Grbits. ForwardOnly'
title: Champ Server2003Grbits. ForwardOnly (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114042"
---
# <a name="server2003grbitsforwardonly-field"></a><span data-ttu-id="e2a62-103">Champ Server2003Grbits. ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="e2a62-103">Server2003Grbits.ForwardOnly field</span></span>

<span data-ttu-id="e2a62-104">Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="e2a62-104">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="e2a62-105">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="e2a62-105">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="e2a62-106">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="e2a62-106">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="e2a62-107">Pour plus d’informations, consultez [unique](./temptablegrbit-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a62-107">See [Unique](./temptablegrbit-enumeration.md) for more information.</span></span>

<span data-ttu-id="e2a62-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2a62-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="e2a62-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2a62-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a62-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2a62-110">Syntax</span></span>

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a><span data-ttu-id="e2a62-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2a62-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2a62-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e2a62-112">Reference</span></span>

[<span data-ttu-id="e2a62-113">Server2003Grbits, classe</span><span class="sxs-lookup"><span data-stu-id="e2a62-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="e2a62-114">Membres Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="e2a62-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="e2a62-115">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="e2a62-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
