---
description: Supprime un objet attribut indexé de la collection.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributes. Remove, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525538"
---
# <a name="attributesremove-method"></a><span data-ttu-id="56c38-103">Attributes. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="56c38-103">Attributes.Remove method</span></span>

<span data-ttu-id="56c38-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56c38-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="56c38-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="56c38-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="56c38-106">La méthode **Remove** supprime un objet [**attribut**](attribute.md) indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="56c38-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c38-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56c38-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="56c38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56c38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c38-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56c38-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c38-110">Index de l’objet d' [**attribut**](attribute.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="56c38-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c38-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56c38-111">Return value</span></span>

<span data-ttu-id="56c38-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="56c38-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c38-113">Notes</span><span class="sxs-lookup"><span data-stu-id="56c38-113">Remarks</span></span>

<span data-ttu-id="56c38-114">Les applications qui utilisent cette méthode doivent contenir du code pour gérer une exception levée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="56c38-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c38-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56c38-115">Requirements</span></span>



| <span data-ttu-id="56c38-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56c38-116">Requirement</span></span> | <span data-ttu-id="56c38-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="56c38-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56c38-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="56c38-118">End of client support</span></span><br/> | <span data-ttu-id="56c38-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56c38-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56c38-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="56c38-120">End of server support</span></span><br/> | <span data-ttu-id="56c38-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56c38-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56c38-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="56c38-122">Redistributable</span></span><br/>       | <span data-ttu-id="56c38-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="56c38-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56c38-124">DLL</span><span class="sxs-lookup"><span data-stu-id="56c38-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="56c38-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56c38-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c38-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56c38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c38-127">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="56c38-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="56c38-128">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="56c38-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
