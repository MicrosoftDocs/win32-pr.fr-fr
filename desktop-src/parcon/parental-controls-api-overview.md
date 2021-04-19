---
description: Vue d’ensemble de l’API des contrôles parentaux
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Vue d’ensemble de l’API des contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538719"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="5df61-103">Vue d’ensemble de l’API des contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="5df61-103">Parental Controls API Overview</span></span>

<span data-ttu-id="5df61-104">Les API utilisées pour les contrôles parentaux exposent la stratégie et les paramètres de restrictions intégrés, ainsi que la fonctionnalité de journalisation.</span><span class="sxs-lookup"><span data-stu-id="5df61-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="5df61-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5df61-105">Settings</span></span>

<span data-ttu-id="5df61-106">Deux API publiques sont fournies :</span><span class="sxs-lookup"><span data-stu-id="5df61-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="5df61-107">Une API de conformité minimale basée sur COM légère (appelée API de conformité) principalement pour les applications afin de déterminer si la journalisation doit être activée.</span><span class="sxs-lookup"><span data-stu-id="5df61-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="5df61-108">En outre, des méthodes simples sont fournies pour :</span><span class="sxs-lookup"><span data-stu-id="5df61-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="5df61-109">Récupération de l’état des restrictions pour les restrictions Web, limites de temps, restrictions de jeux et restrictions d’application.</span><span class="sxs-lookup"><span data-stu-id="5df61-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="5df61-110">Récupération de l’ID du filtre de contenu Web actif.</span><span class="sxs-lookup"><span data-stu-id="5df61-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="5df61-111">Déterminer si les éléments de l’interface utilisateur du fournisseur doivent être affichés, de manière cohérente avec le masquage par zone dans le cas d’une jointure à un domaine.</span><span class="sxs-lookup"><span data-stu-id="5df61-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="5df61-112">Récupération de l’heure de la dernière modification d’un paramètre pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5df61-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="5df61-113">La récupération des téléchargements de fichiers basés sur un navigateur ou un navigateur doit être bloquée pour un utilisateur, ainsi que la possibilité de demander à une URL d’être spécifiquement autorisée par le filtre de contenu Web pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5df61-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="5df61-114">Déterminer si un jeu donné est bloqué pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5df61-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="5df61-115">API Windows Management Instrumentation (WMI) accès à un espace de noms de contrôle parental pour un accès en lecture et en écriture complet à tous les paramètres exposés.</span><span class="sxs-lookup"><span data-stu-id="5df61-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="5df61-116">Le contrôle parental déploie un fournisseur WMI pour gérer les autorisations de lecture/écriture sur le magasin de paramètres sous-jacent, avec la mise en œuvre appropriée des privilèges pour les administrateurs et les utilisateurs contrôlés.</span><span class="sxs-lookup"><span data-stu-id="5df61-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="5df61-117">Les éditeurs de logiciels indépendants sont invités à utiliser l’API de conformité et l’API WMI si nécessaire pour contrôler les restrictions appropriées pour la sécurité des enfants en fonction de la fonctionnalité de l’application ou de la solution.</span><span class="sxs-lookup"><span data-stu-id="5df61-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="5df61-118">Journalisation</span><span class="sxs-lookup"><span data-stu-id="5df61-118">Logging</span></span>

-   <span data-ttu-id="5df61-119">Les API de publication et de consommation des événements Windows standard sont utilisées pour la surveillance de l’activité des contrôles parentaux.</span><span class="sxs-lookup"><span data-stu-id="5df61-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="5df61-120">Le système de suivi et de rapport d’événements de Windows Vista a amélioré les performances par rapport à la fonctionnalité de Suivi d’v nements pour Windows (ETW) précédente.</span><span class="sxs-lookup"><span data-stu-id="5df61-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="5df61-121">Le contrôle parental définit un canal unique pour ses données dans ETW.</span><span class="sxs-lookup"><span data-stu-id="5df61-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="5df61-122">Les éditeurs de logiciels indépendants sont invités à utiliser l’API de publication d’événements pour enregistrer l’activité des utilisateurs comme spécifié dans la section utilisation des API de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="5df61-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



