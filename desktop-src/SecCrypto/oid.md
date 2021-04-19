---
description: Représente un identificateur d’objet (OID) utilisé par plusieurs propriétés CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objet OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542786"
---
# <a name="oid-object"></a><span data-ttu-id="72a97-103">Objet OID</span><span class="sxs-lookup"><span data-stu-id="72a97-103">OID object</span></span>

<span data-ttu-id="72a97-104">\[L’objet **OID** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="72a97-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72a97-105">Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="72a97-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="72a97-106">L’objet **OID** représente un [*identificateur d’objet*](../secgloss/o-gly.md) (OID) utilisé par plusieurs propriétés CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="72a97-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="72a97-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="72a97-107">When to use</span></span>

<span data-ttu-id="72a97-108">L’objet **OID** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="72a97-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="72a97-109">Définissez ou récupérez un nom de CAPICOM et un nom d’affichage pour l’OID.</span><span class="sxs-lookup"><span data-stu-id="72a97-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="72a97-110">Définissez ou récupérez le nombre en pointillés de l’OID.</span><span class="sxs-lookup"><span data-stu-id="72a97-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="72a97-111">Membres</span><span class="sxs-lookup"><span data-stu-id="72a97-111">Members</span></span>

<span data-ttu-id="72a97-112">L’objet **OID** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="72a97-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="72a97-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72a97-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72a97-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72a97-114">Properties</span></span>

<span data-ttu-id="72a97-115">L’objet **OID** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="72a97-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="72a97-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="72a97-116">Property</span></span>                                            | <span data-ttu-id="72a97-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="72a97-117">Access type</span></span>           | <span data-ttu-id="72a97-118">Description</span><span class="sxs-lookup"><span data-stu-id="72a97-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72a97-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="72a97-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="72a97-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72a97-120">Read/write</span></span><br/> | <span data-ttu-id="72a97-121">Définit ou récupère le nom complet de l’OID.</span><span class="sxs-lookup"><span data-stu-id="72a97-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="72a97-122">**Nom**</span><span class="sxs-lookup"><span data-stu-id="72a97-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="72a97-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72a97-123">Read/write</span></span><br/> | <span data-ttu-id="72a97-124">Définit ou récupère le nom défini par CAPICOM pour l’OID.</span><span class="sxs-lookup"><span data-stu-id="72a97-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="72a97-125">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="72a97-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="72a97-126">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="72a97-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="72a97-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72a97-127">Read/write</span></span><br/> | <span data-ttu-id="72a97-128">Définit ou récupère la valeur du numéro d’OID en pointillés de l’OID.</span><span class="sxs-lookup"><span data-stu-id="72a97-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="72a97-129">Notes</span><span class="sxs-lookup"><span data-stu-id="72a97-129">Remarks</span></span>

<span data-ttu-id="72a97-130">L’objet **OID** peut être créé et il est sécurisé pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="72a97-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="72a97-131">Le ProgID de l’objet **OID** est CAPICOM. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="72a97-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="72a97-132">Les propriétés suivantes de l’objet CAPICOM retournent un objet **OID** :</span><span class="sxs-lookup"><span data-stu-id="72a97-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="72a97-133">**PolicyInformation. OID**</span><span class="sxs-lookup"><span data-stu-id="72a97-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="72a97-134">**Qualificateur. OID**</span><span class="sxs-lookup"><span data-stu-id="72a97-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="72a97-135">**Extension. OID**</span><span class="sxs-lookup"><span data-stu-id="72a97-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="72a97-136">**Modèle. OID**</span><span class="sxs-lookup"><span data-stu-id="72a97-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="72a97-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72a97-137">Requirements</span></span>



| <span data-ttu-id="72a97-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72a97-138">Requirement</span></span> | <span data-ttu-id="72a97-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="72a97-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72a97-140">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="72a97-140">Redistributable</span></span><br/> | <span data-ttu-id="72a97-141">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="72a97-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="72a97-142">DLL</span><span class="sxs-lookup"><span data-stu-id="72a97-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="72a97-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72a97-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
