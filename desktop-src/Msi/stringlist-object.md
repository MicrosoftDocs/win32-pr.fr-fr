---
description: L’objet StringList est une collection de chaînes. Le client doit vérifier que l’objet StringList existe et n’est pas vide avant de référencer ses propriétés.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Objet StringList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530523"
---
# <a name="stringlist-object"></a><span data-ttu-id="62b3f-104">Objet StringList</span><span class="sxs-lookup"><span data-stu-id="62b3f-104">StringList object</span></span>

<span data-ttu-id="62b3f-105">L’objet **StringList** est une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="62b3f-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="62b3f-106">Le client doit vérifier que l’objet **StringList** existe et n’est pas vide avant de référencer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="62b3f-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="62b3f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="62b3f-107">Members</span></span>

<span data-ttu-id="62b3f-108">L’objet **StringList** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="62b3f-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="62b3f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62b3f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62b3f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62b3f-110">Properties</span></span>

<span data-ttu-id="62b3f-111">L’objet **StringList** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="62b3f-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="62b3f-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="62b3f-112">Property</span></span>                                     | <span data-ttu-id="62b3f-113">Description</span><span class="sxs-lookup"><span data-stu-id="62b3f-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="62b3f-114">**Saut**</span><span class="sxs-lookup"><span data-stu-id="62b3f-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="62b3f-115">Retourne le nombre d’éléments dans l’objet **StringList** .</span><span class="sxs-lookup"><span data-stu-id="62b3f-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="62b3f-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62b3f-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="62b3f-117">Retourne une chaîne dans la collection d’objets **StringList** .</span><span class="sxs-lookup"><span data-stu-id="62b3f-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="62b3f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62b3f-118">Requirements</span></span>



| <span data-ttu-id="62b3f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62b3f-119">Requirement</span></span> | <span data-ttu-id="62b3f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="62b3f-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b3f-121">Version</span><span class="sxs-lookup"><span data-stu-id="62b3f-121">Version</span></span><br/> | <span data-ttu-id="62b3f-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62b3f-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62b3f-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62b3f-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62b3f-124">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="62b3f-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="62b3f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="62b3f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="62b3f-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62b3f-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="62b3f-127">IID</span><span class="sxs-lookup"><span data-stu-id="62b3f-127">IID</span></span><br/>     | <span data-ttu-id="62b3f-128">IID \_ IStringList est défini en tant que 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="62b3f-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="62b3f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b3f-130">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="62b3f-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




