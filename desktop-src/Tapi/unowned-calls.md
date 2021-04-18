---
description: Pour empêcher les appels sans propriétaire d’être dans le système de téléphonie, TAPI supprime les appels qui ont été signalés auprès d’un fournisseur de services s’il ne peut pas identifier une application comme étant le propriétaire initial de l’appel.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Appels sans propriétaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519330"
---
# <a name="unowned-calls"></a><span data-ttu-id="a88f2-103">Appels sans propriétaire</span><span class="sxs-lookup"><span data-stu-id="a88f2-103">Unowned Calls</span></span>

<span data-ttu-id="a88f2-104">Pour empêcher les appels sans propriétaire d’être dans le système de téléphonie, TAPI supprime les appels qui ont été signalés auprès d’un fournisseur de services s’il ne peut pas identifier une application comme étant le propriétaire initial de l’appel.</span><span class="sxs-lookup"><span data-stu-id="a88f2-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="a88f2-105">Dans TAPI version 2,0 et versions ultérieures, TAPI appelle la fonction [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) pour supprimer l’appel.</span><span class="sxs-lookup"><span data-stu-id="a88f2-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="a88f2-106">Le fournisseur de services peut savoir à l’avance si une application est disponible pour prendre possession d’un nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="a88f2-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="a88f2-107">L’interface TAPI informe toujours le fournisseur de services des types de média pour lesquels une application est disponible à l’aide de la fonction [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .</span><span class="sxs-lookup"><span data-stu-id="a88f2-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="a88f2-108">Par exemple, si un fournisseur de services détermine qu’il y a un appel actif sur la ligne qui a le \_ mode INTERACTIVEVOICE LINEMEDIAMODE, il doit vérifier la détection de support par défaut avant de générer les messages de ligne [**\_ NEWCALL**](line-newcall.md) et de [**ligne \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a88f2-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="a88f2-109">Si la détection de support par défaut indique qu’aucune application n’est en train de rechercher un \_ appel LINEMEDIAMODE INTERACTIVEVOICE, le fournisseur de services ne doit pas envoyer les messages, car l’interface TAPI la supprimera immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a88f2-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
