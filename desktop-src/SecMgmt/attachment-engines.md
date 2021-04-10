---
description: Un moteur d’attachement est une DLL qui gère les demandes d’analyse et de configuration spécifiques aux services.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Moteurs d’attachement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866962"
---
# <a name="attachment-engines"></a><span data-ttu-id="a3c74-103">Moteurs d’attachement</span><span class="sxs-lookup"><span data-stu-id="a3c74-103">Attachment Engines</span></span>

<span data-ttu-id="a3c74-104">Un moteur d’attachement est une DLL qui gère les demandes d’analyse et de configuration spécifiques aux services.</span><span class="sxs-lookup"><span data-stu-id="a3c74-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="a3c74-105">L’utilisateur effectue une demande de configuration et d’analyse spécifique au service à l’aide de l’extension du composant logiciel enfichable d’attachement.</span><span class="sxs-lookup"><span data-stu-id="a3c74-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="a3c74-106">Cette demande est ensuite transmise à travers les composants logiciels enfichables de configuration de sécurité du moteur de configuration de sécurité général, qui à son tour transmet le traitement propre au service au moteur d’attachement approprié.</span><span class="sxs-lookup"><span data-stu-id="a3c74-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="a3c74-107">Le moteur d’attachement se connecte ensuite au service et modifie sa configuration.</span><span class="sxs-lookup"><span data-stu-id="a3c74-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="a3c74-108">En d’autres termes, le moteur d’attachement fournit le traitement principal qui prend en charge l’extension de composant logiciel enfichable d’attachement.</span><span class="sxs-lookup"><span data-stu-id="a3c74-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="a3c74-109">Un moteur d’attachement doit implémenter les trois fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3c74-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="a3c74-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), qui calcule la différence entre la configuration du service et la configuration stockée dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="a3c74-111">Les différences sont écrites dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="a3c74-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), qui configure le service comme spécifié dans l’interface utilisateur du composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="a3c74-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="a3c74-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), qui met à jour la configuration de base et l’analyse de la configuration pour le service dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="a3c74-114">Pour simplifier l’implémentation des fonctions précédentes, le jeu d’outils de configuration de la sécurité fournit des fonctions et des structures de prise en charge que votre application peut utiliser pour interroger et définir des informations dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="a3c74-115">Pour plus d’informations, consultez [fonctions de rappel des pièces jointes](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a3c74-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="a3c74-116">Lorsque vous créez une DLL du moteur de pièces jointes, vous devez l’installer, puis l’inscrire auprès du moteur de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="a3c74-117">Pour inscrire la DLL, vous devez ajouter une clé spécifique au registre.</span><span class="sxs-lookup"><span data-stu-id="a3c74-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="a3c74-118">Lorsque le moteur de configuration de sécurité démarre, il vérifie le registre et charge toutes les dll du moteur de pièces jointes inscrites.</span><span class="sxs-lookup"><span data-stu-id="a3c74-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="a3c74-119">Il transmet ensuite les demandes d’analyse et de configuration spécifiques au service au moteur d’attachement approprié.</span><span class="sxs-lookup"><span data-stu-id="a3c74-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="a3c74-120">Les demandes de configuration et d’analyse standard, celles qui ne sont pas spécifiques au service, sont gérées par le moteur de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="a3c74-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 



