---
description: 'En savoir plus sur : constructeur d’instance (String)'
title: Constructeur d’instance (String)
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
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
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210995"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="6a05c-103">Constructeur d’instance (String)</span><span class="sxs-lookup"><span data-stu-id="6a05c-103">Instance constructor (String)</span></span>

<span data-ttu-id="6a05c-104">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="6a05c-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="6a05c-105">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="6a05c-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="6a05c-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a05c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a05c-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a05c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a05c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a05c-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="6a05c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a05c-109">Parameters</span></span>

  - <span data-ttu-id="6a05c-110">name</span><span class="sxs-lookup"><span data-stu-id="6a05c-110">name</span></span>  
    <span data-ttu-id="6a05c-111">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6a05c-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6a05c-112">Nom de l'instance.</span><span class="sxs-lookup"><span data-stu-id="6a05c-112">The name of the instance.</span></span> <span data-ttu-id="6a05c-113">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="6a05c-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a05c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a05c-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a05c-115">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6a05c-115">Reference</span></span>

[<span data-ttu-id="6a05c-116">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="6a05c-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="6a05c-117">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="6a05c-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="6a05c-118">Surcharge d’instance</span><span class="sxs-lookup"><span data-stu-id="6a05c-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="6a05c-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6a05c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
