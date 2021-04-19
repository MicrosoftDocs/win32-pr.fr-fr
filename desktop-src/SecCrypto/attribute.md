---
description: Représente un attribut authentifié unique.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521742"
---
# <a name="attribute-object"></a><span data-ttu-id="be9b9-103">Attribute (objet)</span><span class="sxs-lookup"><span data-stu-id="be9b9-103">Attribute object</span></span>

<span data-ttu-id="be9b9-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="be9b9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="be9b9-105">Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="be9b9-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="be9b9-106">L’objet d' **attribut** représente un attribut authentifié unique.</span><span class="sxs-lookup"><span data-stu-id="be9b9-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="be9b9-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="be9b9-107">When to use</span></span>

<span data-ttu-id="be9b9-108">L’objet **attribut** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="be9b9-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="be9b9-109">Définissez ou récupérez le nom CAPICOM de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="be9b9-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="be9b9-110">Définissez ou récupérez la valeur de l’attribut, par exemple la durée de signature, le nom du document signé ou une description du document signé.</span><span class="sxs-lookup"><span data-stu-id="be9b9-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="be9b9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="be9b9-111">Members</span></span>

<span data-ttu-id="be9b9-112">L’objet **attribut** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be9b9-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="be9b9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be9b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be9b9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be9b9-114">Properties</span></span>

<span data-ttu-id="be9b9-115">L’objet **attribut** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="be9b9-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="be9b9-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="be9b9-116">Property</span></span>                                    | <span data-ttu-id="be9b9-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="be9b9-117">Access type</span></span>           | <span data-ttu-id="be9b9-118">Description</span><span class="sxs-lookup"><span data-stu-id="be9b9-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be9b9-119">**Nom**</span><span class="sxs-lookup"><span data-stu-id="be9b9-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="be9b9-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be9b9-120">Read/write</span></span><br/> | <span data-ttu-id="be9b9-121">Définit ou récupère le nom CAPICOM de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="be9b9-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="be9b9-122">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="be9b9-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="be9b9-123">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="be9b9-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="be9b9-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="be9b9-124">Read/write</span></span><br/> | <span data-ttu-id="be9b9-125">Définit ou récupère la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="be9b9-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="be9b9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="be9b9-126">Remarks</span></span>

<span data-ttu-id="be9b9-127">L’objet d' **attribut** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="be9b9-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="be9b9-128">Le ProgID de l’objet **attribut** est CAPICOM. Attribut. 1.</span><span class="sxs-lookup"><span data-stu-id="be9b9-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9b9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be9b9-129">Requirements</span></span>



| <span data-ttu-id="be9b9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be9b9-130">Requirement</span></span> | <span data-ttu-id="be9b9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="be9b9-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9b9-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="be9b9-132">End of client support</span></span><br/> | <span data-ttu-id="be9b9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be9b9-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="be9b9-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="be9b9-134">End of server support</span></span><br/> | <span data-ttu-id="be9b9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be9b9-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="be9b9-136">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="be9b9-136">Redistributable</span></span><br/>       | <span data-ttu-id="be9b9-137">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="be9b9-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="be9b9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="be9b9-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="be9b9-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9b9-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9b9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9b9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9b9-141">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="be9b9-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
