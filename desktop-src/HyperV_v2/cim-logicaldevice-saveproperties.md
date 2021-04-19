---
description: Demande que l’appareil capture ses informations de configuration, d’installation et/ou d’état actuelles dans un magasin de stockage.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Méthode SaveProperties de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536615"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="9015d-103">Méthode SaveProperties de la \_ classe du LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="9015d-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="9015d-104">Demande que l’appareil capture ses informations de configuration, d’installation et/ou d’état actuelles dans un magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="9015d-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="9015d-105">L’objectif est d’utiliser ces informations ultérieurement (via la méthode RestoreProperties) pour ramener un appareil à son « état » actuel.</span><span class="sxs-lookup"><span data-stu-id="9015d-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="9015d-106">Cette méthode peut ne pas être prise en charge par tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="9015d-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="9015d-107">La méthode doit retourner 0 en cas de réussite, 1 si la demande n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9015d-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="9015d-108">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="9015d-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="9015d-109">Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9015d-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="9015d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9015d-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="9015d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9015d-111">Parameters</span></span>

<span data-ttu-id="9015d-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9015d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9015d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9015d-113">Return value</span></span>

<span data-ttu-id="9015d-114">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="9015d-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9015d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9015d-115">Requirements</span></span>



| <span data-ttu-id="9015d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9015d-116">Requirement</span></span> | <span data-ttu-id="9015d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9015d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9015d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9015d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9015d-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9015d-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9015d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9015d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9015d-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9015d-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9015d-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9015d-122">Namespace</span></span><br/>                | <span data-ttu-id="9015d-123">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9015d-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9015d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9015d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9015d-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9015d-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9015d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9015d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9015d-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9015d-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9015d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9015d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9015d-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9015d-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




