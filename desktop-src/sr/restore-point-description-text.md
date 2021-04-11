---
title: Texte de description du point de restauration
description: Quand une application appelle la fonction SRSetRestorePoint, elle peut fournir n’importe quel texte comme description pour le point de restauration. Toutefois, le tableau suivant indique le texte de description recommandé.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196876"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="f9caf-103">Texte de description du point de restauration</span><span class="sxs-lookup"><span data-stu-id="f9caf-103">Restore Point Description Text</span></span>

<span data-ttu-id="f9caf-104">Quand une application appelle la fonction [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , elle peut fournir n’importe quel texte comme description pour le point de restauration. Toutefois, le tableau suivant indique le texte de description recommandé.</span><span class="sxs-lookup"><span data-stu-id="f9caf-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="f9caf-105">Modification du système</span><span class="sxs-lookup"><span data-stu-id="f9caf-105">System modification</span></span>                            | <span data-ttu-id="f9caf-106">Type de point de restauration</span><span class="sxs-lookup"><span data-stu-id="f9caf-106">Restore point type</span></span>      | <span data-ttu-id="f9caf-107">Description</span><span class="sxs-lookup"><span data-stu-id="f9caf-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="f9caf-108">Installation d’application</span><span class="sxs-lookup"><span data-stu-id="f9caf-108">Application installation</span></span>                       | <span data-ttu-id="f9caf-109">installation de l’APPLICATION \_</span><span class="sxs-lookup"><span data-stu-id="f9caf-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="f9caf-110">*Appname* installé</span><span class="sxs-lookup"><span data-stu-id="f9caf-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="f9caf-111">Modification de l’application (ajout/suppression de fonctionnalités)</span><span class="sxs-lookup"><span data-stu-id="f9caf-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="f9caf-112">MODIFIER les \_ paramètres</span><span class="sxs-lookup"><span data-stu-id="f9caf-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="f9caf-113">*Appname* configuré</span><span class="sxs-lookup"><span data-stu-id="f9caf-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="f9caf-114">Suppression de l’application</span><span class="sxs-lookup"><span data-stu-id="f9caf-114">Application removal</span></span>                            | <span data-ttu-id="f9caf-115">désinstallation de l’APPLICATION \_</span><span class="sxs-lookup"><span data-stu-id="f9caf-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="f9caf-116">*Appname* supprimé</span><span class="sxs-lookup"><span data-stu-id="f9caf-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="f9caf-117">Installation du pilote de périphérique</span><span class="sxs-lookup"><span data-stu-id="f9caf-117">Device driver installation</span></span>                     | <span data-ttu-id="f9caf-118">\_installation du pilote de périphérique \_</span><span class="sxs-lookup"><span data-stu-id="f9caf-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="f9caf-119">*Nom_pilote* installé</span><span class="sxs-lookup"><span data-stu-id="f9caf-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="f9caf-120">Les programmes d’installation, tels que Windows Installer et InstallShield, utilisent les conventions suivantes pour le texte de Description :</span><span class="sxs-lookup"><span data-stu-id="f9caf-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="f9caf-121">Le nom du produit suit le verbe ; par exemple, l’installation de *appname*.</span><span class="sxs-lookup"><span data-stu-id="f9caf-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="f9caf-122">Le nom du produit peut être utilisé seul (*appname*) ou le nom du produit et le nom de la société peuvent tous les deux être utilisés (*MyCompany AppName*).</span><span class="sxs-lookup"><span data-stu-id="f9caf-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




