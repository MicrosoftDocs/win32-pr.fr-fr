---
description: Récupère le nombre d’objets attribute dans la collection.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537540"
---
# <a name="attributescount-property"></a><span data-ttu-id="7966c-103">Attributes. Count, propriété</span><span class="sxs-lookup"><span data-stu-id="7966c-103">Attributes.Count property</span></span>

<span data-ttu-id="7966c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7966c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7966c-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="7966c-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="7966c-106">La propriété **Count** récupère le nombre d’objets [**attribute**](attribute.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="7966c-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="7966c-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7966c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7966c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7966c-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="7966c-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7966c-109">Property value</span></span>

<span data-ttu-id="7966c-110">Nombre d’objets [**attribute**](attribute.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="7966c-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="7966c-111">Chaque objet d' **attribut** représente un attribut unique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="7966c-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7966c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7966c-112">Remarks</span></span>

<span data-ttu-id="7966c-113">La propriété **Count** peut être utilisée pour spécifier le dernier objet d' [**attribut**](attribute.md) dans la collection lors de la récupération d’un objet **attribut** spécifique à l’aide de la propriété Attributes [**. Item**](attributes-item.md) .</span><span class="sxs-lookup"><span data-stu-id="7966c-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7966c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7966c-114">Requirements</span></span>



| <span data-ttu-id="7966c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7966c-115">Requirement</span></span> | <span data-ttu-id="7966c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7966c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7966c-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7966c-117">End of client support</span></span><br/> | <span data-ttu-id="7966c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7966c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7966c-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7966c-119">End of server support</span></span><br/> | <span data-ttu-id="7966c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7966c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7966c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7966c-121">Redistributable</span></span><br/>       | <span data-ttu-id="7966c-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7966c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7966c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7966c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7966c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7966c-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7966c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7966c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7966c-126">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="7966c-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
