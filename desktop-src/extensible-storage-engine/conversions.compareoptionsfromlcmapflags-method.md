---
description: 'En savoir plus sur : conversions. CompareOptionsFromLCMapFlags, méthode'
title: Conversions. CompareOptionsFromLCMapFlags, méthode
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201758"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="0be89-103">Conversions. CompareOptionsFromLCMapFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="0be89-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="0be89-104">Les indicateurs fournis pour LCMapFlags, les transforment en options de comparaison.</span><span class="sxs-lookup"><span data-stu-id="0be89-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="0be89-105">Les options inconnues sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="0be89-105">Unknown options are ignored.</span></span>

<span data-ttu-id="0be89-106">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="0be89-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="0be89-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0be89-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0be89-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0be89-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0be89-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0be89-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="0be89-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0be89-110">Parameters</span></span>

  - <span data-ttu-id="0be89-111">lcmapFlags</span><span class="sxs-lookup"><span data-stu-id="0be89-111">lcmapFlags</span></span>  
    <span data-ttu-id="0be89-112">Type : [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="0be89-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="0be89-113">Indicateurs LCMapString.</span><span class="sxs-lookup"><span data-stu-id="0be89-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0be89-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0be89-114">Return value</span></span>

<span data-ttu-id="0be89-115">Type : [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="0be89-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="0be89-116">CompareOptions décrivant les indicateurs (connus).</span><span class="sxs-lookup"><span data-stu-id="0be89-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0be89-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0be89-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0be89-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0be89-118">Reference</span></span>

[<span data-ttu-id="0be89-119">Conversions (classe)</span><span class="sxs-lookup"><span data-stu-id="0be89-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="0be89-120">Conversions, membres</span><span class="sxs-lookup"><span data-stu-id="0be89-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="0be89-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0be89-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
