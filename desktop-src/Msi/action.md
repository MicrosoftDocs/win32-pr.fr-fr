---
description: La propriété ACTION peut être définie sur les valeurs suivantes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535282"
---
# <a name="action-property"></a><span data-ttu-id="59fa0-103">ACTION, propriété</span><span class="sxs-lookup"><span data-stu-id="59fa0-103">ACTION property</span></span>

<span data-ttu-id="59fa0-104">La propriété **action** peut être définie sur les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="59fa0-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="59fa0-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fa0-105">Value</span></span>



| <span data-ttu-id="59fa0-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fa0-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="59fa0-107">Signification</span><span class="sxs-lookup"><span data-stu-id="59fa0-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="59fa0-108"><dt>**INSTALLER**</dt></span><span class="sxs-lookup"><span data-stu-id="59fa0-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="59fa0-109">Action d’installation</span><span class="sxs-lookup"><span data-stu-id="59fa0-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="59fa0-110"><dt>**PUBLIÉS**</dt></span><span class="sxs-lookup"><span data-stu-id="59fa0-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="59fa0-111">Action de publication</span><span class="sxs-lookup"><span data-stu-id="59fa0-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="59fa0-112"><dt>**ADMINISTRATEUR**</dt></span><span class="sxs-lookup"><span data-stu-id="59fa0-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="59fa0-113">Action d’administration</span><span class="sxs-lookup"><span data-stu-id="59fa0-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="59fa0-114">La propriété **action** détermine l’action à effectuer si un nom d’action null est fourni à [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou à la [**méthode d’action**](session-doaction.md).</span><span class="sxs-lookup"><span data-stu-id="59fa0-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="59fa0-115">Si aucune valeur n’est définie pour la propriété **action** , le programme d’installation appelle l' [action d’installation](install-action.md).</span><span class="sxs-lookup"><span data-stu-id="59fa0-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59fa0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59fa0-116">Requirements</span></span>



| <span data-ttu-id="59fa0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59fa0-117">Requirement</span></span> | <span data-ttu-id="59fa0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fa0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59fa0-119">Version</span><span class="sxs-lookup"><span data-stu-id="59fa0-119">Version</span></span><br/> | <span data-ttu-id="59fa0-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59fa0-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="59fa0-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59fa0-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="59fa0-122">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59fa0-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="59fa0-123">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="59fa0-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59fa0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59fa0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fa0-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59fa0-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




