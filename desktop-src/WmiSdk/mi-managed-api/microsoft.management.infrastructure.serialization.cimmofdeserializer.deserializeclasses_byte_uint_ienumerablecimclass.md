---
description: 'En savoir plus sur : méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable <CimClass> )'
title: Méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass)) (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518891"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="58785-103">Méthode CimMofDeserializer. DeserializeClasses (Byte \[ \] , UInt32, IEnumerable \<CimClass\> )</span><span class="sxs-lookup"><span data-stu-id="58785-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="58785-104">Désérialise des classes CIM basées sur des données sérialisées et une collection de classes CIM parentes.</span><span class="sxs-lookup"><span data-stu-id="58785-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="58785-105">**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58785-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="58785-106">**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="58785-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="58785-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58785-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="58785-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58785-108">Parameters</span></span>

  - <span data-ttu-id="58785-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="58785-109">serializedData</span></span>  
    <span data-ttu-id="58785-110">Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="58785-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="58785-111">Mémoire tampon qui contient les données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="58785-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="58785-112">offset</span><span class="sxs-lookup"><span data-stu-id="58785-112">offset</span></span>  
    <span data-ttu-id="58785-113">Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="58785-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="58785-114">Offset d’octet à l’emplacement où commencer la lecture des données.</span><span class="sxs-lookup"><span data-stu-id="58785-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="58785-115">Lorsque la méthode est retournée, le décalage pointe vers l’octet suivant après les classes désérialisées.</span><span class="sxs-lookup"><span data-stu-id="58785-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="58785-116">Classes</span><span class="sxs-lookup"><span data-stu-id="58785-116">classes</span></span>  
    <span data-ttu-id="58785-117">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="58785-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="58785-118">Cache facultatif de classes CIM parentes.</span><span class="sxs-lookup"><span data-stu-id="58785-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="58785-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58785-119">Return value</span></span>

<span data-ttu-id="58785-120">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="58785-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="58785-121">Interface [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) qui peut être utilisée pour énumérer les classes CIM.</span><span class="sxs-lookup"><span data-stu-id="58785-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="58785-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58785-122">See also</span></span>

<span data-ttu-id="58785-123">[CimClass, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58785-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="58785-124">[Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58785-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
