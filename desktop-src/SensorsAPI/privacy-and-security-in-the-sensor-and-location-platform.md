---
description: La plate-forme capteur et emplacement Windows comprend des paramètres de confidentialité pour aider à protéger les informations personnelles des utilisateurs.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Confidentialité et sécurité dans la plate-forme capteur et emplacement Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514802"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="45090-103">Confidentialité et sécurité dans la plate-forme capteur et emplacement Windows</span><span class="sxs-lookup"><span data-stu-id="45090-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="45090-104">La plate-forme capteur et emplacement Windows comprend des paramètres de confidentialité pour aider à protéger les informations personnelles des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="45090-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="45090-105">La plateforme permet de s’assurer que les données de capteur restent privées, lorsque la confidentialité est requise, de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="45090-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="45090-106">Par défaut, les capteurs sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="45090-106">By default, sensors are off.</span></span> <span data-ttu-id="45090-107">Étant donné que la conception de la plateforme suppose que tous les capteurs peuvent fournir des données personnelles, chaque capteur est désactivé jusqu’à ce que l’utilisateur fournisse un consentement explicite pour accéder aux données de capteur.</span><span class="sxs-lookup"><span data-stu-id="45090-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="45090-108">Windows fournit des messages de divulgation et des informations d’aide pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45090-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="45090-109">Ce contenu aide les utilisateurs à comprendre comment les capteurs peuvent affecter la confidentialité de leurs données personnelles et aide les utilisateurs à prendre des décisions avisées.</span><span class="sxs-lookup"><span data-stu-id="45090-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="45090-110">L’autorisation d’un capteur nécessite des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="45090-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="45090-111">Lorsqu’il est activé, un périphérique de capteur fonctionne pour tous les programmes s’exécutant sous un compte d’utilisateur particulier (ou pour tous les comptes d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="45090-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="45090-112">Cela comprend les utilisateurs et les services non interactifs, tels que ASPNET ou SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="45090-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="45090-113">Par exemple, si vous activez un capteur GPS pour votre compte d’utilisateur, seuls les programmes qui s’exécutent sous votre compte d’utilisateur ont accès au GPS.</span><span class="sxs-lookup"><span data-stu-id="45090-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="45090-114">Si vous activez le GPS pour tous les utilisateurs, tout programme s’exécutant sous n’importe quel compte d’utilisateur a accès au GPS.</span><span class="sxs-lookup"><span data-stu-id="45090-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="45090-115">Les programmes qui utilisent des capteurs peuvent appeler une méthode pour ouvrir une boîte de dialogue système qui invite les utilisateurs à activer les périphériques de capteur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="45090-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="45090-116">Cette fonctionnalité permet aux développeurs et aux utilisateurs de s’assurer que les capteurs fonctionnent quand les programmes en ont besoin, tout en conservant le contrôle de la divulgation des données de capteur par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45090-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="45090-117">Les pilotes de capteur utilisent un objet spécial qui traite toutes les demandes d’e/s.</span><span class="sxs-lookup"><span data-stu-id="45090-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="45090-118">Cet objet permet de s’assurer que seuls les programmes qui disposent de l’autorisation utilisateur peuvent accéder aux données de capteur.</span><span class="sxs-lookup"><span data-stu-id="45090-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



