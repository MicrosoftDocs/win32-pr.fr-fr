---
description: Explique l’utilisation des jetons d’emprunt d’identité dans le contrôle d’accès.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Jetons d’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524408"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="6219f-103">Jetons d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="6219f-103">Impersonation Tokens</span></span>

<span data-ttu-id="6219f-104">Un thread d’emprunt d’identité a deux [*jetons d’accès*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="6219f-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="6219f-105">[*Jeton d’accès principal*](/windows/desktop/SecGloss/p-gly) qui décrit le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du serveur.</span><span class="sxs-lookup"><span data-stu-id="6219f-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="6219f-106">Pour obtenir un descripteur de ce jeton, appelez la fonction [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="6219f-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="6219f-107">Un jeton d’accès d’emprunt d’identité qui décrit le contexte de sécurité du client dont l’identité est empruntée.</span><span class="sxs-lookup"><span data-stu-id="6219f-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="6219f-108">Pour obtenir un descripteur de ce jeton, appelez la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .</span><span class="sxs-lookup"><span data-stu-id="6219f-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="6219f-109">Un serveur peut utiliser le [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly) dans les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6219f-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="6219f-110">Dans les fonctions [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)et [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) pour déterminer si un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) permet au client un ensemble de droits d’accès.</span><span class="sxs-lookup"><span data-stu-id="6219f-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="6219f-111">Dans la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer ou désactiver les privilèges du client.</span><span class="sxs-lookup"><span data-stu-id="6219f-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="6219f-112">Dans la fonction [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) pour déterminer si un jeu de privilèges est activé dans le jeton du client.</span><span class="sxs-lookup"><span data-stu-id="6219f-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="6219f-113">Dans les fonctions qui génèrent des entrées dans le journal des événements de sécurité, telles que [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) ou [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="6219f-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="6219f-114">Ces fonctions utilisent un jeton d’emprunt d’identité pour obtenir des informations sur le client pour l’entrée de journal.</span><span class="sxs-lookup"><span data-stu-id="6219f-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
