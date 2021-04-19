---
description: Efface tous les objets attribut de la collection.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Attributes. Clear, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525543"
---
# <a name="attributesclear-method"></a><span data-ttu-id="9f652-103">Attributes. Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="9f652-103">Attributes.Clear method</span></span>

<span data-ttu-id="9f652-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f652-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="9f652-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="9f652-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="9f652-106">La méthode **Clear** efface tous les objets [**attribut**](attribute.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="9f652-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f652-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f652-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="9f652-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f652-108">Parameters</span></span>

<span data-ttu-id="9f652-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9f652-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f652-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f652-110">Return value</span></span>

<span data-ttu-id="9f652-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f652-111">This method does not return a value.</span></span> <span data-ttu-id="9f652-112">Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9f652-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f652-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f652-113">Requirements</span></span>



| <span data-ttu-id="9f652-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f652-114">Requirement</span></span> | <span data-ttu-id="9f652-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f652-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f652-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9f652-116">End of client support</span></span><br/> | <span data-ttu-id="9f652-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f652-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9f652-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9f652-118">End of server support</span></span><br/> | <span data-ttu-id="9f652-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f652-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9f652-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9f652-120">Redistributable</span></span><br/>       | <span data-ttu-id="9f652-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f652-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9f652-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9f652-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9f652-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f652-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f652-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f652-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f652-125">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9f652-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="9f652-126">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="9f652-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
