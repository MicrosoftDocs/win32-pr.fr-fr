---
description: 'En savoir plus sur : méthode API. JetFreeBuffer'
title: API. JetFreeBuffer, méthode
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514998"
---
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="90d76-103">API. JetFreeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="90d76-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="90d76-104">Libère de la mémoire qui a été allouée par un appel du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="90d76-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="90d76-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90d76-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90d76-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90d76-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90d76-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90d76-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a><span data-ttu-id="90d76-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90d76-108">Parameters</span></span>

  - <span data-ttu-id="90d76-109">buffer</span><span class="sxs-lookup"><span data-stu-id="90d76-109">buffer</span></span>  
    <span data-ttu-id="90d76-110">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="90d76-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="90d76-111">Mémoire tampon allouée par un appel au moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="90d76-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="90d76-112">[Zéro](/dotnet/api/system.intptr.zero) est acceptable et sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="90d76-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="90d76-113">Notes</span><span class="sxs-lookup"><span data-stu-id="90d76-113">Remarks</span></span>

<span data-ttu-id="90d76-114">Cette méthode est interne, car nous n’exposez jamais la mémoire allouée par ESENT à nos appelants.</span><span class="sxs-lookup"><span data-stu-id="90d76-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="90d76-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90d76-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90d76-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="90d76-116">Reference</span></span>

[<span data-ttu-id="90d76-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="90d76-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="90d76-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="90d76-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="90d76-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="90d76-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
