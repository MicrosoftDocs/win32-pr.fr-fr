---
description: Le programme d’installation définit la propriété RollbackDisabled lorsque la restauration a été désactivée.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propriété RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528791"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="8f2af-103">Propriété RollbackDisabled</span><span class="sxs-lookup"><span data-stu-id="8f2af-103">RollbackDisabled property</span></span>

<span data-ttu-id="8f2af-104">Le programme d’installation définit la propriété **RollbackDisabled** lorsque la restauration a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="8f2af-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="8f2af-105">**RollbackDisabled** est utilisé par les auteurs du package qui doivent s’assurer que le programme d’installation n’a pas désactivé la restauration.</span><span class="sxs-lookup"><span data-stu-id="8f2af-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="8f2af-106">La propriété **RollbackDisabled** peut être utilisée dans une expression conditionnelle qui refuse effectivement de poursuivre l’installation si la propriété **RollbackDisabled** est définie.</span><span class="sxs-lookup"><span data-stu-id="8f2af-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="8f2af-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="8f2af-107">Default Value</span></span>

<span data-ttu-id="8f2af-108">Par défaut, la restauration est activée.</span><span class="sxs-lookup"><span data-stu-id="8f2af-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2af-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8f2af-109">Remarks</span></span>

<span data-ttu-id="8f2af-110">Étant donné que la [restauration](rollback-custom-actions.md) et la [validation](commit-custom-actions.md) ne sont pas exécutées alors que la restauration est désactivée, le programme d’installation ne peut pas installer correctement un package qui utilise ces types d’actions personnalisées dans une transaction au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="8f2af-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="8f2af-111">Dans ce cas, l’auteur du package doit inclure une condition utilisant DisableRollback, qui empêche l’installation de se poursuivre si la restauration est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8f2af-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="8f2af-112">La valeur de la stratégie DisableRollback peut être définie par un administrateur dans le cadre de l’attribution de la stratégie système.</span><span class="sxs-lookup"><span data-stu-id="8f2af-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="8f2af-113">Les administrateurs sont invités à ne pas désactiver la restauration, sauf si cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8f2af-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="8f2af-114">Pour plus d’informations sur la valeur de stratégie DisableRollback, consultez [stratégie système](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8f2af-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2af-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f2af-115">Requirements</span></span>



| <span data-ttu-id="8f2af-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f2af-116">Requirement</span></span> | <span data-ttu-id="8f2af-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2af-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2af-118">Version</span><span class="sxs-lookup"><span data-stu-id="8f2af-118">Version</span></span><br/> | <span data-ttu-id="8f2af-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2af-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8f2af-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f2af-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8f2af-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f2af-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8f2af-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8f2af-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f2af-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f2af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2af-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f2af-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8f2af-125">Restauration de l’installation</span><span class="sxs-lookup"><span data-stu-id="8f2af-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="8f2af-126">Stratégie système</span><span class="sxs-lookup"><span data-stu-id="8f2af-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="8f2af-127">restaurer les actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="8f2af-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8f2af-128">valider des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="8f2af-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




