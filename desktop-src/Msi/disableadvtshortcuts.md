---
description: La définition de la propriété DISABLEADVTSHORTCUTS désactive la génération de raccourcis prenant en charge l’installation à la demande et la publication. La définition de cette propriété spécifie que ces raccourcis doivent plutôt être remplacés par des raccourcis standard.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propriété DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523462"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="38db4-104">Propriété DISABLEADVTSHORTCUTS</span><span class="sxs-lookup"><span data-stu-id="38db4-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="38db4-105">La définition de la propriété **DISABLEADVTSHORTCUTS** désactive la génération de raccourcis prenant en charge l' [installation à la demande](installation-on-demand.md) et la [publication](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="38db4-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="38db4-106">La définition de cette propriété spécifie que ces raccourcis doivent plutôt être remplacés par des raccourcis standard.</span><span class="sxs-lookup"><span data-stu-id="38db4-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="38db4-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="38db4-107">Default Value</span></span>

<span data-ttu-id="38db4-108">Par défaut, la génération de raccourcis d’installation à la demande est activée.</span><span class="sxs-lookup"><span data-stu-id="38db4-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="38db4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="38db4-109">Remarks</span></span>

<span data-ttu-id="38db4-110">Les raccourcis qui prennent en charge la publication ont le nom d’une fonctionnalité, plutôt qu’un chemin de fichier mis en forme au format \[ \# filekey \] , entré dans la colonne cible de la [table de raccourcis](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="38db4-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="38db4-111">Si cette propriété est définie et que la fonctionnalité est installée, le programme d’installation génère un raccourci standard vers la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="38db4-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="38db4-112">Cette propriété est couramment utilisée par les administrateurs pour les utilisateurs qui se déplacent entre des environnements qui ne prennent pas en charge la publicité.</span><span class="sxs-lookup"><span data-stu-id="38db4-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="38db4-113">Cette propriété peut être définie par une transformation, dans le flux d’administration, ou dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="38db4-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="38db4-114">S’il est défini à l’aide de la ligne de commande ou d’un appel à [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), il doit être réinitialisé à nouveau lors de chaque installation suivante.</span><span class="sxs-lookup"><span data-stu-id="38db4-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="38db4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38db4-115">Requirements</span></span>



| <span data-ttu-id="38db4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38db4-116">Requirement</span></span> | <span data-ttu-id="38db4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="38db4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38db4-118">Version</span><span class="sxs-lookup"><span data-stu-id="38db4-118">Version</span></span><br/> | <span data-ttu-id="38db4-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38db4-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38db4-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="38db4-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38db4-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="38db4-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="38db4-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="38db4-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38db4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38db4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38db4-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38db4-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




