---
description: 'En savoir plus sur : conversion implicite d’instance (instance to JET_INSTANCE)'
title: Conversion implicite d’instance (instance à JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520439"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a><span data-ttu-id="3d2c6-103">Conversion implicite d’instance (instance à JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="3d2c6-103">Instance Implicit conversion (Instance to JET_INSTANCE)</span></span>

<span data-ttu-id="3d2c6-104">Fournir la conversion implicite d’un objet d’instance en une structure JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="3d2c6-104">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="3d2c6-105">Cette opération est effectuée afin qu’une instance puisse être utilisée partout où une JET_INSTANCE est requise.</span><span class="sxs-lookup"><span data-stu-id="3d2c6-105">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span>

<span data-ttu-id="3d2c6-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d2c6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d2c6-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d2c6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d2c6-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a><span data-ttu-id="3d2c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d2c6-109">Parameters</span></span>

  - <span data-ttu-id="3d2c6-110">instance</span><span class="sxs-lookup"><span data-stu-id="3d2c6-110">instance</span></span>  
    <span data-ttu-id="3d2c6-111">Type : [Microsoft. ISAM. esent. Interop. instance](./instance-class.md)</span><span class="sxs-lookup"><span data-stu-id="3d2c6-111">Type: [Microsoft.Isam.Esent.Interop.Instance](./instance-class.md)</span></span>  
    
    <span data-ttu-id="3d2c6-112">Instance à convertir.</span><span class="sxs-lookup"><span data-stu-id="3d2c6-112">The instance to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3d2c6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d2c6-113">Return value</span></span>

<span data-ttu-id="3d2c6-114">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d2c6-114">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
<span data-ttu-id="3d2c6-115">JET_INSTANCE encapsulé par l’instance de.</span><span class="sxs-lookup"><span data-stu-id="3d2c6-115">The JET_INSTANCE wrapped by the instance.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d2c6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d2c6-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d2c6-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3d2c6-117">Reference</span></span>

[<span data-ttu-id="3d2c6-118">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="3d2c6-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="3d2c6-119">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="3d2c6-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="3d2c6-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3d2c6-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
