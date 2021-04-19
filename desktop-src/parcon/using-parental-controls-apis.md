---
description: Utilisation des API de contrôle parental
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Utilisation des API de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534498"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="cedd8-103">Utilisation des API de contrôle parental</span><span class="sxs-lookup"><span data-stu-id="cedd8-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="cedd8-104">Sélection de l’API</span><span class="sxs-lookup"><span data-stu-id="cedd8-104">API Selection</span></span>

<span data-ttu-id="cedd8-105">Comme indiqué dans la section vue d’ensemble, le développement implique l’utilisation de trois API au maximum :</span><span class="sxs-lookup"><span data-stu-id="cedd8-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="cedd8-106">Accès aux paramètres de base : l’API COM de conformité minimale des contrôles parentaux (API de conformité) est définie dans Wpcapi. h pour un accès simple à un sous-ensemble d’États de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="cedd8-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="cedd8-107">Accès en écriture/lecture des paramètres complets : l’utilisation d’un petit sous-ensemble de l’API COM WMI pour l’accès complet n’est requise que si l’ISV doit modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="cedd8-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="cedd8-108">L’ajout d’un lien d’extensibilité de l’interface utilisateur, le remplacement du filtre de contenu Web ou des ajouts aux listes d’exemptions d’application HTTP à l’ordinateur ou de filtrage d’URL sont principalement les raisons d’utiliser l’API.</span><span class="sxs-lookup"><span data-stu-id="cedd8-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="cedd8-109">Comme l’utilisation de l’espace de noms de contrôle parental WMI fournit un accès brut au magasin de paramètres sous-jacent, les éditeurs de logiciels indépendants doivent procéder avec prudence pour interpréter l’état des paramètres individuels qui peuvent en fait avoir des dépendances de passerelle sur d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="cedd8-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="cedd8-110">Par conséquent, il est recommandé d’utiliser l’API de conformité pour lire l’état de toutes les valeurs exposées par cette API.</span><span class="sxs-lookup"><span data-stu-id="cedd8-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="cedd8-111">Journalisation : l’API du système de rapports et de suivi d’événements de Windows Vista (également appelée ETW) pour la publication des événements d’activité dans les journaux de contrôle parental, conjointement avec les descripteurs d’événements et les énumérations de tableau définies dans WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="cedd8-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="cedd8-112">Toutes les API peuvent être appelées en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="cedd8-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="cedd8-113">Pour la journalisation, tout utilisateur peut consigner des événements de journal.</span><span class="sxs-lookup"><span data-stu-id="cedd8-113">For logging, any user may source log events.</span></span> <span data-ttu-id="cedd8-114">L’appel de pour extraire ou modifier les paramètres d’un autre utilisateur échoue si l’appelant ne dispose pas de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="cedd8-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="cedd8-115">En d’autres termes, un utilisateur standard peut uniquement accéder à ses propres paramètres et uniquement pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="cedd8-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="cedd8-116">Les paramètres et l’utilisation de l’API de journalisation sont décrits plus en détail dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="cedd8-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="cedd8-117">Utilisation des API de paramètres de contrôle parental</span><span class="sxs-lookup"><span data-stu-id="cedd8-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="cedd8-118">Utilisation des API de journalisation pour les contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="cedd8-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="cedd8-119">Environnement de développement</span><span class="sxs-lookup"><span data-stu-id="cedd8-119">Development Environment</span></span>

<span data-ttu-id="cedd8-120">Le développement pour les contrôles parentaux requiert l’accès à trois fichiers d’en-tête : WPC. h, WpcApi. h et WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="cedd8-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="cedd8-121">WPC. h est un collecteur qui inclut les paramètres API de conformité publique et en-têtes d’événement. par conséquent, il suffit d’inclure WPC. h dans le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="cedd8-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="cedd8-122">Les autorisations de lecture/écriture sur l’API WMI sont spécifiées par le fichier Wpcsprov. mof.</span><span class="sxs-lookup"><span data-stu-id="cedd8-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="cedd8-123">Ce fichier est installé dans le sous-répertoire WBEM sous le répertoire Windows system32.</span><span class="sxs-lookup"><span data-stu-id="cedd8-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="cedd8-124">Le kit de développement logiciel (SDK) Microsoft Windows contient un exemple de code pour renforcer l’exemple de code présenté ici et fournir des outils de ligne de commande simples pour l’exploration des API ou les tests d’intégration.</span><span class="sxs-lookup"><span data-stu-id="cedd8-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



