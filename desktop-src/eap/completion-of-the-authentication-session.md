---
title: Fin de la session d’authentification
description: Une fois la session d’authentification terminée, le service d’authentification appelle la fonction RasEapEnd pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381846"
---
# <a name="completion-of-the-authentication-session"></a><span data-ttu-id="3d420-103">Fin de la session d’authentification</span><span class="sxs-lookup"><span data-stu-id="3d420-103">Completion of the Authentication Session</span></span>

<span data-ttu-id="3d420-104">Une fois la session d’authentification terminée, le service d’authentification appelle la fonction [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail.</span><span class="sxs-lookup"><span data-stu-id="3d420-104">After the authentication session is completed, the authentication service calls the [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) function to allow the authentication protocol to deallocate its work buffer.</span></span> <span data-ttu-id="3d420-105">Cette action est effectuée que l’authentification ait abouti ou non.</span><span class="sxs-lookup"><span data-stu-id="3d420-105">This action is taken regardless of whether authentication was successful.</span></span> <span data-ttu-id="3d420-106">L’appel de la fonction **RasEapEnd** garantit qu’aucun autre appel au protocole d’authentification n’est effectué à l’aide de cet utilisateur ou contexte sans appeler d’abord [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d420-106">Calling the **RasEapEnd** function guarantees that no further calls are made to the authentication protocol using that particular user or context without first calling [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).</span></span>

 

 