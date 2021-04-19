---
description: 'En savoir plus sur : conversion implicite de session (session à JET_SESID)'
title: Conversion implicite de session (session à JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544715"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a><span data-ttu-id="19d85-103">Conversion implicite de session (session à JET_SESID)</span><span class="sxs-lookup"><span data-stu-id="19d85-103">Session Implicit conversion (Session to JET_SESID)</span></span>

<span data-ttu-id="19d85-104">Opérateur de conversion implicite d’une session en JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="19d85-104">Implicit conversion operator from a Session to a JET_SESID.</span></span> <span data-ttu-id="19d85-105">Cela permet d’utiliser une session avec des API qui attendent un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="19d85-105">This allows a Session to be used with APIs which expect a JET_SESID.</span></span>

<span data-ttu-id="19d85-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19d85-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19d85-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19d85-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19d85-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19d85-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a><span data-ttu-id="19d85-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19d85-109">Parameters</span></span>

  - <span data-ttu-id="19d85-110">session</span><span class="sxs-lookup"><span data-stu-id="19d85-110">session</span></span>  
    <span data-ttu-id="19d85-111">Type : [Microsoft. ISAM. esent. Interop. session](./session-class.md)</span><span class="sxs-lookup"><span data-stu-id="19d85-111">Type: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)</span></span>  
    
    <span data-ttu-id="19d85-112">Session à convertir.</span><span class="sxs-lookup"><span data-stu-id="19d85-112">The session to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="19d85-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19d85-113">Return value</span></span>

<span data-ttu-id="19d85-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="19d85-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
<span data-ttu-id="19d85-115">JET_SESID de la session.</span><span class="sxs-lookup"><span data-stu-id="19d85-115">The JET_SESID of the session.</span></span>  

## <a name="see-also"></a><span data-ttu-id="19d85-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19d85-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19d85-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="19d85-117">Reference</span></span>

<span data-ttu-id="19d85-118">[Session class](./session-class.md) (Classe Session)</span><span class="sxs-lookup"><span data-stu-id="19d85-118">[Session class](./session-class.md)</span></span>

[<span data-ttu-id="19d85-119">Membres de session</span><span class="sxs-lookup"><span data-stu-id="19d85-119">Session members</span></span>](./session-members.md)

[<span data-ttu-id="19d85-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="19d85-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
