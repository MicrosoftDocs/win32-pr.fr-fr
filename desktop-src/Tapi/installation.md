---
description: Les principales sources des procédures d’installation sont le kit de ressources pour le système d’exploitation cible, la documentation de l’application et les instructions du fournisseur de services. Pour les fournisseurs de services Microsoft, le kit de ressources approprié contient des instructions.
ms.assetid: a94023ac-5226-4a51-a08b-c53d08260710
title: Installation (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446510c3d92431188bcff50842b15c200cc5d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544775"
---
# <a name="installation-telephony-api"></a><span data-ttu-id="b51b7-104">Installation (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="b51b7-104">Installation (Telephony API)</span></span>

<span data-ttu-id="b51b7-105">Les principales sources des procédures d’installation sont le kit de ressources pour le système d’exploitation cible, la documentation de l’application et les instructions du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b51b7-105">The primary sources for installation procedures are the Resource Kit for the target operating system, application documentation, and service provider instructions.</span></span> <span data-ttu-id="b51b7-106">Pour les fournisseurs de services Microsoft, le kit de ressources approprié contient des instructions.</span><span class="sxs-lookup"><span data-stu-id="b51b7-106">For Microsoft service providers, the appropriate resource kit contains instructions.</span></span>

<span data-ttu-id="b51b7-107">Le processus d’installation doit inclure la liste des « services de téléphonie » en tant que dépendance.</span><span class="sxs-lookup"><span data-stu-id="b51b7-107">The installation process must include listing "Telephony Service" as dependency.</span></span>

<span data-ttu-id="b51b7-108">Si une application ou un fournisseur de services utilise le registre pour le stockage de données privées persistantes, les informations ne doivent pas être placées dans la section TAPI du Registre.</span><span class="sxs-lookup"><span data-stu-id="b51b7-108">If an application or service provider uses the registry for storage of persistent private data, the information must not be placed in TAPI's section of the registry.</span></span> <span data-ttu-id="b51b7-109">Il n’est pas garanti que le format de cette section soit conservé dans les futures versions.</span><span class="sxs-lookup"><span data-stu-id="b51b7-109">The format of this section is not guaranteed to be maintained in future versions.</span></span>

 

 



