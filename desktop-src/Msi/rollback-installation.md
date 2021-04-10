---
description: Lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Restauration de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114550"
---
# <a name="rollback-installation"></a><span data-ttu-id="136c2-103">Restauration de l’installation</span><span class="sxs-lookup"><span data-stu-id="136c2-103">Rollback Installation</span></span>

<span data-ttu-id="136c2-104">Lorsque le Windows Installer traite le script d’installation pour l’installation d’un produit ou d’une application, il génère simultanément un script de restauration et enregistre une copie de chaque fichier supprimé au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="136c2-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="136c2-105">Ces fichiers sont conservés dans un répertoire système masqué et sont automatiquement supprimés une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="136c2-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="136c2-106">Toutefois, si l’installation échoue, le programme d’installation effectue automatiquement une restauration qui rétablit l’état d’origine du système.</span><span class="sxs-lookup"><span data-stu-id="136c2-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="136c2-107">La restauration automatique d’une installation ayant échoué est le comportement par défaut du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="136c2-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="136c2-108">Pour désactiver la restauration au cours d’une installation, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="136c2-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="136c2-109">**Propriété DISABLEROLLBACK**</span><span class="sxs-lookup"><span data-stu-id="136c2-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="136c2-110">**Propriété PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="136c2-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="136c2-111">Action DisableRollback</span><span class="sxs-lookup"><span data-stu-id="136c2-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="136c2-112">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="136c2-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="136c2-113">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="136c2-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="136c2-114">Chaque fois que la restauration est désactivée, le programme d’installation définit la propriété [**RollbackDisabled**](rollbackdisabled.md) .</span><span class="sxs-lookup"><span data-stu-id="136c2-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="136c2-115">Si une installation utilise des [actions personnalisées](custom-actions.md), une création supplémentaire du package d’installation est nécessaire pour utiliser la fonctionnalité de restauration.</span><span class="sxs-lookup"><span data-stu-id="136c2-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="136c2-116">Pour plus d’informations, consultez [restaurer des actions personnalisées](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="136c2-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



