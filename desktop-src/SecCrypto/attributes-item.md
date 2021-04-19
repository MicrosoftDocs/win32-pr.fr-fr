---
description: Récupère l’objet d’attribut qui représente l’attribut indexé.
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Attributes. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 208e36fd8d4d7e3effc2c0f59b7db921fed76d79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528557"
---
# <a name="attributesitem-property"></a><span data-ttu-id="bb61f-103">Attributes. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="bb61f-103">Attributes.Item property</span></span>

<span data-ttu-id="bb61f-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb61f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="bb61f-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="bb61f-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bb61f-106">La propriété **Item** récupère l’objet [**attribut**](attribute.md) qui représente l’attribut indexé.</span><span class="sxs-lookup"><span data-stu-id="bb61f-106">The **Item** property retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="bb61f-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb61f-107">This is the default property.</span></span>

<span data-ttu-id="bb61f-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bb61f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb61f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb61f-109">Syntax</span></span>


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="bb61f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bb61f-110">Property value</span></span>

<span data-ttu-id="bb61f-111">Objet d' [**attribut**](attribute.md) qui représente l’attribut indexé.</span><span class="sxs-lookup"><span data-stu-id="bb61f-111">An [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb61f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb61f-112">Requirements</span></span>



| <span data-ttu-id="bb61f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb61f-113">Requirement</span></span> | <span data-ttu-id="bb61f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb61f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb61f-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bb61f-115">End of client support</span></span><br/> | <span data-ttu-id="bb61f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb61f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb61f-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bb61f-117">End of server support</span></span><br/> | <span data-ttu-id="bb61f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb61f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb61f-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bb61f-119">Redistributable</span></span><br/>       | <span data-ttu-id="bb61f-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb61f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb61f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bb61f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bb61f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb61f-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
