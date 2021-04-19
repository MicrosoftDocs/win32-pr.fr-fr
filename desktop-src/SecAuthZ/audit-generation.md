---
description: Les exigences de sécurité de niveau C2 spécifient que les administrateurs système doivent être en mesure d’auditer les événements liés à la sécurité et que l’accès à ces données d’audit doit être limité aux administrateurs autorisés.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Génération de l’audit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535597"
---
# <a name="audit-generation"></a><span data-ttu-id="bfe2a-103">Génération de l’audit</span><span class="sxs-lookup"><span data-stu-id="bfe2a-103">Audit Generation</span></span>

<span data-ttu-id="bfe2a-104">Les exigences de sécurité de niveau C2 spécifient que les administrateurs système doivent être en mesure d’auditer les événements liés à la sécurité et que l’accès à ces données d’audit doit être limité aux administrateurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="bfe2a-105">L’API Windows fournit des fonctions permettant à un administrateur de surveiller les événements liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="bfe2a-106">Le descripteur de sécurité d’un objet sécurisable peut avoir une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="bfe2a-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="bfe2a-107">Une liste SACL contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) qui spécifient les types de tentatives d’accès qui génèrent des rapports d’audit.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="bfe2a-108">Chaque ACE identifie un tiers de confiance, un ensemble de droits d’accès et un ensemble d’indicateurs qui indiquent si le système génère des messages d’audit pour les échecs de tentative d’accès, les tentatives d’accès réussies ou les deux.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="bfe2a-109">Le système écrit des messages d’audit dans le journal des événements de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="bfe2a-110">Pour plus d’informations sur l’accès aux enregistrements dans un journal des événements de sécurité, consultez [journalisation des événements](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="bfe2a-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="bfe2a-111">Pour lire ou écrire la liste SACL d’un objet, un thread doit d’abord activer le \_ privilège de nom de sécurité se \_ .</span><span class="sxs-lookup"><span data-stu-id="bfe2a-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="bfe2a-112">Pour plus d’informations, consultez [droit d’accès SACL](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="bfe2a-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="bfe2a-113">L’API Windows fournit également une prise en charge pour les applications serveur afin de générer des messages d’audit lorsqu’un client tente d’accéder à un objet privé.</span><span class="sxs-lookup"><span data-stu-id="bfe2a-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="bfe2a-114">Pour plus d’informations, consultez [audit de l’accès aux objets privés](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bfe2a-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
