---
description: 'En savoir plus sur : constructeur d’instance (String, String)'
title: Constructeur d’instance (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318669"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="c937d-103">Constructeur d’instance (String, String)</span><span class="sxs-lookup"><span data-stu-id="c937d-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="c937d-104">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="c937d-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="c937d-105">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="c937d-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="c937d-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c937d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c937d-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c937d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c937d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c937d-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="c937d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c937d-109">Parameters</span></span>

  - <span data-ttu-id="c937d-110">name</span><span class="sxs-lookup"><span data-stu-id="c937d-110">name</span></span>  
    <span data-ttu-id="c937d-111">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c937d-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c937d-112">Nom de l'instance.</span><span class="sxs-lookup"><span data-stu-id="c937d-112">The name of the instance.</span></span> <span data-ttu-id="c937d-113">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="c937d-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="c937d-114">displayName</span><span class="sxs-lookup"><span data-stu-id="c937d-114">displayName</span></span>  
    <span data-ttu-id="c937d-115">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c937d-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c937d-116">Nom complet de l’instance.</span><span class="sxs-lookup"><span data-stu-id="c937d-116">A display name for the instance.</span></span> <span data-ttu-id="c937d-117">Il sera utilisé dans les entrées du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c937d-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="c937d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c937d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c937d-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c937d-119">Reference</span></span>

[<span data-ttu-id="c937d-120">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="c937d-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="c937d-121">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="c937d-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="c937d-122">Surcharge d’instance</span><span class="sxs-lookup"><span data-stu-id="c937d-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="c937d-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c937d-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
