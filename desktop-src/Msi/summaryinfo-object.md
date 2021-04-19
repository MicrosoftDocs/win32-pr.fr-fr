---
description: L’objet SummaryInfo est utilisé pour lire, créer et mettre à jour des propriétés de document à partir du flux d’informations de synthèse d’un objet de stockage.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Objet SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535263"
---
# <a name="summaryinfo-object"></a><span data-ttu-id="daf26-103">Objet SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="daf26-103">SummaryInfo object</span></span>

<span data-ttu-id="daf26-104">L’objet **SummaryInfo** est utilisé pour lire, créer et mettre à jour des propriétés de document à partir du [flux d’informations de synthèse](summary-information-stream.md) d’un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="daf26-104">The **SummaryInfo** object is used to read, create, and update document properties from the [summary information stream](summary-information-stream.md) of a storage object.</span></span>

## <a name="members"></a><span data-ttu-id="daf26-105">Membres</span><span class="sxs-lookup"><span data-stu-id="daf26-105">Members</span></span>

<span data-ttu-id="daf26-106">L’objet **SummaryInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="daf26-106">The **SummaryInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="daf26-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="daf26-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="daf26-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="daf26-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="daf26-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="daf26-109">Methods</span></span>

<span data-ttu-id="daf26-110">L’objet **SummaryInfo** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="daf26-110">The **SummaryInfo** object has these methods.</span></span>



| <span data-ttu-id="daf26-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="daf26-111">Method</span></span>                                 | <span data-ttu-id="daf26-112">Description</span><span class="sxs-lookup"><span data-stu-id="daf26-112">Description</span></span>                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="daf26-113">**Conserver**</span><span class="sxs-lookup"><span data-stu-id="daf26-113">**Persist**</span></span>](summaryinfo-persist.md) | <span data-ttu-id="daf26-114">Met en forme et écrit les propriétés précédemment stockées dans le [flux d’informations de résumé](summary-information-stream.md)standard.</span><span class="sxs-lookup"><span data-stu-id="daf26-114">Formats and writes the previously stored properties into the standard [summary information stream](summary-information-stream.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="daf26-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="daf26-115">Properties</span></span>

<span data-ttu-id="daf26-116">L’objet **SummaryInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="daf26-116">The **SummaryInfo** object has these properties.</span></span>



| <span data-ttu-id="daf26-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="daf26-117">Property</span></span>                                                                             | <span data-ttu-id="daf26-118">Description</span><span class="sxs-lookup"><span data-stu-id="daf26-118">Description</span></span>                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="daf26-119">**Property, propriété (objet SummaryInfo)**</span><span class="sxs-lookup"><span data-stu-id="daf26-119">**Property Property (SummaryInfo Object)**</span></span>](summaryinfo-summaryinfo.md)<br/> | <span data-ttu-id="daf26-120">Obtient ou définit la valeur de la propriété spécifiée dans le flux d’informations de synthèse.</span><span class="sxs-lookup"><span data-stu-id="daf26-120">Gets or sets the value for the specified property in the summary information stream.</span></span><br/> |
| [<span data-ttu-id="daf26-121">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="daf26-121">**PropertyCount**</span></span>](summaryinfo-propertycount.md)<br/>                        | <span data-ttu-id="daf26-122">Indique le nombre actuel de valeurs de propriété dans l’objet d’informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="daf26-122">Indicates the current number of property values in the summary information object.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="daf26-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daf26-123">Requirements</span></span>



| <span data-ttu-id="daf26-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daf26-124">Requirement</span></span> | <span data-ttu-id="daf26-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="daf26-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf26-126">Version</span><span class="sxs-lookup"><span data-stu-id="daf26-126">Version</span></span><br/> | <span data-ttu-id="daf26-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="daf26-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="daf26-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="daf26-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="daf26-129">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="daf26-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="daf26-130">DLL</span><span class="sxs-lookup"><span data-stu-id="daf26-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="daf26-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf26-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="daf26-132">IID</span><span class="sxs-lookup"><span data-stu-id="daf26-132">IID</span></span><br/>     | <span data-ttu-id="daf26-133">IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="daf26-133">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="daf26-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf26-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf26-135">**Propriété SummaryInformation (objet Database)**</span><span class="sxs-lookup"><span data-stu-id="daf26-135">**SummaryInformation Property (Database Object)**</span></span>](database-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="daf26-136">**Propriété SummaryInformation (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="daf26-136">**SummaryInformation Property (Installer Object)**</span></span>](installer-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="daf26-137">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="daf26-137">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




