---
description: L’ensemble d’outils de configuration de sécurité Microsoft est un ensemble d’outils MMC (Microsoft Management Console) qui simplifient la configuration et l’analyse de la sécurité du système.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Pièces jointes de sécurité de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318213"
---
# <a name="service-security-attachments"></a><span data-ttu-id="77f81-103">Pièces jointes de sécurité de service</span><span class="sxs-lookup"><span data-stu-id="77f81-103">Service Security Attachments</span></span>

<span data-ttu-id="77f81-104">L’ensemble d’outils de configuration de sécurité Microsoft est un ensemble d’outils MMC (Microsoft Management Console) qui simplifient la configuration et l’analyse de la sécurité du système.</span><span class="sxs-lookup"><span data-stu-id="77f81-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="77f81-105">Certains services, toutefois, ont des besoins de configuration spécialisés qui vont au-delà des paramètres de sécurité fournis par le jeu d’outils standard.</span><span class="sxs-lookup"><span data-stu-id="77f81-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="77f81-106">Pour gérer ces besoins, vous pouvez étendre les fonctionnalités de l’ensemble d’outils en écrivant une pièce jointe qui gère les tâches de sécurité spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="77f81-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="77f81-107">Par exemple, le spouleur est un service Windows NT qui définit des objets privés, qui doivent être sécurisés, par exemple des imprimantes.</span><span class="sxs-lookup"><span data-stu-id="77f81-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="77f81-108">Cette fonctionnalité n’est pas gérée par le jeu d’outils standard et nécessite donc une pièce jointe pour gérer la configuration et l’analyse des objets d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="77f81-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="77f81-109">La configuration des paramètres de sécurité généraux, tels que la stratégie d’appel de service, est toujours gérée par le jeu d’outils de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="77f81-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="77f81-110">Les pièces jointes du service de sécurité étendent les fonctionnalités de l’outil de configuration de la sécurité défini pour prendre en charge les configurations spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="77f81-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="77f81-111">Une pièce jointe comporte deux composants :</span><span class="sxs-lookup"><span data-stu-id="77f81-111">An attachment has two components:</span></span>

-   <span data-ttu-id="77f81-112">Extension de composant logiciel enfichable MMC qui implémente l’interface utilisateur de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="77f81-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="77f81-113">Moteur d’attachement qui traite les tâches d’analyse et de configuration de la sécurité spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="77f81-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="77f81-114">L’extension du composant logiciel enfichable pièce jointe est hébergée par les composants logiciels enfichables de configuration de sécurité. Il s’agit de composants logiciels enfichables MMC qui fournissent à l’utilisateur des interfaces permettant de configurer et d’analyser les paramètres de sécurité généraux d’un service.</span><span class="sxs-lookup"><span data-stu-id="77f81-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="77f81-115">Les paramètres spécifiques au service sont configurés à l’aide de l’extension du composant logiciel enfichable pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="77f81-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="77f81-116">Lorsque l’utilisateur modifie un paramètre de configuration, les composants logiciels enfichables de configuration de la sécurité stockent les nouvelles informations et transmettent la demande au moteur de configuration de sécurité.</span><span class="sxs-lookup"><span data-stu-id="77f81-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="77f81-117">Le moteur traite la demande et définit le service sur la nouvelle configuration.</span><span class="sxs-lookup"><span data-stu-id="77f81-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="77f81-118">Si la requête affecte un paramètre de sécurité standard, elle est gérée par le moteur.</span><span class="sxs-lookup"><span data-stu-id="77f81-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="77f81-119">Si la demande est spécifique au service, le moteur appelle le moteur d’attachement approprié pour gérer la demande.</span><span class="sxs-lookup"><span data-stu-id="77f81-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="77f81-120">L’illustration suivante montre comment le moteur de pièce jointe et l’extension du composant logiciel enfichable fonctionnent dans le cadre du jeu d’outils de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="77f81-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![moteur de pièce jointe et composants logiciels enfichables](images/model1a.png)

<span data-ttu-id="77f81-122">Pour plus d’informations sur l’utilisation du jeu d’outils de configuration de sécurité Microsoft, recherchez Configuration de la sécurité à l’aide de votre moteur de recherche préféré.</span><span class="sxs-lookup"><span data-stu-id="77f81-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



