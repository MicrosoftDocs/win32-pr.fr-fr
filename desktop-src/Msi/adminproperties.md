---
description: Le AdminProperties doit être créé dans la table de propriétés.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propriété AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535412"
---
# <a name="adminproperties-property"></a><span data-ttu-id="6edd2-103">Propriété AdminProperties</span><span class="sxs-lookup"><span data-stu-id="6edd2-103">AdminProperties property</span></span>

<span data-ttu-id="6edd2-104">Le **AdminProperties** doit être créé dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="6edd2-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="6edd2-105">La valeur de **AdminProperties** est une liste de noms de propriétés séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="6edd2-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="6edd2-106">Le programme d’installation enregistre les valeurs de ces propriétés listées au moment de l' [installation administrative](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="6edd2-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="6edd2-107">Lorsque les utilisateurs installent à partir de l’image administrative, l’installation utilise les valeurs enregistrées des propriétés, plutôt que les valeurs du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="6edd2-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edd2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6edd2-108">Remarks</span></span>

<span data-ttu-id="6edd2-109">Les noms de propriétés dans la liste peuvent être des lettres majuscules et minuscules (propriétés privées) ou tout en majuscules (propriétés publiques).</span><span class="sxs-lookup"><span data-stu-id="6edd2-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="6edd2-110">Cette propriété ne doit jamais se terminer par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="6edd2-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edd2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6edd2-111">Requirements</span></span>



| <span data-ttu-id="6edd2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6edd2-112">Requirement</span></span> | <span data-ttu-id="6edd2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6edd2-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edd2-114">Version</span><span class="sxs-lookup"><span data-stu-id="6edd2-114">Version</span></span><br/> | <span data-ttu-id="6edd2-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6edd2-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6edd2-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6edd2-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6edd2-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6edd2-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6edd2-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6edd2-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6edd2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6edd2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edd2-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6edd2-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




