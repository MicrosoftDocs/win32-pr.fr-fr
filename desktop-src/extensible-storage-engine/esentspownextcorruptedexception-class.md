---
description: 'En savoir plus sur : classe EsentSPOwnExtCorruptedException'
title: EsentSPOwnExtCorruptedException, classe
TOCTitle: EsentSPOwnExtCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspownextcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102983
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 15f3f37dfafcaa58d63a34c19d629f4469826cd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530892"
---
# <a name="esentspownextcorruptedexception-class"></a><span data-ttu-id="c94ad-103">EsentSPOwnExtCorruptedException, classe</span><span class="sxs-lookup"><span data-stu-id="c94ad-103">EsentSPOwnExtCorruptedException class</span></span>

<span data-ttu-id="c94ad-104">Classe de base pour JET_err. Exceptions SPOwnExtCorrupted.</span><span class="sxs-lookup"><span data-stu-id="c94ad-104">Base class for JET_err.SPOwnExtCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c94ad-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="c94ad-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c94ad-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c94ad-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c94ad-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c94ad-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c94ad-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c94ad-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c94ad-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c94ad-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c94ad-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c94ad-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="c94ad-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c94ad-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="c94ad-112">Microsoft. ISAM. esent. Interop. EsentSPOwnExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="c94ad-112">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>  

<span data-ttu-id="c94ad-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c94ad-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c94ad-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c94ad-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c94ad-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c94ad-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPOwnExtCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSPOwnExtCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPOwnExtCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="c94ad-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="c94ad-116">Thread safety</span></span>

<span data-ttu-id="c94ad-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c94ad-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c94ad-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c94ad-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c94ad-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c94ad-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c94ad-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c94ad-120">Reference</span></span>

[<span data-ttu-id="c94ad-121">Membres EsentSPOwnExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="c94ad-121">EsentSPOwnExtCorruptedException members</span></span>](./esentspownextcorruptedexception-members.md)

[<span data-ttu-id="c94ad-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c94ad-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
