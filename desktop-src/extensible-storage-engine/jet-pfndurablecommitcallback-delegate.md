---
description: 'En savoir plus sur : JET_PFNDURABLECOMMITCALLBACK délégué'
title: JET_PFNDURABLECOMMITCALLBACK délégué (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868946"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a><span data-ttu-id="98960-103">Délégué JET_PFNDURABLECOMMITCALLBACK</span><span class="sxs-lookup"><span data-stu-id="98960-103">JET_PFNDURABLECOMMITCALLBACK delegate</span></span>

<span data-ttu-id="98960-104">Rappel pour JET_paramDurableCommitCallback.</span><span class="sxs-lookup"><span data-stu-id="98960-104">Callback for JET_paramDurableCommitCallback.</span></span>

<span data-ttu-id="98960-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98960-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="98960-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="98960-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98960-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98960-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="98960-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98960-108">Parameters</span></span>

  - <span data-ttu-id="98960-109">instance</span><span class="sxs-lookup"><span data-stu-id="98960-109">instance</span></span>  
    <span data-ttu-id="98960-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98960-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="98960-111">Instance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="98960-111">Instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="98960-112">pCommitIdSeen</span><span class="sxs-lookup"><span data-stu-id="98960-112">pCommitIdSeen</span></span>  
    <span data-ttu-id="98960-113">Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="98960-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="98960-114">Commit-ID qui vient d’être vidé.</span><span class="sxs-lookup"><span data-stu-id="98960-114">Commit-id that has just been flushed.</span></span>

<!-- end list -->

  - <span data-ttu-id="98960-115">grbit</span><span class="sxs-lookup"><span data-stu-id="98960-115">grbit</span></span>  
    <span data-ttu-id="98960-116">Tapez : [Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="98960-116">Type: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="98960-117">Réservé actuellement.</span><span class="sxs-lookup"><span data-stu-id="98960-117">Reserved currently.</span></span>

#### <a name="return-value"></a><span data-ttu-id="98960-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98960-118">Return value</span></span>

<span data-ttu-id="98960-119">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="98960-119">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="98960-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98960-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98960-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="98960-121">Reference</span></span>

[<span data-ttu-id="98960-122">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="98960-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
