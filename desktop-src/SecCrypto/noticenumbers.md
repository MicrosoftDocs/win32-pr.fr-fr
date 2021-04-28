---
description: 'Objet NoticeNumbers : représente une collection d’objets d’extension.'
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objet NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090757"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="254a6-103">Objet NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="254a6-103">NoticeNumbers object</span></span>

<span data-ttu-id="254a6-104">\[L’objet **NoticeNumbers** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="254a6-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="254a6-105">Pour plus d’informations, consultez [**qualifier**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="254a6-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="254a6-106">L’objet **NoticeNumbers** représente une collection d’objets d' [**extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="254a6-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="254a6-107">Chaque objet d' [**extension**](extension.md) représente un numéro d’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="254a6-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="254a6-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="254a6-108">When to use</span></span>

<span data-ttu-id="254a6-109">L’objet **NoticeNumbers** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="254a6-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="254a6-110">Récupérez le nombre d’objets d' [**extension**](extension.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="254a6-111">Récupérez un objet d' [**extension**](extension.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="254a6-112">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="254a6-113">Membres</span><span class="sxs-lookup"><span data-stu-id="254a6-113">Members</span></span>

<span data-ttu-id="254a6-114">L’objet **NoticeNumbers** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="254a6-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="254a6-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="254a6-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="254a6-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="254a6-116">Properties</span></span>

<span data-ttu-id="254a6-117">L’objet **NoticeNumbers** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="254a6-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="254a6-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="254a6-118">Property</span></span>                                              | <span data-ttu-id="254a6-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="254a6-119">Access type</span></span>          | <span data-ttu-id="254a6-120">Description</span><span class="sxs-lookup"><span data-stu-id="254a6-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="254a6-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="254a6-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="254a6-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="254a6-122">Read-only</span></span><br/> | <span data-ttu-id="254a6-123">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="254a6-124">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="254a6-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="254a6-125">**Saut**</span><span class="sxs-lookup"><span data-stu-id="254a6-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="254a6-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="254a6-126">Read-only</span></span><br/> | <span data-ttu-id="254a6-127">Récupère le nombre d’objets d' [**extension**](extension.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="254a6-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="254a6-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="254a6-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="254a6-129">Read-only</span></span><br/> | <span data-ttu-id="254a6-130">Récupère l’objet d' [**extension**](extension.md) qui représente le numéro d’avis indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="254a6-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="254a6-131">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="254a6-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="254a6-132">Notes </span><span class="sxs-lookup"><span data-stu-id="254a6-132">Remarks</span></span>

<span data-ttu-id="254a6-133">Impossible de créer l’objet **NoticeNumbers** .</span><span class="sxs-lookup"><span data-stu-id="254a6-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="254a6-134">L’objet NoticeNumbers est utilisé dans la propriété [**qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="254a6-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="254a6-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="254a6-135">Requirements</span></span>



| <span data-ttu-id="254a6-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="254a6-136">Requirement</span></span> | <span data-ttu-id="254a6-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="254a6-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="254a6-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="254a6-138">Redistributable</span></span><br/> | <span data-ttu-id="254a6-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="254a6-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="254a6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="254a6-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="254a6-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="254a6-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
