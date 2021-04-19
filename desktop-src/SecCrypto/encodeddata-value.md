---
description: Récupère les données encodées.
ms.assetid: 8e07ac14-6859-410f-ab30-84b8d60a94ad
title: EncodedData. Value (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e040f78d5c0ccfa3e50729f16b75a0691771980e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534900"
---
# <a name="encodeddatavalue-property"></a><span data-ttu-id="d0da1-103">EncodedData. Value (propriété)</span><span class="sxs-lookup"><span data-stu-id="d0da1-103">EncodedData.Value property</span></span>

<span data-ttu-id="d0da1-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d0da1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d0da1-105">Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d0da1-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d0da1-106">La propriété **value** récupère les données encodées.</span><span class="sxs-lookup"><span data-stu-id="d0da1-106">The **Value** property retrieves the encoded data.</span></span> <span data-ttu-id="d0da1-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0da1-107">This is the default property.</span></span>

<span data-ttu-id="d0da1-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d0da1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0da1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0da1-109">Syntax</span></span>


```VB
EncodedData.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="d0da1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d0da1-110">Property value</span></span>

<span data-ttu-id="d0da1-111">Chaîne qui contient les données encodées.</span><span class="sxs-lookup"><span data-stu-id="d0da1-111">A string that contains the encoded data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0da1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0da1-112">Requirements</span></span>



| <span data-ttu-id="d0da1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0da1-113">Requirement</span></span> | <span data-ttu-id="d0da1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0da1-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0da1-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d0da1-115">End of client support</span></span><br/> | <span data-ttu-id="d0da1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0da1-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d0da1-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d0da1-117">End of server support</span></span><br/> | <span data-ttu-id="d0da1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0da1-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d0da1-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d0da1-119">Redistributable</span></span><br/>       | <span data-ttu-id="d0da1-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0da1-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d0da1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d0da1-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d0da1-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0da1-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
