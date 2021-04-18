---
title: Protection des informations d’identification et applications tierces
description: Credential Guard ne permet pas aux fournisseurs SSP tiers de demander des hachages de mot de passe à l’autorité de sécurité locale.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463155"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="f04d8-103">Fournisseurs de support de sécurité tiers avec Credential Guard</span><span class="sxs-lookup"><span data-stu-id="f04d8-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="f04d8-104">Credential Guard ne permet pas aux fournisseurs SSP tiers de demander des hachages de mot de passe à l’autorité de sécurité locale.</span><span class="sxs-lookup"><span data-stu-id="f04d8-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="f04d8-105">Toutefois, les fournisseurs SSP et les points d’accès reçoivent toujours des notifications du mot de passe lorsqu’un utilisateur se connecte et/ou modifie son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f04d8-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="f04d8-106">Aucune utilisation d’API non documentées dans des fournisseurs SSP et des points d’accès personnalisés n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f04d8-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="f04d8-107">La profondeur et l’étendue des protections fournies par Credential Guard évoluant sans cesse, les versions ultérieures de Windows 10 avec Credential Guard peuvent affecter des scénarios qui fonctionnaient précédemment.</span><span class="sxs-lookup"><span data-stu-id="f04d8-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="f04d8-108">Par exemple, Credential Guard peut bloquer l’utilisation d’un type particulier d’informations d’identification ou d’un composant particulier pour empêcher les programmes malveillants de tirer parti des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="f04d8-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="f04d8-109">Par conséquent, nous recommandons que les scénarios nécessaires aux opérations d’une organisation soient testés avant de mettre à niveau un appareil sur lequel Credential Guard est exécuté.</span><span class="sxs-lookup"><span data-stu-id="f04d8-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="f04d8-110">Reportez-vous à [cet article](/windows/security/identity-protection/credential-guard/credential-guard) pour obtenir la description complète et les atténuations recommandées.</span><span class="sxs-lookup"><span data-stu-id="f04d8-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 