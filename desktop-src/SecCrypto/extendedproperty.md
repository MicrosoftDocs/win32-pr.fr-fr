---
description: Représente une propriété étendue Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objet ExtendedProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530972"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="18889-103">Objet ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="18889-103">ExtendedProperty object</span></span>

<span data-ttu-id="18889-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18889-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="18889-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="18889-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="18889-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="18889-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="18889-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="18889-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="18889-108">L’objet **ExtendedProperty** représente une propriété étendue Microsoft.</span><span class="sxs-lookup"><span data-stu-id="18889-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="18889-109">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="18889-109">When to use</span></span>

<span data-ttu-id="18889-110">L’objet **ExtendedProperty** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="18889-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="18889-111">Définissez ou récupérez le type de la propriété étendue.</span><span class="sxs-lookup"><span data-stu-id="18889-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="18889-112">Définissez ou récupérez le type d’encodage utilisé pour encoder la propriété étendue.</span><span class="sxs-lookup"><span data-stu-id="18889-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="18889-113">Membres</span><span class="sxs-lookup"><span data-stu-id="18889-113">Members</span></span>

<span data-ttu-id="18889-114">L’objet **ExtendedProperty** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18889-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="18889-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18889-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18889-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18889-116">Properties</span></span>

<span data-ttu-id="18889-117">L’objet **ExtendedProperty** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="18889-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="18889-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="18889-118">Property</span></span>                                             | <span data-ttu-id="18889-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="18889-119">Access type</span></span>           | <span data-ttu-id="18889-120">Description</span><span class="sxs-lookup"><span data-stu-id="18889-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18889-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="18889-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="18889-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18889-122">Read/write</span></span><br/> | <span data-ttu-id="18889-123">Valeur de l’énumération [**\_ propid propid**](capicom-propid.md) qui définit ou récupère le type de la propriété étendue.</span><span class="sxs-lookup"><span data-stu-id="18889-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="18889-124">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="18889-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="18889-125">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="18889-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="18889-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18889-126">Read/write</span></span><br/> | <span data-ttu-id="18889-127">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui définit ou récupère les données de propriété étendues.</span><span class="sxs-lookup"><span data-stu-id="18889-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="18889-128">Notes</span><span class="sxs-lookup"><span data-stu-id="18889-128">Remarks</span></span>

<span data-ttu-id="18889-129">L’objet **ExtendedProperty** est utilisé par la collection [**ExtendedProperties**](extendedproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="18889-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="18889-130">L’objet **ExtendedProperty** peut être créé et il n’est pas sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="18889-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="18889-131">Le ProgID de l’objet **ExtendedProperty** est CAPICOM. ExtendedProperty. 1.</span><span class="sxs-lookup"><span data-stu-id="18889-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="18889-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18889-132">Requirements</span></span>



| <span data-ttu-id="18889-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18889-133">Requirement</span></span> | <span data-ttu-id="18889-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="18889-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18889-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="18889-135">End of client support</span></span><br/> | <span data-ttu-id="18889-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18889-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18889-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="18889-137">End of server support</span></span><br/> | <span data-ttu-id="18889-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18889-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18889-139">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="18889-139">Redistributable</span></span><br/>       | <span data-ttu-id="18889-140">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="18889-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="18889-141">DLL</span><span class="sxs-lookup"><span data-stu-id="18889-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="18889-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18889-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
