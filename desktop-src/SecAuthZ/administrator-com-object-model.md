---
description: Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de modèle d’objet de composant avec élévation de privilèges.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modèle d’objet COM administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867225"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="1480d-103">Modèle d’objet COM administrateur</span><span class="sxs-lookup"><span data-stu-id="1480d-103">Administrator COM Object Model</span></span>

<span data-ttu-id="1480d-104">Dans le modèle objet COM de l’administrateur, une application qui s’exécute en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de [modèle d’objet de composant](/windows/desktop/com/component-object-model--com--portal) avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="1480d-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="1480d-105">Pour plus d’informations sur la création d’un objet COM élevé, consultez [le moniker d’élévation com](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="1480d-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="1480d-106">L’un des inconvénients de l’utilisation du modèle d’objet COM administrateur est que l’utilisateur est invité à chaque fois qu’une opération privilégiée est effectuée.</span><span class="sxs-lookup"><span data-stu-id="1480d-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="1480d-107">Toute interface utilisateur qui peut contrôler l’objet COM doit être présentée par l’objet COM lui-même.</span><span class="sxs-lookup"><span data-stu-id="1480d-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="1480d-108">Dans le cas contraire, un processus non privilégié peut entraîner l’exécution d’opérations privilégiées par l’objet COM élevé, sans que l’utilisateur soit invité.</span><span class="sxs-lookup"><span data-stu-id="1480d-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1480d-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1480d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1480d-110">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="1480d-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="1480d-111">Modèle de Broker administrateur</span><span class="sxs-lookup"><span data-stu-id="1480d-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="1480d-112">Modèle de tâche avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="1480d-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="1480d-113">Modèle de service du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1480d-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
