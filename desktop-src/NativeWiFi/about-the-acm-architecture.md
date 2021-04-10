---
description: À propos de l’architecture ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: À propos de l’architecture ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210447"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="c27b5-103">À propos de l’architecture ACM</span><span class="sxs-lookup"><span data-stu-id="c27b5-103">About the ACM Architecture</span></span>

<span data-ttu-id="c27b5-104">Le module d’auto-configuration (ACM) est le nouveau composant de configuration sans fil pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c27b5-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="c27b5-105">Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2) utilisent à la place le service de configuration automatique sans fil (WZC).</span><span class="sxs-lookup"><span data-stu-id="c27b5-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="c27b5-106">L’ACM balaie régulièrement les réseaux et utilise un processus itératif pour sélectionner le réseau le plus favori de la plage et s’y connecter, si une interface est activée pour la connexion automatique sur ce réseau.</span><span class="sxs-lookup"><span data-stu-id="c27b5-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="c27b5-107">L’ACM enregistre et récupère également les profils réseau, qui contiennent des paramètres d’ACM, de module spécifique aux médias (MSM), de sécurité et de fabricants de matériel indépendant.</span><span class="sxs-lookup"><span data-stu-id="c27b5-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="c27b5-108">Ces profils réseau sont destinés à la configuration automatique.</span><span class="sxs-lookup"><span data-stu-id="c27b5-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="c27b5-109">La configuration automatique prend en charge les paramètres globaux et par interface et les profils réseau.</span><span class="sxs-lookup"><span data-stu-id="c27b5-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="c27b5-110">Les paramètres globaux et les profils réseau sont configurés si l’ordinateur a rejoint un domaine avec un objet de stratégie de groupe (GPO) au niveau du domaine ou de l’unité d’organisation (UO) dans la hiérarchie Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="c27b5-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="c27b5-111">Ces paramètres et profils de stratégie de groupe sont en lecture seule, appliqués à chaque interface 802,11 dans le système, et sont toujours prioritaires sur les paramètres par interface et par utilisateur et les profils réseau.</span><span class="sxs-lookup"><span data-stu-id="c27b5-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="c27b5-112">Les profils de stratégie de groupe sont placés en haut de la liste des profils réseau préférés sur chaque interface réseau 802,11.</span><span class="sxs-lookup"><span data-stu-id="c27b5-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="c27b5-113">L’architecture ACM est extensible.</span><span class="sxs-lookup"><span data-stu-id="c27b5-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="c27b5-114">Les IHV peuvent implémenter une fonctionnalité sans fil propriétaire sans altérer l’infrastructure 802,11 native fournie.</span><span class="sxs-lookup"><span data-stu-id="c27b5-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="c27b5-115">Les structures et fonctions de contrôle IHV exposées activent cette extensibilité.</span><span class="sxs-lookup"><span data-stu-id="c27b5-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c27b5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c27b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c27b5-117">À propos de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="c27b5-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



