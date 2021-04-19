---
description: La propriété DefaultUIFont définit le style de police par défaut utilisé pour les contrôles. Pour spécifier la valeur par défaut, définissez DefaultUIFont sur l’un des styles prédéfinis dans la table TextStyle de la table Property.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propriété DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541558"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="e2425-104">Propriété DefaultUIFont</span><span class="sxs-lookup"><span data-stu-id="e2425-104">DefaultUIFont property</span></span>

<span data-ttu-id="e2425-105">La propriété **DefaultUIFont** définit le style de police par défaut utilisé pour les contrôles.</span><span class="sxs-lookup"><span data-stu-id="e2425-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="e2425-106">Pour spécifier la valeur par défaut, définissez **DefaultUIFont** sur l’un des styles prédéfinis dans la [table TextStyle](textstyle-table.md) de la [table Property](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="e2425-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2425-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e2425-107">Remarks</span></span>

<span data-ttu-id="e2425-108">La propriété **DefaultUIFont** de chaque package d’installation avec une interface utilisateur doit être définie dans la [table de propriétés](property-table.md) avec l’un des styles prédéfinis listés dans le [tableau TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="e2425-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="e2425-109">Si cette propriété n’est pas spécifiée, le programme d’installation utilise la police système.</span><span class="sxs-lookup"><span data-stu-id="e2425-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="e2425-110">Ainsi, le programme d’installation peut afficher de manière incorrecte les chaînes de texte lorsque la page de codes du package est différente de la page de codes de l’interface utilisateur par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2425-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="e2425-111">Le texte et le style de police d’un contrôle peuvent être définis comme décrit dans [Ajout de contrôles et de texte](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="e2425-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="e2425-112">Si la chaîne de caractères figurant dans la colonne text de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md) ne spécifie pas le style de police, le contrôle utilise la valeur de la propriété **DefaultUIFont** comme style de police.</span><span class="sxs-lookup"><span data-stu-id="e2425-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2425-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2425-113">Requirements</span></span>



| <span data-ttu-id="e2425-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2425-114">Requirement</span></span> | <span data-ttu-id="e2425-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2425-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2425-116">Version</span><span class="sxs-lookup"><span data-stu-id="e2425-116">Version</span></span><br/> | <span data-ttu-id="e2425-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2425-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2425-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2425-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2425-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2425-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e2425-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e2425-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2425-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2425-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2425-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2425-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




