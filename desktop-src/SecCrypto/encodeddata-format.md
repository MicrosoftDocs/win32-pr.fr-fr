---
description: Retourne une représentation sous forme de chaîne des données encodées.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData. format, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523441"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="e54d3-103">EncodedData. format, méthode</span><span class="sxs-lookup"><span data-stu-id="e54d3-103">EncodedData.Format method</span></span>

<span data-ttu-id="e54d3-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e54d3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e54d3-105">Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e54d3-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e54d3-106">La méthode **format** retourne une représentation sous forme de chaîne des données encodées.</span><span class="sxs-lookup"><span data-stu-id="e54d3-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e54d3-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e54d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e54d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54d3-109">*bMultiLines* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e54d3-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e54d3-110">Valeur booléenne qui indique si la chaîne retournée contient plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="e54d3-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="e54d3-111">Si la **valeur est true**, la chaîne retournée peut contenir plusieurs lignes séparées par **vbCrLf**.</span><span class="sxs-lookup"><span data-stu-id="e54d3-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="e54d3-112">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="e54d3-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e54d3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e54d3-113">Return value</span></span>

<span data-ttu-id="e54d3-114">Chaîne explicite qui représente les données encodées.</span><span class="sxs-lookup"><span data-stu-id="e54d3-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="e54d3-115">Si CAPICOM ne comprend pas les données encodées, une représentation hexadécimale des données est retournée.</span><span class="sxs-lookup"><span data-stu-id="e54d3-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e54d3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e54d3-116">Remarks</span></span>

<span data-ttu-id="e54d3-117">Le format de la chaîne retournée peut changer entre les différentes versions de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="e54d3-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="e54d3-118">Ne vous fiez pas à un format particulier dans votre application.</span><span class="sxs-lookup"><span data-stu-id="e54d3-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54d3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e54d3-119">Requirements</span></span>



| <span data-ttu-id="e54d3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e54d3-120">Requirement</span></span> | <span data-ttu-id="e54d3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e54d3-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e54d3-122">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e54d3-122">End of client support</span></span><br/> | <span data-ttu-id="e54d3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e54d3-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e54d3-124">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e54d3-124">End of server support</span></span><br/> | <span data-ttu-id="e54d3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e54d3-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e54d3-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e54d3-126">Redistributable</span></span><br/>       | <span data-ttu-id="e54d3-127">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e54d3-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e54d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e54d3-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e54d3-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e54d3-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54d3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e54d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54d3-131">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="e54d3-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
