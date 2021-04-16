---
description: 'En savoir plus sur : classe EsentDatabaseAlreadyUpgradedException'
title: EsentDatabaseAlreadyUpgradedException, classe
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27ad5a37676ef0b8e4a450619c19a45f3bdee1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530363"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a><span data-ttu-id="5aad0-103">EsentDatabaseAlreadyUpgradedException, classe</span><span class="sxs-lookup"><span data-stu-id="5aad0-103">EsentDatabaseAlreadyUpgradedException class</span></span>

<span data-ttu-id="5aad0-104">Classe de base pour JET_err. Exceptions DatabaseAlreadyUpgraded.</span><span class="sxs-lookup"><span data-stu-id="5aad0-104">Base class for JET_err.DatabaseAlreadyUpgraded exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5aad0-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="5aad0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5aad0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5aad0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5aad0-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5aad0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5aad0-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5aad0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5aad0-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5aad0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5aad0-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="5aad0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5aad0-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="5aad0-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="5aad0-112">Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="5aad0-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>  

<span data-ttu-id="5aad0-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5aad0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5aad0-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5aad0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5aad0-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aad0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="5aad0-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="5aad0-116">Thread safety</span></span>

<span data-ttu-id="5aad0-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5aad0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5aad0-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5aad0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5aad0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aad0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5aad0-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5aad0-120">Reference</span></span>

[<span data-ttu-id="5aad0-121">Membres EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="5aad0-121">EsentDatabaseAlreadyUpgradedException members</span></span>](./esentdatabasealreadyupgradedexception-members.md)

[<span data-ttu-id="5aad0-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5aad0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
