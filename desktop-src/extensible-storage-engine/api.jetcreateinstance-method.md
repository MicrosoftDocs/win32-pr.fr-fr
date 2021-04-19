---
description: 'En savoir plus sur : méthode API. JetCreateInstance'
title: API. JetCreateInstance, méthode
TOCTitle: 'JetCreateInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance(v=EXCHG.10)
ms:contentKeyID: 55100672
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e865c443d4f19b14a955204840355ee73be8773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516434"
---
# <a name="apijetcreateinstance-method"></a><span data-ttu-id="37817-103">API. JetCreateInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="37817-103">Api.JetCreateInstance method</span></span>

<span data-ttu-id="37817-104">Alloue une nouvelle instance du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="37817-104">Allocates a new instance of the database engine.</span></span>

<span data-ttu-id="37817-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37817-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37817-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37817-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37817-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37817-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As StringApi.JetCreateInstance(instance, _
    name)
```

``` csharp
public static void JetCreateInstance(
    out JET_INSTANCE instance,
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="37817-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37817-108">Parameters</span></span>

  - <span data-ttu-id="37817-109">instance</span><span class="sxs-lookup"><span data-stu-id="37817-109">instance</span></span>  
    <span data-ttu-id="37817-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37817-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="37817-111">Retourne la nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="37817-111">Returns the new instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="37817-112">name</span><span class="sxs-lookup"><span data-stu-id="37817-112">name</span></span>  
    <span data-ttu-id="37817-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="37817-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="37817-114">Nom de l'instance.</span><span class="sxs-lookup"><span data-stu-id="37817-114">The name of the instance.</span></span> <span data-ttu-id="37817-115">Les noms doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="37817-115">Names must be unique.</span></span>

## <a name="see-also"></a><span data-ttu-id="37817-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37817-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37817-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="37817-117">Reference</span></span>

[<span data-ttu-id="37817-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="37817-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="37817-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="37817-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="37817-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="37817-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
