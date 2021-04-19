---
description: 'En savoir plus sur : méthode API. JetTerm2'
title: API. JetTerm2, méthode
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e8a4aa8c96f9a4d0242657fe7126abf1388a7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521996"
---
# <a name="apijetterm2-method"></a><span data-ttu-id="56e5e-103">API. JetTerm2, méthode</span><span class="sxs-lookup"><span data-stu-id="56e5e-103">Api.JetTerm2 method</span></span>

<span data-ttu-id="56e5e-104">Termine une instance qui a été créée avec [JetInit (JET_INSTANCE)](./api.jetinit-method.md) ou [JetCreateInstance (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="56e5e-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="56e5e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56e5e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56e5e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56e5e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56e5e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56e5e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="56e5e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56e5e-108">Parameters</span></span>

  - <span data-ttu-id="56e5e-109">instance</span><span class="sxs-lookup"><span data-stu-id="56e5e-109">instance</span></span>  
    <span data-ttu-id="56e5e-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="56e5e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="56e5e-111">Instance à arrêter.</span><span class="sxs-lookup"><span data-stu-id="56e5e-111">The instance to terminate.</span></span>

<!-- end list -->

  - <span data-ttu-id="56e5e-112">grbit</span><span class="sxs-lookup"><span data-stu-id="56e5e-112">grbit</span></span>  
    <span data-ttu-id="56e5e-113">Type : [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="56e5e-113">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="56e5e-114">Options d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="56e5e-114">Termination options.</span></span>

## <a name="see-also"></a><span data-ttu-id="56e5e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56e5e-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56e5e-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="56e5e-116">Reference</span></span>

[<span data-ttu-id="56e5e-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="56e5e-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="56e5e-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="56e5e-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="56e5e-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="56e5e-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
