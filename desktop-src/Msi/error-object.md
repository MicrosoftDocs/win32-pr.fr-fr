---
description: L’objet Error retourne les informations d’une erreur de fusion unique.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objet Error (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540386"
---
# <a name="error-object"></a><span data-ttu-id="1c742-103">Objet d’erreur</span><span class="sxs-lookup"><span data-stu-id="1c742-103">Error object</span></span>

<span data-ttu-id="1c742-104">L’objet **Error** retourne les informations d’une erreur de fusion unique.</span><span class="sxs-lookup"><span data-stu-id="1c742-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="1c742-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1c742-105">Members</span></span>

<span data-ttu-id="1c742-106">L’objet **Error** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c742-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="1c742-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c742-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c742-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c742-108">Properties</span></span>

<span data-ttu-id="1c742-109">L’objet **Error** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c742-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="1c742-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="1c742-110">Property</span></span>                                                | <span data-ttu-id="1c742-111">Description</span><span class="sxs-lookup"><span data-stu-id="1c742-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c742-112">**DatabaseKeys**</span><span class="sxs-lookup"><span data-stu-id="1c742-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="1c742-113">Retourne les clés primaires de la ligne dans la table de base de données qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="1c742-114">**DatabaseTable**</span><span class="sxs-lookup"><span data-stu-id="1c742-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="1c742-115">Retourne le nom de table de la table dans la base de données à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="1c742-116">**Language**</span><span class="sxs-lookup"><span data-stu-id="1c742-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="1c742-117">Retourne la langue de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="1c742-118">**ModuleKeys**</span><span class="sxs-lookup"><span data-stu-id="1c742-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="1c742-119">Retourne les clés primaires de la ligne dans la table de module qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="1c742-120">**ModuleTable**</span><span class="sxs-lookup"><span data-stu-id="1c742-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="1c742-121">Retourne le nom de table de la table dans le module à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="1c742-122">**D**</span><span class="sxs-lookup"><span data-stu-id="1c742-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="1c742-123">Retourne le chemin d’accès au fichier ou au répertoire à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="1c742-124">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="1c742-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="1c742-125">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="1c742-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="1c742-126">Retourne le type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c742-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="1c742-127">C++</span><span class="sxs-lookup"><span data-stu-id="1c742-127">C++</span></span>

<span data-ttu-id="1c742-128">interface **IMsmError : IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1c742-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="1c742-129">ID d’interface</span><span class="sxs-lookup"><span data-stu-id="1c742-129">Interface ID</span></span>



| <span data-ttu-id="1c742-130">Constante</span><span class="sxs-lookup"><span data-stu-id="1c742-130">Constant</span></span>           | <span data-ttu-id="1c742-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c742-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="1c742-132">**IID \_ IMsmError**</span><span class="sxs-lookup"><span data-stu-id="1c742-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="1c742-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="1c742-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1c742-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c742-134">Requirements</span></span>



| <span data-ttu-id="1c742-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c742-135">Requirement</span></span> | <span data-ttu-id="1c742-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c742-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c742-137">Version</span><span class="sxs-lookup"><span data-stu-id="1c742-137">Version</span></span><br/> | <span data-ttu-id="1c742-138">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1c742-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1c742-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c742-139">Header</span></span><br/>  | <dl> <span data-ttu-id="1c742-140"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c742-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c742-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1c742-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c742-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c742-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




