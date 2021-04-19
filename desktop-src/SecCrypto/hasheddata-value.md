---
description: Récupère les données hachées après des appels réussis à la méthode de hachage.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData. Value (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540949"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="aea5f-103">HashedData. Value (propriété)</span><span class="sxs-lookup"><span data-stu-id="aea5f-103">HashedData.Value property</span></span>

<span data-ttu-id="aea5f-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aea5f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="aea5f-105">Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="aea5f-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="aea5f-106">La propriété **valeur** récupère les données hachées après des appels réussis à la méthode de [**hachage**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="aea5f-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="aea5f-107">La valeur de hachage est retournée au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="aea5f-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="aea5f-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="aea5f-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea5f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aea5f-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="aea5f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aea5f-110">Property value</span></span>

<span data-ttu-id="aea5f-111">Chaîne qui contient les données hachées au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="aea5f-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea5f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aea5f-112">Remarks</span></span>

<span data-ttu-id="aea5f-113">Pour créer le hachage d’une grande quantité de données, appelez la méthode de [**hachage**](hasheddata-hash.md) pour chaque élément de données.</span><span class="sxs-lookup"><span data-stu-id="aea5f-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="aea5f-114">Le hachage de chaque élément de données est concaténé à la propriété **value** jusqu’à ce que la propriété soit lue.</span><span class="sxs-lookup"><span data-stu-id="aea5f-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="aea5f-115">Le contenu de la propriété **value** est réinitialisé lorsque la propriété est lue.</span><span class="sxs-lookup"><span data-stu-id="aea5f-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea5f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aea5f-116">Requirements</span></span>



| <span data-ttu-id="aea5f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aea5f-117">Requirement</span></span> | <span data-ttu-id="aea5f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea5f-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aea5f-119">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="aea5f-119">End of client support</span></span><br/> | <span data-ttu-id="aea5f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aea5f-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aea5f-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="aea5f-121">End of server support</span></span><br/> | <span data-ttu-id="aea5f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aea5f-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aea5f-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aea5f-123">Redistributable</span></span><br/>       | <span data-ttu-id="aea5f-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aea5f-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aea5f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aea5f-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="aea5f-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aea5f-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea5f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea5f-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="aea5f-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
