---
description: 'En savoir plus sur : conversions. ConvertDoubleToDateTime, méthode'
title: Conversions. ConvertDoubleToDateTime, méthode
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530139"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="d0ae0-103">Conversions. ConvertDoubleToDateTime, méthode</span><span class="sxs-lookup"><span data-stu-id="d0ae0-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="d0ae0-104">Convertit un double (format de date et d’heure OA) en DateTime.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="d0ae0-105">Contrairement à DateTime. FromOADate, cela ne lève pas d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="d0ae0-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0ae0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0ae0-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0ae0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ae0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0ae0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="d0ae0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0ae0-109">Parameters</span></span>

  - <span data-ttu-id="d0ae0-110">d</span><span class="sxs-lookup"><span data-stu-id="d0ae0-110">d</span></span>  
    <span data-ttu-id="d0ae0-111">Type : [System. double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="d0ae0-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="d0ae0-112">Valeur de type double.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d0ae0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0ae0-113">Return value</span></span>

<span data-ttu-id="d0ae0-114">Type : [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="d0ae0-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="d0ae0-115">Valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="d0ae0-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0ae0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0ae0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0ae0-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d0ae0-117">Reference</span></span>

[<span data-ttu-id="d0ae0-118">Conversions (classe)</span><span class="sxs-lookup"><span data-stu-id="d0ae0-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="d0ae0-119">Conversions, membres</span><span class="sxs-lookup"><span data-stu-id="d0ae0-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="d0ae0-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0ae0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
