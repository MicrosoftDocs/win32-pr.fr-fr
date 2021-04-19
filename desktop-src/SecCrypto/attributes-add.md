---
description: Ajoute un objet d’attribut à la collection.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Attributes. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541498"
---
# <a name="attributesadd-method"></a><span data-ttu-id="a0449-103">Attributes. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="a0449-103">Attributes.Add method</span></span>

<span data-ttu-id="a0449-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0449-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a0449-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="a0449-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="a0449-106">La méthode **Add** ajoute un objet [**attribut**](attribute.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="a0449-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0449-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0449-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="a0449-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0449-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0449-109">*Attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0449-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0449-110">Objet d' [**attribut**](attribute.md) à ajouter à la fin de la collection.</span><span class="sxs-lookup"><span data-stu-id="a0449-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0449-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0449-111">Return value</span></span>

<span data-ttu-id="a0449-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a0449-112">This method does not return a value.</span></span> <span data-ttu-id="a0449-113">Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a0449-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0449-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0449-114">Requirements</span></span>



| <span data-ttu-id="a0449-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0449-115">Requirement</span></span> | <span data-ttu-id="a0449-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0449-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0449-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a0449-117">End of client support</span></span><br/> | <span data-ttu-id="a0449-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0449-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0449-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a0449-119">End of server support</span></span><br/> | <span data-ttu-id="a0449-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0449-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0449-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a0449-121">Redistributable</span></span><br/>       | <span data-ttu-id="a0449-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0449-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0449-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a0449-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a0449-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0449-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0449-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0449-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0449-126">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a0449-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a0449-127">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="a0449-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
