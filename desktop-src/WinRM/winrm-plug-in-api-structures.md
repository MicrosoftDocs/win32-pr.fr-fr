---
title: Structures d’API de plug-in WinRM
description: Structures d’API de plug-in WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310681"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="99202-103">Structures d’API de plug-in WinRM</span><span class="sxs-lookup"><span data-stu-id="99202-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="99202-104">Le tableau suivant fournit une vue d’ensemble des structures de l’interface de programmation d’applications (API) du plug-in Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="99202-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="99202-105">Structure</span><span class="sxs-lookup"><span data-stu-id="99202-105">Structure</span></span>                                                        | <span data-ttu-id="99202-106">Description</span><span class="sxs-lookup"><span data-stu-id="99202-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99202-107">**QUOTA d’autorisation WSMAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99202-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="99202-108">Définit les informations de quota pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="99202-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="99202-109">**\_Détails du certificat WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="99202-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="99202-110">Représente les champs dans le certificat client.</span><span class="sxs-lookup"><span data-stu-id="99202-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="99202-111">**jeu d’arguments de la \_ commande WSMan \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99202-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="99202-112">Représente l’ensemble des arguments passés à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="99202-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="99202-113">**\_filtre WSMan**</span><span class="sxs-lookup"><span data-stu-id="99202-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="99202-114">Définit le filtrage utilisé pour une opération.</span><span class="sxs-lookup"><span data-stu-id="99202-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="99202-115">**\_fragment WSMan**</span><span class="sxs-lookup"><span data-stu-id="99202-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="99202-116">Définit les informations de fragment pour une opération.</span><span class="sxs-lookup"><span data-stu-id="99202-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="99202-117">**\_informations sur l’opération WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="99202-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="99202-118">Représente un point de terminaison de ressource spécifique pour lequel le plug-in doit exécuter la demande.</span><span class="sxs-lookup"><span data-stu-id="99202-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="99202-119">**\_demande de plug-in WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="99202-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="99202-120">Contient des informations sur la demande et est passé à chaque opération de plug-in.</span><span class="sxs-lookup"><span data-stu-id="99202-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="99202-121">**Détails de l' \_ expéditeur WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="99202-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="99202-122">Spécifie les détails du client pour chaque demande entrante.</span><span class="sxs-lookup"><span data-stu-id="99202-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




