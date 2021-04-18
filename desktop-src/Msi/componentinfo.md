---
description: L’objet ComponentInfo représente des détails supplémentaires sur un composant qui peut être obtenu via un appel de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objet ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533063"
---
# <a name="componentinfo-object"></a><span data-ttu-id="5b797-103">Objet ComponentInfo</span><span class="sxs-lookup"><span data-stu-id="5b797-103">ComponentInfo object</span></span>

<span data-ttu-id="5b797-104">L’objet ComponentInfo représente des détails supplémentaires sur un composant qui peut être obtenu via un appel de MsiGetComponentPathEx.</span><span class="sxs-lookup"><span data-stu-id="5b797-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="5b797-105">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5b797-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5b797-106">Cet objet est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="5b797-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="5b797-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5b797-107">Members</span></span>

<span data-ttu-id="5b797-108">L’objet **ComponentInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b797-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="5b797-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b797-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b797-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b797-110">Properties</span></span>

<span data-ttu-id="5b797-111">L’objet **ComponentInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5b797-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="5b797-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="5b797-112">Property</span></span>                                                        | <span data-ttu-id="5b797-113">Description</span><span class="sxs-lookup"><span data-stu-id="5b797-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="5b797-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="5b797-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="5b797-115">Code du composant en question.</span><span class="sxs-lookup"><span data-stu-id="5b797-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="5b797-116">**D**</span><span class="sxs-lookup"><span data-stu-id="5b797-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="5b797-117">Chemin d’accès du composant.</span><span class="sxs-lookup"><span data-stu-id="5b797-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="5b797-118">**State**</span><span class="sxs-lookup"><span data-stu-id="5b797-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="5b797-119">État du composant.</span><span class="sxs-lookup"><span data-stu-id="5b797-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="5b797-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b797-120">Requirements</span></span>



| <span data-ttu-id="5b797-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b797-121">Requirement</span></span> | <span data-ttu-id="5b797-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b797-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b797-123">Version</span><span class="sxs-lookup"><span data-stu-id="5b797-123">Version</span></span><br/> | <span data-ttu-id="5b797-124">Windows Installer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5b797-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="5b797-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5b797-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b797-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b797-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b797-127">IID</span><span class="sxs-lookup"><span data-stu-id="5b797-127">IID</span></span><br/>     | <span data-ttu-id="5b797-128">IID \_ IComponentInfo est défini en tant que 000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5b797-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5b797-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b797-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b797-130">Utilisation de l’interface d’automatisation</span><span class="sxs-lookup"><span data-stu-id="5b797-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="5b797-131">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5b797-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




