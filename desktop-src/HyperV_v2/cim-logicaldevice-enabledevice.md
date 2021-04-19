---
description: La méthode EnableDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Méthode EnableDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543719"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="9beea-103">Méthode EnableDevice de la \_ classe du LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="9beea-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="9beea-104">La méthode EnableDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9beea-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="9beea-105">Demande que le LogicalDevice soit activé (« Enabled », paramètre d’entrée = TRUE) ou désactivé (= FALSe).</span><span class="sxs-lookup"><span data-stu-id="9beea-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="9beea-106">En cas de réussite, les propriétés StatusInfo/EnabledState de l’appareil doivent refléter l’état souhaité (activé/désactivé).</span><span class="sxs-lookup"><span data-stu-id="9beea-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="9beea-107">Notez que la fonction de cette méthode chevauche la propriété RequestedState.</span><span class="sxs-lookup"><span data-stu-id="9beea-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="9beea-108">RequestedState a été ajouté au modèle pour tenir à jour un enregistrement (c’est-à-dire, une valeur persistante) de la dernière demande d’État.</span><span class="sxs-lookup"><span data-stu-id="9beea-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="9beea-109">L’appel de la méthode EnableDevice doit définir la propriété RequestedState de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="9beea-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="9beea-110">Le code de retour doit être 0 si la requête a été exécutée avec succès, 1 si la demande n’est pas prise en charge et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9beea-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="9beea-111">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="9beea-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="9beea-112">Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9beea-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="9beea-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9beea-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="9beea-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9beea-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9beea-115">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9beea-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9beea-116">Si la valeur est TRUE, activez l’appareil, si la valeur FALSe, désactivez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9beea-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9beea-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9beea-117">Return value</span></span>

<span data-ttu-id="9beea-118">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="9beea-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9beea-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9beea-119">Requirements</span></span>



| <span data-ttu-id="9beea-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9beea-120">Requirement</span></span> | <span data-ttu-id="9beea-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9beea-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9beea-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9beea-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9beea-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9beea-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9beea-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9beea-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9beea-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9beea-126">Namespace</span></span><br/>                | <span data-ttu-id="9beea-127">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9beea-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9beea-128">MOF</span><span class="sxs-lookup"><span data-stu-id="9beea-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9beea-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9beea-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9beea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9beea-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9beea-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9beea-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9beea-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9beea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9beea-133">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9beea-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




