---
description: 'En savoir plus sur : conversions. LCMapFlagsFromCompareOptions, méthode'
title: Conversions. LCMapFlagsFromCompareOptions, méthode
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516944"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="88f62-103">Conversions. LCMapFlagsFromCompareOptions, méthode</span><span class="sxs-lookup"><span data-stu-id="88f62-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="88f62-104">Donnez à CompareOptions, transformez-les en indicateurs à partir de LCMapString.</span><span class="sxs-lookup"><span data-stu-id="88f62-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="88f62-105">Les options inconnues sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="88f62-105">Unknown options are ignored.</span></span>

<span data-ttu-id="88f62-106">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="88f62-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="88f62-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88f62-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="88f62-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="88f62-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88f62-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88f62-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="88f62-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88f62-110">Parameters</span></span>

  - <span data-ttu-id="88f62-111">Admet</span><span class="sxs-lookup"><span data-stu-id="88f62-111">compareOptions</span></span>  
    <span data-ttu-id="88f62-112">Type : [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="88f62-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="88f62-113">Options à convertir.</span><span class="sxs-lookup"><span data-stu-id="88f62-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="88f62-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88f62-114">Return value</span></span>

<span data-ttu-id="88f62-115">Type : [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="88f62-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="88f62-116">Indicateurs LCMapString qui correspondent aux options de comparaison.</span><span class="sxs-lookup"><span data-stu-id="88f62-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="88f62-117">Les options non prises en charge sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="88f62-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="88f62-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88f62-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88f62-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="88f62-119">Reference</span></span>

[<span data-ttu-id="88f62-120">Conversions (classe)</span><span class="sxs-lookup"><span data-stu-id="88f62-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="88f62-121">Conversions, membres</span><span class="sxs-lookup"><span data-stu-id="88f62-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="88f62-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="88f62-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
