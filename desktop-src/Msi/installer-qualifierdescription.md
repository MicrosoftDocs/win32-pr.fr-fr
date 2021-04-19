---
description: La propriété QualifierDescription en lecture seule retourne une chaîne de texte décrivant le composant qualifié.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer. QualifierDescription, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530351"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="c2dfc-103">Installer. QualifierDescription, propriété</span><span class="sxs-lookup"><span data-stu-id="c2dfc-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="c2dfc-104">La propriété **QualifierDescription** en lecture seule retourne une chaîne de texte décrivant le composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="c2dfc-105">Cette chaîne localisable est créée dans la colonne AppData de la [table PublishComponent](publishcomponent-table.md) et peut être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="c2dfc-106">Le qualificateur fait la distinction entre plusieurs formes du même composant, par exemple un composant implémenté dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="c2dfc-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2dfc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2dfc-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="c2dfc-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c2dfc-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c2dfc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2dfc-110">Requirements</span></span>



| <span data-ttu-id="c2dfc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2dfc-111">Requirement</span></span> | <span data-ttu-id="c2dfc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2dfc-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dfc-113">Version</span><span class="sxs-lookup"><span data-stu-id="c2dfc-113">Version</span></span><br/> | <span data-ttu-id="c2dfc-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c2dfc-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c2dfc-116">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2dfc-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c2dfc-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c2dfc-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="c2dfc-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2dfc-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c2dfc-119">IID</span><span class="sxs-lookup"><span data-stu-id="c2dfc-119">IID</span></span><br/>     | <span data-ttu-id="c2dfc-120">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c2dfc-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c2dfc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2dfc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dfc-122">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="c2dfc-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="c2dfc-123">Composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="c2dfc-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




