---
description: 'En savoir plus sur : propriété JET_RETINFO. itagSequence'
title: JET_RETINFO. itagSequence, propriété
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210384"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="9c334-103">JET_RETINFO. itagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="9c334-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="9c334-104">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="9c334-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="9c334-105">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="9c334-105">The array of values is one-based.</span></span> <span data-ttu-id="9c334-106">La première valeur est séquence 1, et non 0.</span><span class="sxs-lookup"><span data-stu-id="9c334-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="9c334-107">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que itagSequence.</span><span class="sxs-lookup"><span data-stu-id="9c334-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="9c334-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9c334-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9c334-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9c334-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9c334-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c334-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9c334-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9c334-111">Property value</span></span>

<span data-ttu-id="9c334-112">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9c334-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c334-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c334-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9c334-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9c334-114">Reference</span></span>

[<span data-ttu-id="9c334-115">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9c334-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="9c334-116">Membres JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9c334-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="9c334-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9c334-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
