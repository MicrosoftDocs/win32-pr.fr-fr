---
description: 'En savoir plus sur : constructeur EsentObsoleteException (String, JET_err)'
title: Constructeur EsentObsoleteException (String, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517025"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a><span data-ttu-id="02b6a-103">Constructeur EsentObsoleteException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="02b6a-103">EsentObsoleteException constructor (String, JET_err)</span></span>

<span data-ttu-id="02b6a-104">Initialise une nouvelle instance de la classe EsentObsoleteException.</span><span class="sxs-lookup"><span data-stu-id="02b6a-104">Initializes a new instance of the EsentObsoleteException class.</span></span>

<span data-ttu-id="02b6a-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02b6a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02b6a-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02b6a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02b6a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02b6a-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="02b6a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02b6a-108">Parameters</span></span>

  - <span data-ttu-id="02b6a-109">description</span><span class="sxs-lookup"><span data-stu-id="02b6a-109">description</span></span>  
    <span data-ttu-id="02b6a-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02b6a-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02b6a-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="02b6a-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="02b6a-112">Raise</span><span class="sxs-lookup"><span data-stu-id="02b6a-112">err</span></span>  
    <span data-ttu-id="02b6a-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02b6a-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="02b6a-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="02b6a-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="02b6a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02b6a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02b6a-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="02b6a-116">Reference</span></span>

[<span data-ttu-id="02b6a-117">EsentObsoleteException, classe</span><span class="sxs-lookup"><span data-stu-id="02b6a-117">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="02b6a-118">Membres EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="02b6a-118">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="02b6a-119">Surcharge EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="02b6a-119">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="02b6a-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="02b6a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
