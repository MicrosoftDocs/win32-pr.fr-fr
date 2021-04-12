---
title: Configuration de la restauration du système
description: La restauration du système utilise Windows Management Instrumentation (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités. Il expose deux classes, SystemRestore et SystemRestoreConfig, dans l' \\ espace de noms racine par défaut.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382195"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="b0c19-104">Configuration de la restauration du système</span><span class="sxs-lookup"><span data-stu-id="b0c19-104">Configuring System Restore</span></span>

<span data-ttu-id="b0c19-105">La restauration du système utilise [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) pour fournir un moyen scriptable de configurer et d’utiliser ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b0c19-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="b0c19-106">Il expose deux classes, [**SystemRestore**](systemrestore.md) et [**SystemRestoreConfig**](systemrestoreconfig.md), dans l' \\ espace de noms racine par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0c19-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="b0c19-107">La classe [**SystemRestore**](systemrestore.md) fournit des méthodes pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0c19-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="b0c19-108">Désactivation et activation de l’analyse</span><span class="sxs-lookup"><span data-stu-id="b0c19-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="b0c19-109">Liste des points de restauration disponibles</span><span class="sxs-lookup"><span data-stu-id="b0c19-109">Listing available restore points</span></span>
-   <span data-ttu-id="b0c19-110">Lancement d’une restauration sur le système local</span><span class="sxs-lookup"><span data-stu-id="b0c19-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="b0c19-111">Récupération de l’état de la dernière restauration du système</span><span class="sxs-lookup"><span data-stu-id="b0c19-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="b0c19-112">La classe [**SystemRestoreConfig**](systemrestoreconfig.md) fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiés et la quantité d’espace disque consommée par la restauration du système sur chaque lecteur.</span><span class="sxs-lookup"><span data-stu-id="b0c19-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="b0c19-113">Vous pouvez accéder aux deux classes à distance à l’aide des techniques WMI standard.</span><span class="sxs-lookup"><span data-stu-id="b0c19-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="b0c19-114">Pour obtenir une description complète de WMI, consultez [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="b0c19-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 