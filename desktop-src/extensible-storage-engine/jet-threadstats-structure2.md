---
description: 'En savoir plus sur : structure JET_THREADSTATS'
title: Structure de JET_THREADSTATS (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517224"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="f6fbf-103">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="f6fbf-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="f6fbf-104">Contient des statistiques cumulatives sur le travail effectué par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="f6fbf-105">Ces informations sont retournées via JetGetThreadStats.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="f6fbf-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6fbf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f6fbf-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6fbf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fbf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6fbf-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="f6fbf-109">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f6fbf-109">Thread safety</span></span>

<span data-ttu-id="f6fbf-110">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f6fbf-111">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6fbf-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6fbf-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6fbf-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f6fbf-113">Reference</span></span>

[<span data-ttu-id="f6fbf-114">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="f6fbf-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="f6fbf-115">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="f6fbf-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
