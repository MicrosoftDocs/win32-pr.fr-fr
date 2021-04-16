---
description: 'En savoir plus sur : constructeur EsentResourceException (String, JET_err)'
title: Constructeur EsentResourceException (String, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529458"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a><span data-ttu-id="aa91e-103">Constructeur EsentResourceException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="aa91e-103">EsentResourceException constructor (String, JET_err)</span></span>

<span data-ttu-id="aa91e-104">Initialise une nouvelle instance de la classe EsentResourceException.</span><span class="sxs-lookup"><span data-stu-id="aa91e-104">Initializes a new instance of the EsentResourceException class.</span></span>

<span data-ttu-id="aa91e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa91e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa91e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa91e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa91e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa91e-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="aa91e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa91e-108">Parameters</span></span>

  - <span data-ttu-id="aa91e-109">description</span><span class="sxs-lookup"><span data-stu-id="aa91e-109">description</span></span>  
    <span data-ttu-id="aa91e-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="aa91e-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="aa91e-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="aa91e-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa91e-112">Raise</span><span class="sxs-lookup"><span data-stu-id="aa91e-112">err</span></span>  
    <span data-ttu-id="aa91e-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aa91e-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="aa91e-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="aa91e-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa91e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa91e-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa91e-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="aa91e-116">Reference</span></span>

[<span data-ttu-id="aa91e-117">Classe EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="aa91e-117">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="aa91e-118">Membres EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="aa91e-118">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="aa91e-119">Surcharge EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="aa91e-119">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="aa91e-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aa91e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
