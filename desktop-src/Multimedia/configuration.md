---
title: Configuration (Windows Multimedia)
description: Configuration
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- pilotes installables, configuration
- pilotes installables, DRV_CONFIGURE message
- Message DRV_CONFIGURE
- Message DRV_QUERYCONFIGURE
- Message DRVCONFIGINFO
- Configuration des pilotes installables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032214"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="db710-109">Configuration (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="db710-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="db710-110">Un pilote pouvant être installé peut permettre aux utilisateurs de choisir des paramètres de configuration pour le pilote et le matériel associé en affichant une boîte de dialogue de configuration lors du traitement du message de configuration du [**DRV \_**](drv-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="db710-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="db710-111">Le pilote est responsable de la création et de la gestion de la boîte de dialogue, du traitement de toute entrée d’utilisateur à partir de la boîte de dialogue et de la modification de la configuration du pilote ou du matériel comme demandé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db710-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="db710-112">Le pilote doit fournir une procédure de boîte de dialogue distincte pour traiter les messages de fenêtre pour la boîte de dialogue et un modèle de boîte de dialogue pour définir l’apparence et le contenu de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="db710-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="db710-113">Avant de recevoir le \_ message de configuration du DRV, un pilote reçoit le message [**\_ QUERYCONFIGURE du DRV**](drv-queryconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="db710-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="db710-114">Le pilote doit retourner une valeur différente de zéro à la requête pour garantir la réception du message de configuration du DRV suivant \_ .</span><span class="sxs-lookup"><span data-stu-id="db710-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="db710-115">Lors de l’initialisation de la boîte de dialogue de configuration, le pilote récupère généralement les informations de configuration à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="db710-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="db710-116">Pour faciliter la recherche de ces informations, le \_ message de configuration du DRV inclut généralement l’adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) qui contient les noms de la clé de Registre et la valeur associée au pilote.</span><span class="sxs-lookup"><span data-stu-id="db710-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="db710-117">Si l’utilisateur demande des modifications à la configuration, le pilote doit mettre à jour les informations de configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="db710-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
