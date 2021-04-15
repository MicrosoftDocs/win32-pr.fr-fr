---
description: 'En savoir plus sur : méthode CimMofDeserializer. DeserializeInstances (Byte [], UInt32)'
title: Méthode CimMofDeserializer. DeserializeInstances (Byte [], UInt32) (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 90cc4f9d88afa9f4ec566ff4733995bce8160eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524813"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a><span data-ttu-id="aa7f0-103">Méthode CimMofDeserializer. DeserializeInstances (Byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="aa7f0-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="aa7f0-104">Désérialise les instances CIM en fonction des données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="aa7f0-104">Deserializes CIM instances based on serialized data.</span></span>

<span data-ttu-id="aa7f0-105">**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa7f0-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="aa7f0-106">**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="aa7f0-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="aa7f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa7f0-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="aa7f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa7f0-108">Parameters</span></span>

  - <span data-ttu-id="aa7f0-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="aa7f0-109">serializedData</span></span>  
    <span data-ttu-id="aa7f0-110">Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="aa7f0-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="aa7f0-111">Mémoire tampon qui contient les données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="aa7f0-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa7f0-112">offset</span><span class="sxs-lookup"><span data-stu-id="aa7f0-112">offset</span></span>  
    <span data-ttu-id="aa7f0-113">Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="aa7f0-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="aa7f0-114">Offset d’octet à l’emplacement où commencer la lecture des données.</span><span class="sxs-lookup"><span data-stu-id="aa7f0-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="aa7f0-115">Lorsque la méthode est retournée, le décalage pointe vers l’octet suivant après les instances désérialisées.</span><span class="sxs-lookup"><span data-stu-id="aa7f0-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aa7f0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa7f0-116">Return value</span></span>

<span data-ttu-id="aa7f0-117">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="aa7f0-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="aa7f0-118">Interface [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) qui peut être utilisée pour énumérer les classes CIM.</span><span class="sxs-lookup"><span data-stu-id="aa7f0-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa7f0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa7f0-119">See also</span></span>

<span data-ttu-id="aa7f0-120">[CimInstance, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa7f0-120">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="aa7f0-121">[Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa7f0-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
