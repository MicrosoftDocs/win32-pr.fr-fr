---
description: 'En savoir plus sur : JET_TABLEID. ToString, méthode (String, IFormatProvider)'
title: JET_TABLEID. ToString, méthode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e8d57d572a44f04c5b76ffb11f5243f7afb2b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520666"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a><span data-ttu-id="70b47-103">JET_TABLEID. ToString, méthode (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="70b47-103">JET_TABLEID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="70b47-104">Met en forme la valeur de l’instance actuelle en utilisant le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="70b47-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="70b47-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="70b47-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="70b47-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="70b47-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="70b47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70b47-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
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

#### <a name="parameters"></a><span data-ttu-id="70b47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70b47-108">Parameters</span></span>

  - <span data-ttu-id="70b47-109">format</span><span class="sxs-lookup"><span data-stu-id="70b47-109">format</span></span>  
    <span data-ttu-id="70b47-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="70b47-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="70b47-111">[Chaîne](/dotnet/api/system.string) spécifiant le format à utiliser ; ou valeur null pour utiliser le format par défaut défini pour le type de l’implémentation de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="70b47-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="70b47-112">formatProvider</span><span class="sxs-lookup"><span data-stu-id="70b47-112">formatProvider</span></span>  
    <span data-ttu-id="70b47-113">Type : [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="70b47-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="70b47-114">[IFormatProvider](/dotnet/api/system.iformatprovider) à utiliser pour mettre en forme la valeur ; ou, NULL pour obtenir les informations de format numérique à partir des paramètres régionaux actuels du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="70b47-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="70b47-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70b47-115">Return value</span></span>

<span data-ttu-id="70b47-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="70b47-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="70b47-117">[Chaîne](/dotnet/api/system.string) contenant la valeur de l’instance actuelle au format spécifié.</span><span class="sxs-lookup"><span data-stu-id="70b47-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="70b47-118">Implémente</span><span class="sxs-lookup"><span data-stu-id="70b47-118">Implements</span></span>

[<span data-ttu-id="70b47-119">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="70b47-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="70b47-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70b47-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70b47-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="70b47-121">Reference</span></span>

[<span data-ttu-id="70b47-122">Structure JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70b47-122">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="70b47-123">Membres JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70b47-123">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="70b47-124">ToString, surcharge</span><span class="sxs-lookup"><span data-stu-id="70b47-124">ToString overload</span></span>](./jet-tableid.tostring-method.md)

[<span data-ttu-id="70b47-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="70b47-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
