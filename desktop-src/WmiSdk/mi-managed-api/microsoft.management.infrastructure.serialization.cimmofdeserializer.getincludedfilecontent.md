---
description: 'En savoir plus sur : CimMofDeserializer. GetIncludedFileContent Delegate (String)'
title: Délégué CimMofDeserializer. GetIncludedFileContent (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.GetIncludedFileContent delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::GetIncludedFileContent
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: cb922d785da7d01de93adec56cefee29785210d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527352"
---
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a><span data-ttu-id="8b8ab-103">CimMofDeserializer. GetIncludedFileContent, délégué (String)</span><span class="sxs-lookup"><span data-stu-id="8b8ab-103">CimMofDeserializer.GetIncludedFileContent delegate (String)</span></span>

<span data-ttu-id="8b8ab-104">Représente un rappel permettant de récupérer le contenu du fichier sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="8b8ab-104">Represents a callback to retrieve the file's contents in the form of a byte array.</span></span>

<span data-ttu-id="8b8ab-105">**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b8ab-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="8b8ab-106">**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="8b8ab-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="8b8ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b8ab-107">Syntax</span></span>

``` csharp
public delegate byte[] GetIncludedFileContent(
    string fileName
)
```

``` c++
public delegate array<unsigned char>^ GetIncludedFileContent(
    String^ fileName
)
```

``` fsharp
type GetIncludedFileContent = 
    delegate of 
        fileName:string -> byte[]
```

``` vb
Public Delegate Function GetIncludedFileContent (
    fileName As String
) As Byte()
```

#### <a name="parameters"></a><span data-ttu-id="8b8ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b8ab-108">Parameters</span></span>

  - <span data-ttu-id="8b8ab-109">fileName</span><span class="sxs-lookup"><span data-stu-id="8b8ab-109">fileName</span></span>  
    <span data-ttu-id="8b8ab-110">Type : [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="8b8ab-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="8b8ab-111">Nom de fichier, chemin d’accès compris.</span><span class="sxs-lookup"><span data-stu-id="8b8ab-111">File name, including path.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8b8ab-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b8ab-112">Return Value</span></span>

<span data-ttu-id="8b8ab-113">Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="8b8ab-113">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>

<span data-ttu-id="8b8ab-114">Retourne le contenu du fichier sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="8b8ab-114">Returns the file's contents in the form of a byte array.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b8ab-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b8ab-115">See Also</span></span>

<span data-ttu-id="8b8ab-116">[Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b8ab-116">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
