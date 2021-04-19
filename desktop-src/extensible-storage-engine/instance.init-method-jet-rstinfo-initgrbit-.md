---
description: 'En savoir plus sur : méthode Instance.Init (JET_RSTINFO, InitGrbit)'
title: Méthode Instance.Init (JET_RSTINFO, InitGrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538657"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="c9a6c-103">Méthode Instance.Init (JET_RSTINFO, InitGrbit)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="c9a6c-104">Initialisez le JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="c9a6c-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="c9a6c-105">Cette API nécessite au moins la version Vista d’ESENT.</span><span class="sxs-lookup"><span data-stu-id="c9a6c-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="c9a6c-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9a6c-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a6c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9a6c-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c9a6c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9a6c-109">Parameters</span></span>

  - <span data-ttu-id="c9a6c-110">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="c9a6c-110">recoveryOptions</span></span>  
    <span data-ttu-id="c9a6c-111">Type : [Microsoft.ISAM.esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="c9a6c-112">Paramètres de récupération supplémentaires pour le remappage des bases de données lors de la récupération, position où arrêter la récupération ou l’état de récupération.</span><span class="sxs-lookup"><span data-stu-id="c9a6c-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9a6c-113">grbit</span><span class="sxs-lookup"><span data-stu-id="c9a6c-113">grbit</span></span>  
    <span data-ttu-id="c9a6c-114">Type : [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c9a6c-115">Options d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="c9a6c-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9a6c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9a6c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9a6c-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c9a6c-117">Reference</span></span>

[<span data-ttu-id="c9a6c-118">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="c9a6c-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="c9a6c-119">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="c9a6c-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="c9a6c-120">Init (surcharge)</span><span class="sxs-lookup"><span data-stu-id="c9a6c-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="c9a6c-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c9a6c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
