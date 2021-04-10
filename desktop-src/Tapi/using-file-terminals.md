---
description: Les terminaux de fichiers peuvent être utilisés de deux manières.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Utilisation des terminaux de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115810"
---
# <a name="using-file-terminals"></a><span data-ttu-id="279ed-103">Utilisation des terminaux de fichiers</span><span class="sxs-lookup"><span data-stu-id="279ed-103">Using File Terminals</span></span>

<span data-ttu-id="279ed-104">Les terminaux de fichiers peuvent être utilisés de deux manières.</span><span class="sxs-lookup"><span data-stu-id="279ed-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="279ed-105">La méthode la plus simple consiste à utiliser [**ITBasicCallControl2 :: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) pour sélectionner un terminal de fichiers (lecture ou enregistrement) sur un objet d’appel TAPI.</span><span class="sxs-lookup"><span data-stu-id="279ed-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="279ed-106">Dans ce cas, l’interface TAPI prend en charge la connexion des flux audio aux terminaux de suivi.</span><span class="sxs-lookup"><span data-stu-id="279ed-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="279ed-107">La deuxième méthode permet à une application d’avoir un contrôle plus fin sur le mappage des flux audio à des pistes.</span><span class="sxs-lookup"><span data-stu-id="279ed-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="279ed-108">Dans ce scénario, l’application énumère les flux disponibles sur l’appel, sélectionne ceux qu’elle souhaite enregistrer (ou utiliser pour la lecture), crée (ou recherche) les pistes correspondantes sur le terminal de fichiers et sélectionne les pistes sur les flux d’appels.</span><span class="sxs-lookup"><span data-stu-id="279ed-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="279ed-109">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="279ed-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="279ed-110">Lecture simple</span><span class="sxs-lookup"><span data-stu-id="279ed-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="279ed-111">Lecture contrôlée par le suivi</span><span class="sxs-lookup"><span data-stu-id="279ed-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="279ed-112">Enregistrement simple</span><span class="sxs-lookup"><span data-stu-id="279ed-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="279ed-113">Enregistrement contrôlé par suivi</span><span class="sxs-lookup"><span data-stu-id="279ed-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



