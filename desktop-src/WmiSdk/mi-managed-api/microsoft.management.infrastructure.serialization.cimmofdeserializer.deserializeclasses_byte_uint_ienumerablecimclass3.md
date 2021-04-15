---
description: 'En savoir plus sur : méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable <CimClass> , String, String, OnClassNeeded, GetIncludedFileContent)'
title: Méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524808"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="00541-103">Méthode CimMofDeserializer. DeserializeClasses (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , String, String, OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="00541-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, String, String, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="00541-104">Désérialise les classes CIM en fonction des données sérialisées, de la collection de classes CIM parents, des noms d’ordinateur et d’espace de noms et des rappels.</span><span class="sxs-lookup"><span data-stu-id="00541-104">Deserializes CIM classes based on serialized data, collection of parent CIM classes, computer and namespace names, and callbacks.</span></span>

<span data-ttu-id="00541-105">**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00541-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="00541-106">**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="00541-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="00541-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00541-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="00541-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00541-108">Parameters</span></span>

  - <span data-ttu-id="00541-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="00541-109">serializedData</span></span>  
    <span data-ttu-id="00541-110">Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="00541-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="00541-111">Mémoire tampon qui contient les données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="00541-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-112">offset</span><span class="sxs-lookup"><span data-stu-id="00541-112">offset</span></span>  
    <span data-ttu-id="00541-113">Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="00541-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="00541-114">Offset d’octet à l’emplacement où commencer la lecture des données.</span><span class="sxs-lookup"><span data-stu-id="00541-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="00541-115">Lorsque la méthode est retournée, le décalage pointe vers l’octet suivant après les classes désérialisées.</span><span class="sxs-lookup"><span data-stu-id="00541-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-116">Classes</span><span class="sxs-lookup"><span data-stu-id="00541-116">classes</span></span>  
    <span data-ttu-id="00541-117">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="00541-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="00541-118">Cache facultatif de classes CIM parentes.</span><span class="sxs-lookup"><span data-stu-id="00541-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-119">computerName</span><span class="sxs-lookup"><span data-stu-id="00541-119">computerName</span></span>  
    [<span data-ttu-id="00541-120">System.String</span><span class="sxs-lookup"><span data-stu-id="00541-120">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="00541-121">Nom de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00541-121">The computer name.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-122">namespaceName</span><span class="sxs-lookup"><span data-stu-id="00541-122">namespaceName</span></span>  
    [<span data-ttu-id="00541-123">System.String</span><span class="sxs-lookup"><span data-stu-id="00541-123">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="00541-124">L'espace de noms.</span><span class="sxs-lookup"><span data-stu-id="00541-124">The namespace name.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-125">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="00541-125">onClassNeededCallback</span></span>  
    <span data-ttu-id="00541-126">Type : [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="00541-126">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="00541-127">Fonction de rappel utilisée pour fournir un objet de classe demandé pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="00541-127">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="00541-128">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="00541-128">getIncludedFileCallback</span></span>  
    <span data-ttu-id="00541-129">Type : [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="00541-129">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="00541-130">Fonction de rappel utilisée pour fournir le contenu de la mémoire tampon d’un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="00541-130">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="00541-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00541-131">Return value</span></span>

<span data-ttu-id="00541-132">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="00541-132">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="00541-133">Interface [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) qui peut être utilisée pour énumérer les classes CIM.</span><span class="sxs-lookup"><span data-stu-id="00541-133">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="00541-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00541-134">See also</span></span>

<span data-ttu-id="00541-135">[CimClass, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00541-135">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="00541-136">[Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00541-136">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
