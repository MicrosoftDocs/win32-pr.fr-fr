---
description: Le remplacement des ressources protégées est pris en charge par les mécanismes suivants.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mécanismes de remplacement des ressources pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545062"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="61b60-103">Mécanismes de remplacement des ressources pris en charge</span><span class="sxs-lookup"><span data-stu-id="61b60-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="61b60-104">Le remplacement des ressources protégées est pris en charge par les mécanismes suivants.</span><span class="sxs-lookup"><span data-stu-id="61b60-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="61b60-105">L’autorisation d’accès complet pour modifier les ressources protégées par WRP sur Windows Vista et Windows Server 2008 est limitée à TrustedInstaller avec le service d’installation de modules Windows à l’aide des mécanismes suivants :</span><span class="sxs-lookup"><span data-stu-id="61b60-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="61b60-106">Service Packs Windows installés par TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="61b60-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="61b60-107">Correctifs installés par TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="61b60-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="61b60-108">Mises à niveau du système d’exploitation installées par TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="61b60-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="61b60-109">Windows Update installé par TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="61b60-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="61b60-110">Les applications et les programmes d’installation qui tentent de remplacer une ressource protégée par WRP par un autre moyen que les méthodes spécifiées se voient refuser l’accès pour modifier la ressource et générer un message d’erreur d’accès refusé.</span><span class="sxs-lookup"><span data-stu-id="61b60-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="61b60-111">Pour les programmes d’installation connus qui tentent de remplacer les ressources protégées par WRP, le message d’erreur et d’erreur Accès refusé peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="61b60-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="61b60-112">Dans ce cas, l’opération retourne avec succès, le message d’erreur et d’erreur est supprimé, mais aucune modification n’est appliquée à la ressource protégée par WRP.</span><span class="sxs-lookup"><span data-stu-id="61b60-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="61b60-113">L’erreur peut être supprimée pour un programme d’installation connu uniquement lorsque tous les critères suivants sont remplis :</span><span class="sxs-lookup"><span data-stu-id="61b60-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="61b60-114">Il s’agit d’une application héritée.</span><span class="sxs-lookup"><span data-stu-id="61b60-114">This is a legacy application.</span></span> <span data-ttu-id="61b60-115">L’application n’inclut pas de manifeste avec un requestedExecutionlevel qui identifie l’application telle qu’elle est conçue pour Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="61b60-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="61b60-116">L’erreur Accès refusé est due uniquement à la tentative de modification d’une ressource protégée par WRP.</span><span class="sxs-lookup"><span data-stu-id="61b60-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="61b60-117">Un administrateur installe l’application.</span><span class="sxs-lookup"><span data-stu-id="61b60-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="61b60-118">Pour plus d’informations sur l’utilisation de l’Windows Installer avec WRP, consultez [utilisation de Windows Installer et de protection des ressources Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) dans le kit de développement logiciel (SDK) [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .</span><span class="sxs-lookup"><span data-stu-id="61b60-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="61b60-119">**Windows Server 2003 et Windows XP :** Le remplacement des fichiers système protégés par WFP est pris en charge uniquement par le biais des mécanismes suivants :</span><span class="sxs-lookup"><span data-stu-id="61b60-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="61b60-120">Installation du Service Pack Windows à l’aide de Update.exe</span><span class="sxs-lookup"><span data-stu-id="61b60-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="61b60-121">Correctifs installés à l’aide de Hotfix.exe</span><span class="sxs-lookup"><span data-stu-id="61b60-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="61b60-122">Mises à niveau du système d’exploitation à l’aide de Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="61b60-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="61b60-123">Windows Update</span><span class="sxs-lookup"><span data-stu-id="61b60-123">Windows Update</span></span>

<span data-ttu-id="61b60-124">Le remplacement de fichiers protégés par d’autres moyens que ceux spécifiés entraîne la restauration des fichiers d’origine par WFP.</span><span class="sxs-lookup"><span data-stu-id="61b60-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
