---
description: Le programme d’installation définit la propriété UILevel sur le niveau de l’interface utilisateur.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propriété UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539659"
---
# <a name="uilevel-property"></a><span data-ttu-id="3cf4f-103">Propriété UILevel</span><span class="sxs-lookup"><span data-stu-id="3cf4f-103">UILevel property</span></span>

<span data-ttu-id="3cf4f-104">Le programme d’installation définit la propriété **UILevel** sur le niveau de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="3cf4f-105">L’interface utilisateur interne est activée et définie par [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="3cf4f-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="3cf4f-106">Cette propriété est définie sur l’un des types de données INSTALLUILEVEL suivants.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="3cf4f-107">INSTALLUILEVEL</span><span class="sxs-lookup"><span data-stu-id="3cf4f-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="3cf4f-108">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="3cf4f-108">Numeric value</span></span> | <span data-ttu-id="3cf4f-109">Niveau de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3cf4f-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="3cf4f-110">INSTALLUILEVEL \_ aucun</span><span class="sxs-lookup"><span data-stu-id="3cf4f-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="3cf4f-111">2</span><span class="sxs-lookup"><span data-stu-id="3cf4f-111">2</span></span>             | <span data-ttu-id="3cf4f-112">Installation entièrement sans assistance :</span><span class="sxs-lookup"><span data-stu-id="3cf4f-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="3cf4f-113">INSTALLUILEVEL de \_ base</span><span class="sxs-lookup"><span data-stu-id="3cf4f-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="3cf4f-114">3</span><span class="sxs-lookup"><span data-stu-id="3cf4f-114">3</span></span>             | <span data-ttu-id="3cf4f-115">Progression et gestion des erreurs simples.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="3cf4f-116">INSTALLUILEVEL \_ réduit</span><span class="sxs-lookup"><span data-stu-id="3cf4f-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="3cf4f-117">4</span><span class="sxs-lookup"><span data-stu-id="3cf4f-117">4</span></span>             | <span data-ttu-id="3cf4f-118">Interface utilisateur créée, boîtes de dialogue d’Assistant supprimées.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="3cf4f-119">INSTALLUILEVEL \_ Full</span><span class="sxs-lookup"><span data-stu-id="3cf4f-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="3cf4f-120">5</span><span class="sxs-lookup"><span data-stu-id="3cf4f-120">5</span></span>             | <span data-ttu-id="3cf4f-121">Interface utilisateur créée avec les assistants, la progression, les erreurs.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3cf4f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cf4f-122">Requirements</span></span>



| <span data-ttu-id="3cf4f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cf4f-123">Requirement</span></span> | <span data-ttu-id="3cf4f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cf4f-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf4f-125">Version</span><span class="sxs-lookup"><span data-stu-id="3cf4f-125">Version</span></span><br/> | <span data-ttu-id="3cf4f-126">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3cf4f-127">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3cf4f-128">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3cf4f-129">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf4f-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cf4f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cf4f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf4f-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3cf4f-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="3cf4f-132">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3cf4f-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="3cf4f-133">Détermination du niveau d’interface utilisateur à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="3cf4f-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




