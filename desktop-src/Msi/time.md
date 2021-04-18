---
description: 'La propriété Time est l’heure actuelle en heures, minutes et secondes sous la forme d’une chaîne de texte littéral au format HH : MM : SS avec une horloge de 24 heures.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propriété Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533139"
---
# <a name="time-property"></a><span data-ttu-id="28067-103">Propriété Time</span><span class="sxs-lookup"><span data-stu-id="28067-103">Time property</span></span>

<span data-ttu-id="28067-104">La propriété **Time** est l’heure actuelle en heures, minutes et secondes sous la forme d’une chaîne de texte littéral au format hh : mm : SS avec une horloge de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="28067-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="28067-105">Par exemple, l’heure 6:57 p.m.</span><span class="sxs-lookup"><span data-stu-id="28067-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="28067-106">est représenté par « 18:57:00 ».</span><span class="sxs-lookup"><span data-stu-id="28067-106">is represented by "18:57:00".</span></span> <span data-ttu-id="28067-107">Le format de la valeur dépend des paramètres régionaux de l’utilisateur, et est le format obtenu à l’aide de la fonction [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) avec l' \_ option Time FORCE24HOURFORMAT \| Time \_ NOTIMEMARKER.</span><span class="sxs-lookup"><span data-stu-id="28067-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="28067-108">La valeur de cette propriété est définie par le Windows Installer et non par l’auteur du package.</span><span class="sxs-lookup"><span data-stu-id="28067-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="28067-109">Notes</span><span class="sxs-lookup"><span data-stu-id="28067-109">Remarks</span></span>

<span data-ttu-id="28067-110">Comme il s’agit d’une chaîne de texte, elle ne peut pas être utilisée dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="28067-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="28067-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28067-111">Requirements</span></span>



| <span data-ttu-id="28067-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28067-112">Requirement</span></span> | <span data-ttu-id="28067-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="28067-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28067-114">Version</span><span class="sxs-lookup"><span data-stu-id="28067-114">Version</span></span><br/> | <span data-ttu-id="28067-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28067-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28067-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28067-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28067-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28067-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="28067-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="28067-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28067-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28067-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28067-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28067-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
