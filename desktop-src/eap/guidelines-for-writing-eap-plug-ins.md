---
title: Instructions pour l’écriture de dll EAP
description: Les plug-ins ou dll EAP peuvent être écrits pour optimiser leurs performances dans différents scénarios.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106513699"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="20bb6-103">Instructions pour l’écriture de dll EAP</span><span class="sxs-lookup"><span data-stu-id="20bb6-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="20bb6-104">Les plug-ins ou dll EAP peuvent être écrits pour optimiser leurs performances dans différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="20bb6-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="20bb6-105">Instructions générales</span><span class="sxs-lookup"><span data-stu-id="20bb6-105">General Guidelines</span></span>

-   <span data-ttu-id="20bb6-106">Pour créer une connexion chiffrée, les plug-ins EAP doivent générer des clés de chiffrement et les retourner via les attributs RADIUS spécifiques aux fournisseurs Microsoft MS-MPPE-Send-Keys et MS-MPPE-recv-keys.</span><span class="sxs-lookup"><span data-stu-id="20bb6-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="20bb6-107">Pour plus d’informations, consultez la section Notes dans [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .</span><span class="sxs-lookup"><span data-stu-id="20bb6-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="20bb6-108">Directives sans fil</span><span class="sxs-lookup"><span data-stu-id="20bb6-108">Wireless Guidelines</span></span>

<span data-ttu-id="20bb6-109">Vous trouverez ci-dessous des instructions et des recommandations pour l’écriture d’un plug-in EAP qui prend en charge l’authentification des ordinateurs dans des scénarios sans fil (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="20bb6-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="20bb6-110">Cette section ne s’applique pas aux scénarios VPN et d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="20bb6-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="20bb6-111">Afin de ne pas bloquer l’exécution des systèmes sans assistance, les plug-ins EAP ne doivent pas effectuer d’appels d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="20bb6-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="20bb6-112">L’implémentation du plug-in EAP de l’étape d’authentification de l’ordinateur doit être effectuée aussi rapidement que possible, de sorte qu’elle n’entrave pas le démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="20bb6-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="20bb6-113">Si votre protocole EAP ne prend pas en charge l’authentification de l’ordinateur, il doit vérifier l’indicateur d’authentification de l’ordinateur, l’authentification de l’ordinateur de l' **\_ \_ indicateur EAP \_ \_ RAS** utilisé dans le champ **fFlags** de l' [**\_ \_ entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)et retourner une erreur.</span><span class="sxs-lookup"><span data-stu-id="20bb6-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




