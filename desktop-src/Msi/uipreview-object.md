---
description: L’objet UIPreview est utilisé pour afficher les boîtes de dialogue et les panneaux de l’interface utilisateur lors de la création. Cet objet est créé par la méthode EnableUIPreview de l’objet de base de données.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objet UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537496"
---
# <a name="uipreview-object"></a><span data-ttu-id="dfce0-104">Objet UIPreview</span><span class="sxs-lookup"><span data-stu-id="dfce0-104">UIPreview object</span></span>

<span data-ttu-id="dfce0-105">L’objet **UIPreview** est utilisé pour afficher les boîtes de dialogue et les panneaux de l’interface utilisateur lors de la création.</span><span class="sxs-lookup"><span data-stu-id="dfce0-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="dfce0-106">Cet objet est créé par la méthode [**EnableUIPreview**](database-enableuipreview.md) de l’objet [**de base de données**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="dfce0-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="dfce0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="dfce0-107">Members</span></span>

<span data-ttu-id="dfce0-108">L’objet **UIPreview** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dfce0-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="dfce0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfce0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dfce0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dfce0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dfce0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfce0-111">Methods</span></span>

<span data-ttu-id="dfce0-112">L’objet **UIPreview** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dfce0-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="dfce0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="dfce0-113">Method</span></span>                                           | <span data-ttu-id="dfce0-114">Description</span><span class="sxs-lookup"><span data-stu-id="dfce0-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfce0-115">**ViewBillboard**</span><span class="sxs-lookup"><span data-stu-id="dfce0-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="dfce0-116">Affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="dfce0-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="dfce0-117">**ViewDialog**</span><span class="sxs-lookup"><span data-stu-id="dfce0-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="dfce0-118">Affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="dfce0-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="dfce0-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dfce0-119">Properties</span></span>

<span data-ttu-id="dfce0-120">L’objet **UIPreview** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dfce0-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="dfce0-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="dfce0-121">Property</span></span>                                          | <span data-ttu-id="dfce0-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="dfce0-122">Access type</span></span>           | <span data-ttu-id="dfce0-123">Description</span><span class="sxs-lookup"><span data-stu-id="dfce0-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfce0-124">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="dfce0-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="dfce0-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dfce0-125">Read/write</span></span><br/> | <span data-ttu-id="dfce0-126">Représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="dfce0-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dfce0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfce0-127">Requirements</span></span>



| <span data-ttu-id="dfce0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfce0-128">Requirement</span></span> | <span data-ttu-id="dfce0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfce0-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfce0-130">Version</span><span class="sxs-lookup"><span data-stu-id="dfce0-130">Version</span></span><br/> | <span data-ttu-id="dfce0-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dfce0-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dfce0-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfce0-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dfce0-133">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="dfce0-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dfce0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dfce0-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="dfce0-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfce0-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dfce0-136">IID</span><span class="sxs-lookup"><span data-stu-id="dfce0-136">IID</span></span><br/>     | <span data-ttu-id="dfce0-137">IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dfce0-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="dfce0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfce0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfce0-139">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dfce0-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




