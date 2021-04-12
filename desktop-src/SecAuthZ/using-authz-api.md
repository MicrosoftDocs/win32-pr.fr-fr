---
description: L’API auth permet aux applications d’effectuer des vérifications d’accès personnalisables avec de meilleures performances et un développement plus simplifié que les Access Control de bas niveau.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Utilisation de l’API auth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320858"
---
# <a name="using-authz-api"></a><span data-ttu-id="089cf-103">Utilisation de l’API auth</span><span class="sxs-lookup"><span data-stu-id="089cf-103">Using Authz API</span></span>

<span data-ttu-id="089cf-104">L’API auth permet aux applications d’effectuer des vérifications d’accès personnalisables avec de meilleures performances et un développement plus simplifié que les [Access Control de bas niveau](low-level-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="089cf-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="089cf-105">AUTH API permet aux applications de mettre en cache les contrôles d’accès pour améliorer les performances, d’interroger et de modifier les contextes du client, et de définir des règles d’entreprise qui peuvent être utilisées pour évaluer dynamiquement l’autorisation d’accès.</span><span class="sxs-lookup"><span data-stu-id="089cf-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="089cf-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="089cf-106">In This Section</span></span>



| <span data-ttu-id="089cf-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="089cf-107">Topic</span></span>                                                                             | <span data-ttu-id="089cf-108">Description</span><span class="sxs-lookup"><span data-stu-id="089cf-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="089cf-109">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="089cf-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="089cf-110">Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.</span><span class="sxs-lookup"><span data-stu-id="089cf-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="089cf-111">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="089cf-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="089cf-112">Les applications peuvent appeler la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) pour demander des informations sur un contexte client existant.</span><span class="sxs-lookup"><span data-stu-id="089cf-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="089cf-113">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="089cf-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="089cf-114">Une application peut ajouter des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) à un contexte client existant en appelant la fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="089cf-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="089cf-115">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="089cf-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="089cf-116">Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="089cf-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="089cf-117">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="089cf-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="089cf-118">Quand une application effectue une vérification d’accès en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , les résultats de cette vérification d’accès peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="089cf-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

