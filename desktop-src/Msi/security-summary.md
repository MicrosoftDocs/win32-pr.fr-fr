---
description: La propriété Résumé de sécurité indique si le package doit être ouvert en lecture seule.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propriété Résumé de sécurité
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542716"
---
# <a name="security-summary-property"></a><span data-ttu-id="02aa9-103">Propriété Résumé de sécurité</span><span class="sxs-lookup"><span data-stu-id="02aa9-103">Security Summary property</span></span>

<span data-ttu-id="02aa9-104">La propriété **Résumé de sécurité** indique si le package doit être ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="02aa9-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="02aa9-105">L’outil d’édition de base de données ne doit pas modifier une base de données en lecture seule appliquée et doit émettre un avertissement lors des tentatives de modification d’une base de données en lecture seule recommandée.</span><span class="sxs-lookup"><span data-stu-id="02aa9-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="02aa9-106">Les valeurs suivantes de cette propriété s’appliquent aux fichiers Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="02aa9-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="02aa9-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="02aa9-107">Value</span></span> | <span data-ttu-id="02aa9-108">Description</span><span class="sxs-lookup"><span data-stu-id="02aa9-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="02aa9-109">0</span><span class="sxs-lookup"><span data-stu-id="02aa9-109">0</span></span>     | <span data-ttu-id="02aa9-110">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="02aa9-110">No restriction</span></span>        |
| <span data-ttu-id="02aa9-111">2</span><span class="sxs-lookup"><span data-stu-id="02aa9-111">2</span></span>     | <span data-ttu-id="02aa9-112">Lecture seule recommandée</span><span class="sxs-lookup"><span data-stu-id="02aa9-112">Read-only recommended</span></span> |
| <span data-ttu-id="02aa9-113">4</span><span class="sxs-lookup"><span data-stu-id="02aa9-113">4</span></span>     | <span data-ttu-id="02aa9-114">En lecture seule forcé</span><span class="sxs-lookup"><span data-stu-id="02aa9-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="02aa9-115">Cette propriété doit être définie sur lecture seule recommandée (2) pour une base de données d’installation et pour application en lecture seule (4) pour une transformation ou un correctif.</span><span class="sxs-lookup"><span data-stu-id="02aa9-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="02aa9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02aa9-116">Requirements</span></span>



| <span data-ttu-id="02aa9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02aa9-117">Requirement</span></span> | <span data-ttu-id="02aa9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="02aa9-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02aa9-119">Version</span><span class="sxs-lookup"><span data-stu-id="02aa9-119">Version</span></span><br/> | <span data-ttu-id="02aa9-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02aa9-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02aa9-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02aa9-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02aa9-122">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="02aa9-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02aa9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02aa9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02aa9-124">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="02aa9-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




