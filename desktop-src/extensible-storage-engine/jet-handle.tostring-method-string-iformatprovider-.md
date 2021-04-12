---
description: 'En savoir plus sur : JET_HANDLE. ToString, méthode (String, IFormatProvider)'
title: JET_HANDLE. ToString, méthode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.tostring(v=EXCHG.10)
ms:contentKeyID: 39515173
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2891e33712027c3387e2d45ff73111e7bf54126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320501"
---
# <a name="jet_handletostring-method-string-iformatprovider"></a><span data-ttu-id="89df5-103">JET_HANDLE. ToString, méthode (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="89df5-103">JET_HANDLE.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="89df5-104">Met en forme la valeur de l’instance actuelle en utilisant le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="89df5-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="89df5-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89df5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89df5-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89df5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89df5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89df5-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_HANDLE
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="89df5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89df5-108">Parameters</span></span>

  - <span data-ttu-id="89df5-109">format</span><span class="sxs-lookup"><span data-stu-id="89df5-109">format</span></span>  
    <span data-ttu-id="89df5-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="89df5-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="89df5-111">[Chaîne](/dotnet/api/system.string) spécifiant le format à utiliser.</span><span class="sxs-lookup"><span data-stu-id="89df5-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="89df5-112">-ou-null pour utiliser le format par défaut défini pour le type de l’implémentation de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="89df5-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="89df5-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="89df5-113">formatProvider</span></span>  
    <span data-ttu-id="89df5-114">Type : [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="89df5-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="89df5-115">[IFormatProvider](/dotnet/api/system.iformatprovider) à utiliser pour mettre en forme la valeur.</span><span class="sxs-lookup"><span data-stu-id="89df5-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="89df5-116">-ou-null pour obtenir les informations de format numérique à partir des paramètres régionaux actuels du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="89df5-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89df5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89df5-117">Return value</span></span>

<span data-ttu-id="89df5-118">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="89df5-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="89df5-119">[Chaîne](/dotnet/api/system.string) contenant la valeur de l’instance actuelle au format spécifié.</span><span class="sxs-lookup"><span data-stu-id="89df5-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="89df5-120">Implémente</span><span class="sxs-lookup"><span data-stu-id="89df5-120">Implements</span></span>

[<span data-ttu-id="89df5-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="89df5-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="89df5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89df5-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89df5-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="89df5-123">Reference</span></span>

[<span data-ttu-id="89df5-124">Structure JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="89df5-124">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="89df5-125">Membres JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="89df5-125">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="89df5-126">ToString, surcharge</span><span class="sxs-lookup"><span data-stu-id="89df5-126">ToString overload</span></span>](./jet-handle.tostring-method.md)

[<span data-ttu-id="89df5-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89df5-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
