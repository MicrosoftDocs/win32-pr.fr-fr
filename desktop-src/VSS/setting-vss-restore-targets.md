---
description: L’interface IVssComponent permet à un enregistreur d’ajuster précisément la manière dont les fichiers sont restaurés composant par composant.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Définition des cibles de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544795"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="55ce3-103">Définition des cibles de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="55ce3-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="55ce3-104">L’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permet à un enregistreur d’ajuster précisément la manière dont les fichiers sont restaurés composant par composant.</span><span class="sxs-lookup"><span data-stu-id="55ce3-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="55ce3-105">Étant donné qu’il est possible que la configuration du système pendant la restauration soit autre que celle prévue lors de la sauvegarde, le mécanisme de la cible de restauration est fourni.</span><span class="sxs-lookup"><span data-stu-id="55ce3-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="55ce3-106">Elle permet aux rédacteurs d’appeler [**IVssComponent :: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) pour modifier la façon dont les composants qui sont [*explicitement inclus*](vssgloss-e.md) dans le document des composants de sauvegarde sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="55ce3-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="55ce3-107">Cela modifie également le mécanisme de restauration utilisé sur les composants qui sont [*implicitement inclus*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="55ce3-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="55ce3-108">La restauration de fichiers qui a lieu lors d’un redémarrage du système (sous les valeurs d’énumération VSS [**\_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ RME \_ Restore \_ au \_ redémarrage et VSS \_ RME \_ Restore \_ au \_ redémarrage \_ si \_ ne peut pas \_ être remplacé) ne peut pas être affectée par les cibles de restauration, car il n’existe aucun service VSS en cours d’exécution lorsque **MoveFileEx** copie les fichiers à leur emplacement final.</span><span class="sxs-lookup"><span data-stu-id="55ce3-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="55ce3-109">De même, \_ \_ les restaurations personnalisées de VSS RME peuvent être affectées, car chaque restauration personnalisée est spécifique à un writer donné et peut choisir de respecter ou d’ignorer les cibles de restauration.</span><span class="sxs-lookup"><span data-stu-id="55ce3-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="55ce3-110">Les demandeurs et les enregistreurs peuvent utiliser [**IVssComponent :: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) pour vérifier la cible de restauration d’un jeu de composants.</span><span class="sxs-lookup"><span data-stu-id="55ce3-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="55ce3-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) prend en charge les cibles de restauration suivantes, qui peuvent être définies sur un composant défini à l’aide d’un jeu de composants :</span><span class="sxs-lookup"><span data-stu-id="55ce3-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="55ce3-112">\_ \_ version d’origine de VSS RT.</span><span class="sxs-lookup"><span data-stu-id="55ce3-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="55ce3-113">La méthode Restore spécifiée par l’énumération [**VSS \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) est respectée.</span><span class="sxs-lookup"><span data-stu-id="55ce3-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="55ce3-114">alternative à VSS \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="55ce3-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="55ce3-115">Les fichiers sont restaurés à un emplacement déterminé à partir d’un mappage d’emplacement de remplacement existant.</span><span class="sxs-lookup"><span data-stu-id="55ce3-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="55ce3-116">Si un mappage d’emplacement secondaire correspondant à un chemin d’accès dans un sous-composant de jeu de composants existe, restaurez-le dans un autre emplacement, si possible ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="55ce3-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



