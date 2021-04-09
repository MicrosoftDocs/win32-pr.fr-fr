---
description: Security Center Windows
ms.assetid: FF0D7B81-AFDC-4DB2-B2B0-0D2536B2757B
title: Security Center Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694185b0a0fed7af9c2ab3d7965674c02354c079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110074"
---
# <a name="windows-security-center"></a><span data-ttu-id="35a30-103">Security Center Windows</span><span class="sxs-lookup"><span data-stu-id="35a30-103">Windows Security Center</span></span>

<span data-ttu-id="35a30-104">Windows Security Center (WSC) est un outil de création de rapports complet qui aide les utilisateurs à établir et maintenir une couche de sécurité de protection autour de leurs systèmes informatiques.</span><span class="sxs-lookup"><span data-stu-id="35a30-104">Windows Security Center (WSC) is a comprehensive reporting tool that helps users establish and maintain a protective security layer around their computer systems.</span></span> <span data-ttu-id="35a30-105">Une fois qu’une couche de sécurité est établie, Windows Security Center est invisible lors de l’analyse de l’état d’intégrité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="35a30-105">Once a security layer is established, Windows Security Center is inconspicuous as it monitors the computer’s health state.</span></span> <span data-ttu-id="35a30-106">Toutefois, si des vulnérabilités existent, le WSC fournit des alertes et des conseils pour aider l’utilisateur à atteindre un état sécurisé qui est exposé à l’utilisateur final via le centre de maintenance.</span><span class="sxs-lookup"><span data-stu-id="35a30-106">However, if vulnerabilities exist, WSC provides alerts and prescriptive guidance to assist the user in achieving a secure state which is surfaced to the end user through the Action Center.</span></span>

<span data-ttu-id="35a30-107">Pour que les solutions de sécurité tierces (antivirus, logiciel anti-programme malveillant ou anti-logiciel espion) soient conformes à Windows et signalent correctement l’État au centre de maintenance, elles doivent s’inscrire auprès de Security Center et signaler les modifications d’État ultérieures à l’aide d’API privées pour communiquer avec le groupe de sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="35a30-107">In order for third party security solutions (antivirus, antimalware, or antispyware) to be compliant with Windows and successfully report status to Action Center, they are required to register themselves with Security Center and report any subsequent status changes using private APIs for communicating with WSC.</span></span> <span data-ttu-id="35a30-108">Le catalogue WSC, à son tour, communique ces mises à jour au centre de maintenance, où elles sont finalement affichées à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="35a30-108">WSC, in turn, communicates these updates to Action Center, where they are finally displayed to the end user.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35a30-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="35a30-109">In this section</span></span>

-   [<span data-ttu-id="35a30-110">Énumérations Windows Security Center</span><span class="sxs-lookup"><span data-stu-id="35a30-110">Windows Security Center Enumerations</span></span>](windows-security-center-enumerations.md)
-   [<span data-ttu-id="35a30-111">Interfaces Windows Security Center</span><span class="sxs-lookup"><span data-stu-id="35a30-111">Windows Security Center Interfaces</span></span>](windows-security-center-interfaces.md)
-   [<span data-ttu-id="35a30-112">Fonctions Windows Security Center</span><span class="sxs-lookup"><span data-stu-id="35a30-112">Windows Security Center Functions</span></span>](windows-security-center-functions.md)

 

 



