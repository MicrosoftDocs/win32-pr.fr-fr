---
description: 'En savoir plus sur : JET_DBID. ToString, méthode (String, IFormatProvider)'
title: JET_DBID. ToString, méthode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f9c950c86e4f749c7889fcf6914b8294850f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513215"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a><span data-ttu-id="233bd-103">JET_DBID. ToString, méthode (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="233bd-103">JET_DBID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="233bd-104">Met en forme la valeur de l’instance actuelle en utilisant le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="233bd-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="233bd-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="233bd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="233bd-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="233bd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="233bd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="233bd-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_DBID
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

#### <a name="parameters"></a><span data-ttu-id="233bd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="233bd-108">Parameters</span></span>

  - <span data-ttu-id="233bd-109">format</span><span class="sxs-lookup"><span data-stu-id="233bd-109">format</span></span>  
    <span data-ttu-id="233bd-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="233bd-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="233bd-111">[Chaîne](/dotnet/api/system.string) spécifiant le format à utiliser.</span><span class="sxs-lookup"><span data-stu-id="233bd-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="233bd-112">-ou-null pour utiliser le format par défaut défini pour le type de l’implémentation de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="233bd-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="233bd-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="233bd-113">formatProvider</span></span>  
    <span data-ttu-id="233bd-114">Type : [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="233bd-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="233bd-115">[IFormatProvider](/dotnet/api/system.iformatprovider) à utiliser pour mettre en forme la valeur.</span><span class="sxs-lookup"><span data-stu-id="233bd-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="233bd-116">-ou-null pour obtenir les informations de format numérique à partir des paramètres régionaux actuels du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="233bd-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="233bd-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="233bd-117">Return value</span></span>

<span data-ttu-id="233bd-118">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="233bd-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="233bd-119">[Chaîne](/dotnet/api/system.string) contenant la valeur de l’instance actuelle au format spécifié.</span><span class="sxs-lookup"><span data-stu-id="233bd-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="233bd-120">Implémente</span><span class="sxs-lookup"><span data-stu-id="233bd-120">Implements</span></span>

[<span data-ttu-id="233bd-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="233bd-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="233bd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="233bd-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="233bd-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="233bd-123">Reference</span></span>

[<span data-ttu-id="233bd-124">Structure JET_DBID</span><span class="sxs-lookup"><span data-stu-id="233bd-124">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="233bd-125">Membres JET_DBID</span><span class="sxs-lookup"><span data-stu-id="233bd-125">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="233bd-126">ToString, surcharge</span><span class="sxs-lookup"><span data-stu-id="233bd-126">ToString overload</span></span>](./jet-dbid.tostring-method.md)

[<span data-ttu-id="233bd-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="233bd-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
