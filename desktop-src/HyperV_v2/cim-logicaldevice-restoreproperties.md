---
description: Demande que l’appareil rétablit la configuration, l’installation et/ou les informations d’État à partir d’un magasin de stockage.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Méthode RestoreProperties de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536600"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="dd42d-103">Méthode RestoreProperties de la \_ classe du LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="dd42d-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="dd42d-104">Demande que l’appareil rétablit la configuration, l’installation et/ou les informations d’État à partir d’un magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="dd42d-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="dd42d-105">L’objectif est de capturer ces informations à un moment antérieur (via la méthode SaveProperties) et de les utiliser pour retourner un appareil à cette « condition » antérieure.</span><span class="sxs-lookup"><span data-stu-id="dd42d-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="dd42d-106">Cette méthode peut ne pas être prise en charge par tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="dd42d-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="dd42d-107">La méthode doit retourner 0 en cas de réussite, 1 si la demande n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="dd42d-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="dd42d-108">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="dd42d-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="dd42d-109">Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="dd42d-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd42d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd42d-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="dd42d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd42d-111">Parameters</span></span>

<span data-ttu-id="dd42d-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd42d-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd42d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd42d-113">Requirements</span></span>



| <span data-ttu-id="dd42d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd42d-114">Requirement</span></span> | <span data-ttu-id="dd42d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd42d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd42d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd42d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd42d-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd42d-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd42d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd42d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd42d-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd42d-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd42d-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dd42d-120">Namespace</span></span><br/>                | <span data-ttu-id="dd42d-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd42d-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd42d-122">MOF</span><span class="sxs-lookup"><span data-stu-id="dd42d-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd42d-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd42d-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd42d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dd42d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd42d-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd42d-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd42d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd42d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd42d-127">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dd42d-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




