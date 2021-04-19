---
description: La propriété Résumé de l’heure et de la date de dernière sauvegarde indique la dernière heure à laquelle le package d’installation, la transformation ou le package de correctifs a été modified.Initially, un auteur doit définir la valeur de la propriété Résumé de l’heure/date du dernier enregistrement sur null pour indiquer qu’aucune modification n’a encore été apportée au package. Un auteur doit ensuite mettre à jour la propriété de résumé heure/date du dernier enregistrement à la date/heure système à chaque enregistrement d’une base de données d’installation, d’une transformation ou d’un package de correctifs modifiés.
ms.assetid: be3957fa-463a-4eb2-8b9d-93a16e95a8cf
title: Propriété date/heure du dernier enregistrement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe2300640434a52a78575221dc69e0f7263883
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535003"
---
# <a name="last-saved-timedate-summary-property"></a><span data-ttu-id="471b1-104">Propriété date/heure du dernier enregistrement</span><span class="sxs-lookup"><span data-stu-id="471b1-104">Last Saved Time/Date Summary property</span></span>

<span data-ttu-id="471b1-105">La propriété Résumé de l' **heure et de la date du dernier enregistrement** indique l’heure de la dernière modification du package d’installation, de la transformation ou du package correctif.</span><span class="sxs-lookup"><span data-stu-id="471b1-105">The **Last Saved Time/Date Summary** property conveys the last time when this installation package, transform, or patch package was modified.</span></span>

<span data-ttu-id="471b1-106">Au départ, un auteur doit définir la valeur de la propriété Résumé de l' **heure et de la date du dernier enregistrement** sur null pour indiquer qu’aucune modification n’a encore été apportée au package.</span><span class="sxs-lookup"><span data-stu-id="471b1-106">Initially, an author should set the value of the **Last Saved Time/Date Summary** property to Null to indicate that no changes have yet been made to the package.</span></span> <span data-ttu-id="471b1-107">Un auteur doit ensuite mettre à jour la propriété de **Résumé heure/date du dernier enregistrement** à la date/heure système à chaque enregistrement d’une base de données d’installation, d’une transformation ou d’un package de correctifs modifiés.</span><span class="sxs-lookup"><span data-stu-id="471b1-107">An author should then update the **Last Saved Time/Date Summary** property to the current system time/date each time a modified installation database, transform, or patch package is saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="471b1-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="471b1-108">Requirements</span></span>



| <span data-ttu-id="471b1-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="471b1-109">Requirement</span></span> | <span data-ttu-id="471b1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="471b1-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471b1-111">Version</span><span class="sxs-lookup"><span data-stu-id="471b1-111">Version</span></span><br/> | <span data-ttu-id="471b1-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="471b1-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="471b1-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="471b1-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="471b1-114">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="471b1-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471b1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="471b1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471b1-116">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="471b1-116">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




