---
description: La propriété date est le mois, le jour et l’année en cours sous la forme d’une chaîne de texte littéral au format MM/jj/aaaa.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541640"
---
# <a name="date-property"></a><span data-ttu-id="d78c1-103">Date, propriété</span><span class="sxs-lookup"><span data-stu-id="d78c1-103">Date property</span></span>

<span data-ttu-id="d78c1-104">La propriété **Date** est le mois, le jour et l’année en cours sous la forme d’une chaîne de texte littéral au format mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="d78c1-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="d78c1-105">Par exemple, la date du 22 juin 2005 peut être représentée sous la forme « 06/22/2005 ».</span><span class="sxs-lookup"><span data-stu-id="d78c1-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="d78c1-106">Le format de la valeur dépend des paramètres régionaux de l’utilisateur, et est le format obtenu à l’aide de [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) avec l' \_ option Date SHORTDATE.</span><span class="sxs-lookup"><span data-stu-id="d78c1-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="d78c1-107">La valeur de cette propriété est définie par le Windows Installer et non par l’auteur du package.</span><span class="sxs-lookup"><span data-stu-id="d78c1-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78c1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d78c1-108">Remarks</span></span>

<span data-ttu-id="d78c1-109">Comme il s’agit d’une chaîne de texte, elle ne peut pas être utilisée dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="d78c1-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d78c1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d78c1-110">Requirements</span></span>



| <span data-ttu-id="d78c1-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d78c1-111">Requirement</span></span> | <span data-ttu-id="d78c1-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d78c1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d78c1-113">Version</span><span class="sxs-lookup"><span data-stu-id="d78c1-113">Version</span></span><br/> | <span data-ttu-id="d78c1-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d78c1-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d78c1-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d78c1-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d78c1-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d78c1-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d78c1-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c1-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d78c1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d78c1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d78c1-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d78c1-119">Properties</span></span>](properties.md)
</dt> </dl>

 

