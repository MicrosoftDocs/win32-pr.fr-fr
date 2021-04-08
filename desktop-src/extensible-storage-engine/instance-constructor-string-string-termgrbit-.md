---
description: 'En savoir plus sur : constructeur d’instance (String, String, TermGrbit)'
title: Constructeur d’instance (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753301"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="9854a-103">Constructeur d’instance (String, String, TermGrbit)</span><span class="sxs-lookup"><span data-stu-id="9854a-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="9854a-104">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="9854a-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="9854a-105">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="9854a-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="9854a-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9854a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9854a-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9854a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9854a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9854a-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9854a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9854a-109">Parameters</span></span>

  - <span data-ttu-id="9854a-110">name</span><span class="sxs-lookup"><span data-stu-id="9854a-110">name</span></span>  
    <span data-ttu-id="9854a-111">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9854a-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9854a-112">Nom de l'instance.</span><span class="sxs-lookup"><span data-stu-id="9854a-112">The name of the instance.</span></span> <span data-ttu-id="9854a-113">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="9854a-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="9854a-114">displayName</span><span class="sxs-lookup"><span data-stu-id="9854a-114">displayName</span></span>  
    <span data-ttu-id="9854a-115">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9854a-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9854a-116">Nom complet de l’instance.</span><span class="sxs-lookup"><span data-stu-id="9854a-116">A display name for the instance.</span></span> <span data-ttu-id="9854a-117">Il sera utilisé dans les entrées du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="9854a-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="9854a-118">termGrbit</span><span class="sxs-lookup"><span data-stu-id="9854a-118">termGrbit</span></span>  
    <span data-ttu-id="9854a-119">Type : [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9854a-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9854a-120">TermGrbit à utiliser au moment de la JetTerm.</span><span class="sxs-lookup"><span data-stu-id="9854a-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="9854a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9854a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9854a-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9854a-122">Reference</span></span>

[<span data-ttu-id="9854a-123">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="9854a-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="9854a-124">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="9854a-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="9854a-125">Surcharge d’instance</span><span class="sxs-lookup"><span data-stu-id="9854a-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="9854a-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9854a-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
