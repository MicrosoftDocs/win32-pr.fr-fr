---
description: Pour déléguer les informations d’identification au protocole CredSSP (Credential Security Support Provider Protocol), vous devez spécifier les serveurs auxquels il est possible de déléguer.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Paramètres stratégie de groupe CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524283"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="cbc2e-103">Paramètres stratégie de groupe CredSSP</span><span class="sxs-lookup"><span data-stu-id="cbc2e-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="cbc2e-104">Pour déléguer les informations d’identification au [protocole CredSSP (Credential Security Support Provider Protocol)](credential-security-support-provider.md) , vous devez spécifier les serveurs auxquels il est possible de déléguer.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="cbc2e-105">Pour spécifier ces serveurs, modifiez les paramètres dans le composant logiciel enfichable MMC (Microsoft Management Console) de l’éditeur de stratégie de groupe (GPE).</span><span class="sxs-lookup"><span data-stu-id="cbc2e-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="cbc2e-106">Les paramètres GPE qui contrôlent la délégation sont sous **Configuration ordinateur \| modèles d’administration la délégation des \| \| informations d’identification système**.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="cbc2e-107">Il ne s’agit pas d’une délégation restreinte.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-107">This is not constrained delegation.</span></span> <span data-ttu-id="cbc2e-108">CredSSP transmet les informations d’identification complètes de l’utilisateur au serveur sans aucune contrainte.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="cbc2e-109">Les paramètres de stratégie de groupe contrôlent la délégation des types d’informations d’identification suivants.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="cbc2e-110">Type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="cbc2e-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="cbc2e-111">Description</span><span class="sxs-lookup"><span data-stu-id="cbc2e-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc2e-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Informations d’identification par défaut</span><span class="sxs-lookup"><span data-stu-id="cbc2e-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="cbc2e-113">Informations d’identification obtenues lorsque l’utilisateur se connecte pour la première fois à Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="cbc2e-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Nouvelles informations d’identification</span><span class="sxs-lookup"><span data-stu-id="cbc2e-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="cbc2e-115">Informations d’identification demandées par l’utilisateur lors de l’exécution d’une application.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="cbc2e-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Informations d’identification enregistrées</span><span class="sxs-lookup"><span data-stu-id="cbc2e-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="cbc2e-117">Informations d’identification enregistrées à l’aide du [Gestionnaire d’informations d’identification](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="cbc2e-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="cbc2e-118">Pour inclure un serveur dans la catégorie associée à un paramètre de stratégie de groupe particulier, ajoutez le [*nom de principal du service*](/windows/desktop/SecGloss/s-gly) (SPN) de ce serveur à la liste des serveurs de ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="cbc2e-119">Le nom de principal du service peut contenir un caractère générique unique.</span><span class="sxs-lookup"><span data-stu-id="cbc2e-119">The SPN can contain a single wildcard character.</span></span>

 

