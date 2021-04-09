---
title: Création de disques avec plusieurs sessions
description: IMAPi est en charge de la création de disques de données à plusieurs sessions. Il existe quelques considérations à prendre en compte lors de la création d’un disque à sessions multiples.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196614"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="f1dec-104">Création de disques avec plusieurs sessions</span><span class="sxs-lookup"><span data-stu-id="f1dec-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="f1dec-105">IMAPi est en charge de la création de disques de données à plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="f1dec-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="f1dec-106">Il existe quelques considérations à prendre en compte lors de la création d’un disque à sessions multiples.</span><span class="sxs-lookup"><span data-stu-id="f1dec-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="f1dec-107">La méthode [**IDiscMaster :: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) détermine s’il existe un disque multi-session IMAPI dans le lecteur actif sur le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f1dec-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="f1dec-108">Si c’est le cas, IMAPi passe automatiquement en mode de session multiple.</span><span class="sxs-lookup"><span data-stu-id="f1dec-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="f1dec-109">L’utilisation de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) après l’établissement du mode de session multiple entraîne le retour de IMAPI en mode session unique.</span><span class="sxs-lookup"><span data-stu-id="f1dec-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="f1dec-110">Cela signifie qu’un disque vierge est requis pour une gravure [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) .</span><span class="sxs-lookup"><span data-stu-id="f1dec-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="f1dec-111">Si le disque est en mode multi-session, le même disque doit se trouver dans l’enregistreur actif ou un code d’erreur IMAPi \_ E \_ WRONGDISC est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="f1dec-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="f1dec-112">Si vous sélectionnez un enregistreur au format Joliet, IMAPi lit les informations du disque actuellement installé. Si le disque est un disque IMAPi Joliet antérieur qui a de l’espace pour une autre session, IMAPi se définit automatiquement en mode multi-session.</span><span class="sxs-lookup"><span data-stu-id="f1dec-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="f1dec-113">Ce disque doit être présent dans l’enregistreur actif lors de l’appel de [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span><span class="sxs-lookup"><span data-stu-id="f1dec-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="f1dec-114">La fermeture de la première session sur un disque nécessite 21 Mo.</span><span class="sxs-lookup"><span data-stu-id="f1dec-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="f1dec-115">Chaque session supplémentaire nécessite 11 Mo pour se fermer.</span><span class="sxs-lookup"><span data-stu-id="f1dec-115">Each additional session requires 11 MB to close.</span></span>

 

 




