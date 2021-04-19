---
description: Ce document fournit des informations sur les considérations de sécurité liées à l’acquisition d’images Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considérations relatives à la sécurité : acquisition d’images Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514627"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="b7ec2-103">Considérations relatives à la sécurité : acquisition d’images Windows</span><span class="sxs-lookup"><span data-stu-id="b7ec2-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="b7ec2-104">Ce document fournit des informations sur les considérations de sécurité liées à l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="b7ec2-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="b7ec2-105">Ce document ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-le plutôt comme point de départ et référence pour ce domaine technologique.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="b7ec2-106">Utiliser des guillemets autour des noms de chemins</span><span class="sxs-lookup"><span data-stu-id="b7ec2-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="b7ec2-107">Placer les applications inscrites dans des emplacements sécurisés</span><span class="sxs-lookup"><span data-stu-id="b7ec2-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="b7ec2-108">N’utilisez pas les répertoires ou les clés de Registre sous-jacents</span><span class="sxs-lookup"><span data-stu-id="b7ec2-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="b7ec2-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7ec2-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="b7ec2-110">Utiliser des guillemets autour des noms de chemins</span><span class="sxs-lookup"><span data-stu-id="b7ec2-110">Use quotation marks around path names</span></span>

<span data-ttu-id="b7ec2-111">Quand vous utilisez [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) pour inscrire une application pour recevoir des événements de périphérique, veillez à placer le chemin d’accès et le nom de fichier de l’application entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="b7ec2-112">Cela évite de faire en sorte que le chemin d’accès soit mal interprété et qu’une application non autorisée soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="b7ec2-113">Placer les applications inscrites dans des emplacements sécurisés</span><span class="sxs-lookup"><span data-stu-id="b7ec2-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="b7ec2-114">Lorsqu’une application est inscrite pour recevoir un événement d’appareil, cette application peut être exécutée par n’importe quel utilisateur ayant accès à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="b7ec2-115">Par exemple, si une application est inscrite pour un événement d’analyse, le fait d’appuyer sur le bouton « Scan » (analyser) sur un scanneur entraîne l’exécution de cette application.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="b7ec2-116">Si l’application s’exécute avec un privilège plus élevé que celui de l’utilisateur, cela provoque un problème de sécurité potentiel.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="b7ec2-117">N’utilisez pas les répertoires ou les clés de Registre sous-jacents</span><span class="sxs-lookup"><span data-stu-id="b7ec2-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="b7ec2-118">WIA utilise plusieurs répertoires et clés de registre en interne pour stocker des données ou des informations.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="b7ec2-119">N’accédez pas directement à ces répertoires ou clés de registre.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="b7ec2-120">Utilisez plutôt les méthodes d’interface exposées pour spécifier des répertoires pour les images acquises.</span><span class="sxs-lookup"><span data-stu-id="b7ec2-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7ec2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7ec2-121">Related Topics</span></span>

-   [<span data-ttu-id="b7ec2-122">Sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="b7ec2-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="b7ec2-123">Page d’hébergement sur la sécurité de MSDN Library</span><span class="sxs-lookup"><span data-stu-id="b7ec2-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="b7ec2-124">Ressources de procédures pour la sécurité</span><span class="sxs-lookup"><span data-stu-id="b7ec2-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="b7ec2-125">Ressources de sécurité TechNet</span><span class="sxs-lookup"><span data-stu-id="b7ec2-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="b7ec2-126">[Considérations sur la sécurité pour les développeurs Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b7ec2-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="b7ec2-127">Meilleures pratiques de sécurité</span><span class="sxs-lookup"><span data-stu-id="b7ec2-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
