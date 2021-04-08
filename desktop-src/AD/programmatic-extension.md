---
title: Extension de programmation
description: Les extensions de programmation ont plusieurs avantages, toutefois, une application est opaque ; l’administrateur doit faire confiance à la documentation fournie avec l’application d’installation.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extension de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671254"
---
# <a name="programmatic-extension"></a><span data-ttu-id="fb923-104">Extension de programmation</span><span class="sxs-lookup"><span data-stu-id="fb923-104">Programmatic Extension</span></span>

<span data-ttu-id="fb923-105">L’avantage d’un fichier LDIF est que l’administrateur peut examiner sa fonction.</span><span class="sxs-lookup"><span data-stu-id="fb923-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="fb923-106">Toutefois, le schéma peut également être étendu par programmation.</span><span class="sxs-lookup"><span data-stu-id="fb923-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="fb923-107">Les extensions de programmation ont plusieurs avantages, mais une application est opaque ; l’administrateur doit faire confiance à la documentation fournie avec l’application d’installation.</span><span class="sxs-lookup"><span data-stu-id="fb923-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="fb923-108">L’utilisation d’extensions de schéma de programmation peut être un obstacle au déploiement pour les applications qui les utilisent.</span><span class="sxs-lookup"><span data-stu-id="fb923-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="fb923-109">Une extension de programmation est indifférente ; Il s’agit d’un fichier exécutable Windows NT.</span><span class="sxs-lookup"><span data-stu-id="fb923-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="fb923-110">Le binaire ne peut pas être falsifié, contrairement à un fichier LDIF ou. csv, qui peut être modifié par inadvertance ou par malveillance.</span><span class="sxs-lookup"><span data-stu-id="fb923-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="fb923-111">Les avantages d’un fichier LDIF sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fb923-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="fb923-112">Les applications peuvent détecter et récupérer des erreurs et fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb923-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="fb923-113">Les applications peuvent gérer Unicode sans avoir recours à l’encodage Base64.</span><span class="sxs-lookup"><span data-stu-id="fb923-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="fb923-114">Les applications peuvent tirer parti des API d’installation Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fb923-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="fb923-115">Les applications peuvent être signées pour établir l’authenticité.</span><span class="sxs-lookup"><span data-stu-id="fb923-115">Applications can be signed to establish authenticity.</span></span>

 

 




