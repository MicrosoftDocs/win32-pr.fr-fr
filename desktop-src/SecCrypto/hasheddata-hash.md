---
description: Crée un hachage de la chaîne spécifiée.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData. Hash, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542481"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="19fbc-103">HashedData. Hash, méthode</span><span class="sxs-lookup"><span data-stu-id="19fbc-103">HashedData.Hash method</span></span>

<span data-ttu-id="19fbc-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19fbc-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="19fbc-105">Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="19fbc-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="19fbc-106">La méthode de **hachage** crée un hachage de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="19fbc-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19fbc-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="19fbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19fbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fbc-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="19fbc-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="19fbc-110">Chaîne qui contient la valeur à hacher.</span><span class="sxs-lookup"><span data-stu-id="19fbc-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fbc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19fbc-111">Return value</span></span>

<span data-ttu-id="19fbc-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="19fbc-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19fbc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="19fbc-113">Remarks</span></span>

<span data-ttu-id="19fbc-114">Pour créer le hachage d’une grande quantité de données, appelez la méthode de **hachage** pour chaque élément de données.</span><span class="sxs-lookup"><span data-stu-id="19fbc-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="19fbc-115">Le hachage de chaque élément de données est concaténé à la propriété [**value**](hasheddata-value.md) jusqu’à ce que la propriété soit lue.</span><span class="sxs-lookup"><span data-stu-id="19fbc-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="19fbc-116">Le contenu de la propriété **value** est réinitialisé lorsque la propriété est lue.</span><span class="sxs-lookup"><span data-stu-id="19fbc-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="19fbc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19fbc-117">Requirements</span></span>



| <span data-ttu-id="19fbc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19fbc-118">Requirement</span></span> | <span data-ttu-id="19fbc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="19fbc-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19fbc-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="19fbc-120">End of client support</span></span><br/> | <span data-ttu-id="19fbc-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19fbc-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19fbc-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="19fbc-122">End of server support</span></span><br/> | <span data-ttu-id="19fbc-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19fbc-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19fbc-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="19fbc-124">Redistributable</span></span><br/>       | <span data-ttu-id="19fbc-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="19fbc-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19fbc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19fbc-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="19fbc-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19fbc-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
