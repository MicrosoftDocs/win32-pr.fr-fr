---
description: Mode protégé
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Mode protégé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116447"
---
# <a name="protected-mode"></a><span data-ttu-id="95d0b-103">Mode protégé</span><span class="sxs-lookup"><span data-stu-id="95d0b-103">Protected Mode</span></span>

<span data-ttu-id="95d0b-104">La plupart des fonctionnalités de sécurité de Windows Internet Explorer 8 sont disponibles dans Internet Explorer 8 pour le système d’exploitation Windows XP avec Service Pack 2 (SP2) et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95d0b-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="95d0b-105">Le mode protégé est disponible uniquement pour Windows Vista ou versions ultérieures, car il est basé sur les fonctionnalités de sécurité suivantes qui sont nouvelles dans Windows Vista :</span><span class="sxs-lookup"><span data-stu-id="95d0b-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="95d0b-106">[Le contrôle de compte d’utilisateur (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilite l’exécution sans privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="95d0b-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="95d0b-107">Lorsque les utilisateurs exécutent des programmes avec des privilèges utilisateur limités, ils sont plus sûrs contre une attaque que lorsqu’ils s’exécutent avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="95d0b-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="95d0b-108">Le système d’exploitation Windows peut empêcher le code malveillant d’effectuer des actions nuisibles.</span><span class="sxs-lookup"><span data-stu-id="95d0b-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="95d0b-109">Un mécanisme d’intégrité restreint l’accès en écriture aux [objets sécurisables](../secauthz/securable-objects.md) par des processus de plus faible intégrité, de la même façon que l’appartenance aux groupes de comptes d’utilisateur restreint les droits des utilisateurs à accéder aux composants système sensibles.</span><span class="sxs-lookup"><span data-stu-id="95d0b-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="95d0b-110">L’isolation des privilèges de l' [interface utilisateur (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) empêche les processus d’envoyer des messages de fenêtre sélectionnés et d’autres API utilisateur aux processus qui s’exécutent avec une intégrité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="95d0b-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="95d0b-111">L’infrastructure de sécurité du mécanisme d’intégrité Windows permet au mode protégé de fournir à Windows Internet Explorer les privilèges dont les utilisateurs ont besoin pour naviguer sur le Web, tout en disposant des privilèges dont les utilisateurs ont besoin pour installer des programmes en mode silencieux ou pour modifier les données système sensibles.</span><span class="sxs-lookup"><span data-stu-id="95d0b-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="95d0b-112">Les utilisateurs peuvent désactiver cette fonctionnalité par le biais d’une case à cocher, et les administrateurs peuvent la désactiver à l’aide de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="95d0b-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95d0b-113">Vous ne devez désactiver la fonctionnalité qu’en tant que mesure temporaire pendant la résolution des problèmes pour comparer le comportement de l’application lorsque celle-ci est activée ou non.</span><span class="sxs-lookup"><span data-stu-id="95d0b-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="95d0b-114">Nous vous recommandons de conserver cette fonctionnalité activée de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="95d0b-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="95d0b-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95d0b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95d0b-116">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="95d0b-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
