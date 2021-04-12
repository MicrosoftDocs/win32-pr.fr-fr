---
title: Valeurs de retour de SYSMON
description: La liste suivante répertorie les valeurs renvoyées par le moniteur système qui sont définies dans Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382371"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="32e49-103">Valeurs de retour de SYSMON</span><span class="sxs-lookup"><span data-stu-id="32e49-103">SYSMON Return Values</span></span>

<span data-ttu-id="32e49-104">La liste suivante répertorie les valeurs renvoyées par le moniteur système qui sont définies dans Smonmsg. h.</span><span class="sxs-lookup"><span data-stu-id="32e49-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="32e49-105">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32e49-105">Return value</span></span>                                       | <span data-ttu-id="32e49-106">Description</span><span class="sxs-lookup"><span data-stu-id="32e49-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e49-107">SMON \_ état \_ DUPL \_ chemin du compteur \_ (0xC0001388)</span><span class="sxs-lookup"><span data-stu-id="32e49-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="32e49-108">La collection de compteurs contient déjà le compteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="32e49-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="32e49-109">\_État smon \_ aucun \_ \_ objet SYSMON (0xC0001389)</span><span class="sxs-lookup"><span data-stu-id="32e49-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="32e49-110">Les paramètres ne contiennent pas d’objets HTML du moniteur système complets.</span><span class="sxs-lookup"><span data-stu-id="32e49-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="32e49-111">\_Exemples d’États smon \_ insuffisants \_ \_ (0xC000138A)</span><span class="sxs-lookup"><span data-stu-id="32e49-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="32e49-112">Le fichier journal spécifié contient moins de deux échantillons de données.</span><span class="sxs-lookup"><span data-stu-id="32e49-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="32e49-113">\_ \_ Limite de la taille du fichier journal d’État smon \_ \_ \_ (0xC000138B)</span><span class="sxs-lookup"><span data-stu-id="32e49-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="32e49-114">Le fichier journal spécifié dépasse les limites de taille du contrôle Moniteur système.</span><span class="sxs-lookup"><span data-stu-id="32e49-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="32e49-115">Si un fichier journal est actuellement sélectionné, sélectionnez activité actuelle comme source de données afin de décharger le fichier journal actuel, puis resélectionnez le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="32e49-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="32e49-116">\_ \_ Source de données du fichier journal d’État smon \_ \_ \_ (0xC000138C)</span><span class="sxs-lookup"><span data-stu-id="32e49-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="32e49-117">Pour ajouter un nouveau fichier journal à la source de données, le type de source de données doit être changé en un type autre que sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="32e49-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="32e49-118">SMON \_ état \_ DUPL \_ \_ \_ chemin d’accès du fichier journal (0xC000138D)</span><span class="sxs-lookup"><span data-stu-id="32e49-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="32e49-119">La collection de fichiers journaux contient déjà le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="32e49-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="32e49-120">Pour obtenir une description des valeurs de retour supplémentaires retournées par le moniteur système, consultez Codes d' [erreur système](/windows/desktop/Debug/system-error-codes) et [codes d’erreur du programme d’assistance des données de performances](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="32e49-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 