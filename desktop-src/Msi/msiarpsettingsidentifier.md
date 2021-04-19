---
description: La propriété MSIARPSETTINGSIDENTIFIER contient une liste délimitée par des points-virgules des emplacements du registre où l’application stocke les paramètres et les préférences d’un utilisateur.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propriété MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533410"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="c7b0f-103">Propriété MSIARPSETTINGSIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="c7b0f-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="c7b0f-104">La propriété **MSIARPSETTINGSIDENTIFIER** contient une liste délimitée par des points-virgules des emplacements du registre où l’application stocke les paramètres et les préférences d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="c7b0f-105">Pendant une mise à niveau du système d’exploitation, le programme d’installation peut utiliser ces informations pour améliorer l’expérience des utilisateurs qui migrent des applications.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="c7b0f-106">La valeur de la propriété **MSIARPSETTINGSIDENTIFIER** est un texte littéral qui contient la liste des emplacements du registre où l’application stocke ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="c7b0f-107">La valeur peut spécifier plusieurs emplacements de Registre possibles.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="c7b0f-108">Séparez plusieurs emplacements du Registre à l’aide de points-virgules.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="c7b0f-109">Les paramètres d’application sont généralement stockés dans les ruches de Registre **HKCU** ou **HKLM** sous la forme : *\\ \\ version* de l’application d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="c7b0f-110">L’exemple suivant est une valeur possible pour la propriété **MSIARPSETTINGSIDENTIFIER** .</span><span class="sxs-lookup"><span data-stu-id="c7b0f-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="c7b0f-111">*MyCompany \\ AppSuite \\ 1,0 ; MyCompany \\ App1 \\ 1,0 ; MyCompany \\ App2 \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="c7b0f-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="c7b0f-112">Cette propriété est facultative et peut être définie dans la table de [Propriétés](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b0f-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="c7b0f-113">Si cette propriété apparaît dans la table de propriétés, la valeur ne doit pas être définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b0f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7b0f-114">Requirements</span></span>



| <span data-ttu-id="c7b0f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7b0f-115">Requirement</span></span> | <span data-ttu-id="c7b0f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7b0f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b0f-117">Version</span><span class="sxs-lookup"><span data-stu-id="c7b0f-117">Version</span></span><br/> | <span data-ttu-id="c7b0f-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c7b0f-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c7b0f-120">Windows Installer 4,5 sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7b0f-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c7b0f-121">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b0f-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7b0f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7b0f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b0f-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7b0f-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c7b0f-124">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="c7b0f-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




