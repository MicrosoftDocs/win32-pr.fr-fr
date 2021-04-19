---
description: L’objet Component représente une instance unique d’un composant qui est disponible pour l’énumération.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objet composant
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537500"
---
# <a name="component-object"></a><span data-ttu-id="93426-103">Objet composant</span><span class="sxs-lookup"><span data-stu-id="93426-103">Component object</span></span>

<span data-ttu-id="93426-104">L’objet Component représente une instance unique d’un composant qui est disponible pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="93426-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="93426-105">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="93426-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="93426-106">Cet objet est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="93426-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="93426-107">Membres</span><span class="sxs-lookup"><span data-stu-id="93426-107">Members</span></span>

<span data-ttu-id="93426-108">L’objet **Component** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93426-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="93426-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93426-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93426-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93426-110">Properties</span></span>

<span data-ttu-id="93426-111">L’objet **Component** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="93426-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="93426-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="93426-112">Property</span></span>                                                    | <span data-ttu-id="93426-113">Description</span><span class="sxs-lookup"><span data-stu-id="93426-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93426-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="93426-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="93426-115">Code du composant en question.</span><span class="sxs-lookup"><span data-stu-id="93426-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="93426-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="93426-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="93426-117">Contexte déterminé pour être applicable au composant en question.</span><span class="sxs-lookup"><span data-stu-id="93426-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="93426-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="93426-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="93426-119">SID de l’utilisateur pour le composant énuméré.</span><span class="sxs-lookup"><span data-stu-id="93426-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="93426-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93426-120">Requirements</span></span>



| <span data-ttu-id="93426-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93426-121">Requirement</span></span> | <span data-ttu-id="93426-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="93426-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93426-123">Version</span><span class="sxs-lookup"><span data-stu-id="93426-123">Version</span></span><br/> | <span data-ttu-id="93426-124">Windows Installer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="93426-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="93426-125">DLL</span><span class="sxs-lookup"><span data-stu-id="93426-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="93426-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93426-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="93426-127">IID</span><span class="sxs-lookup"><span data-stu-id="93426-127">IID</span></span><br/>     | <span data-ttu-id="93426-128">IID \_ IComponent est défini en tant que 000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="93426-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="93426-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93426-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93426-130">Utilisation de l’interface d’automatisation</span><span class="sxs-lookup"><span data-stu-id="93426-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="93426-131">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="93426-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




