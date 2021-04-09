---
description: Le protocole PGM utilise des options de socket pour définir l’État, fournir des paramètres de multidiffusion et, sinon, implémenter ses fonctionnalités de multidiffusion.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Options de socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862545"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="96df8-103">Options de socket PGM</span><span class="sxs-lookup"><span data-stu-id="96df8-103">PGM Socket Options</span></span>

<span data-ttu-id="96df8-104">Le protocole PGM utilise des options de socket pour définir l’État, fournir des paramètres de multidiffusion et, sinon, implémenter ses fonctionnalités de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="96df8-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="96df8-105">Cette page spécifie la manière dont les options de socket PGM doivent être définies, énumère les options de Socket disponibles pour le protocole PGM et, le cas échéant, fournit des exemples d’utilisation et des informations supplémentaires pour diverses options.</span><span class="sxs-lookup"><span data-stu-id="96df8-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="96df8-106">Pour obtenir les définitions de base de chaque option de socket PCM, consultez [options de socket](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="96df8-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="96df8-107">**Windows XP :** La programmation de la multidiffusion (PGM) fiable n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="96df8-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="96df8-108">Les options de socket suivantes sont disponibles pour les expéditeurs PGM :</span><span class="sxs-lookup"><span data-stu-id="96df8-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="96df8-109">\_LATEJOIN RM</span><span class="sxs-lookup"><span data-stu-id="96df8-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="96df8-110">taille de la \_ fenêtre de tarif RM \_ \_</span><span class="sxs-lookup"><span data-stu-id="96df8-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="96df8-111">taux d’avancée de la \_ fenêtre d’envoi RM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="96df8-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="96df8-112">\_statistiques des expéditeurs RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="96df8-113">\_ \_ \_ méthode avancée de la fenêtre d’expéditeur RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="96df8-114">RM \_ Set \_ MCAST \_ TTL</span><span class="sxs-lookup"><span data-stu-id="96df8-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="96df8-115">configuration de la \_ \_ limite du message RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="96df8-116">RM- \_ définir \_ Envoyer \_ si</span><span class="sxs-lookup"><span data-stu-id="96df8-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="96df8-117">RM \_ utiliser \_ FEC</span><span class="sxs-lookup"><span data-stu-id="96df8-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="96df8-118">L’option de méthode Advance de la fenêtre de l' \_ expéditeur RM \_ \_ \_ spécifie la méthode utilisée lors de l’avancement de la fenêtre d’envoi du bord de fin.</span><span class="sxs-lookup"><span data-stu-id="96df8-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="96df8-119">Le paramètre optval peut uniquement être une \_ fenêtre \_ Advance \_ par \_ heure (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="96df8-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="96df8-120">Notez que l' \_ \_ utilisation \_ du cache de données par la fenêtre E \_ \_ n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="96df8-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="96df8-121">Les options de socket suivantes sont disponibles pour les récepteurs PGM :</span><span class="sxs-lookup"><span data-stu-id="96df8-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="96df8-122">RM- \_ Ajouter une \_ réception \_ si</span><span class="sxs-lookup"><span data-stu-id="96df8-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="96df8-123">\_réception RM \_ del \_ si</span><span class="sxs-lookup"><span data-stu-id="96df8-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="96df8-124">\_ \_ abonnement intranet à vitesse élevée \_ RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="96df8-125">\_statistiques du récepteur RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="96df8-126">Définition des options de socket PGM</span><span class="sxs-lookup"><span data-stu-id="96df8-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="96df8-127">L’extrait de code suivant illustre une règle de programmation pour définir les options de socket PGM :</span><span class="sxs-lookup"><span data-stu-id="96df8-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="96df8-128">Dans l’extrait de code ci-dessus, le type et le contenu de l’objet de contenu sont dépendants de l' *option de socket* définie.</span><span class="sxs-lookup"><span data-stu-id="96df8-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="96df8-129">Pour toutes les options de socket PGM, le niveau de socket est IPPROTO \_ RM.</span><span class="sxs-lookup"><span data-stu-id="96df8-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="96df8-130">Les options de socket PGM doivent être définies immédiatement après l’appel à la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , avec les exceptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="96df8-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="96df8-131">configuration de la \_ \_ limite du message RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="96df8-132">\_statistiques des expéditeurs RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="96df8-133">\_statistiques du récepteur RM \_</span><span class="sxs-lookup"><span data-stu-id="96df8-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



