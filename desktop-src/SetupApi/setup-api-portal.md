---
description: Installe des pilotes de périphérique à partir de programmes avec un script de configuration et des fichiers INF. Écrivez un programme d’installation pour la configuration des appareils et l’installation du pilote. Cette API n’est plus recommandée dans le cadre de l’installation d’applications logicielles.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519971"
---
# <a name="setup-api"></a><span data-ttu-id="a3dff-105">API d’installation</span><span class="sxs-lookup"><span data-stu-id="a3dff-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="a3dff-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="a3dff-106">Purpose</span></span>

<span data-ttu-id="a3dff-107">L’API d’installation fournit un ensemble de fonctions que l’application de configuration appelle pour effectuer des opérations d’installation.</span><span class="sxs-lookup"><span data-stu-id="a3dff-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a3dff-108">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="a3dff-108">Where applicable</span></span>

<span data-ttu-id="a3dff-109">Ces fonctions de configuration sont disponibles pour le développement d’une application d’installation.</span><span class="sxs-lookup"><span data-stu-id="a3dff-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="a3dff-110">L’API d’installation ne doit plus être utilisée pour installer des applications.</span><span class="sxs-lookup"><span data-stu-id="a3dff-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="a3dff-111">Utilisez plutôt le [Windows Installer](/windows/desktop/Msi/windows-installer-portal)pour développer des programmes d’installation d’application.</span><span class="sxs-lookup"><span data-stu-id="a3dff-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="a3dff-112">L’API d’installation continue à être utilisée pour installer les pilotes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a3dff-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="a3dff-113">L’API d’installation est destinée au développement d’applications de style bureau.</span><span class="sxs-lookup"><span data-stu-id="a3dff-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a3dff-114">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a3dff-114">Developer audience</span></span>

<span data-ttu-id="a3dff-115">Un développeur peut utiliser l’API d’installation si son application d’installation requiert les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3dff-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="a3dff-116">Mise en file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a3dff-116">Queuing of files.</span></span>
-   <span data-ttu-id="a3dff-117">Installation des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a3dff-117">Installation of files.</span></span>
-   <span data-ttu-id="a3dff-118">Gestion des erreurs d’installation et demande de support.</span><span class="sxs-lookup"><span data-stu-id="a3dff-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="a3dff-119">Mise à jour des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="a3dff-119">Updating registry entries.</span></span>
-   <span data-ttu-id="a3dff-120">Journalisation des fichiers au fur et à mesure de leur installation.</span><span class="sxs-lookup"><span data-stu-id="a3dff-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="a3dff-121">Stockage des chemins sources les plus récemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="a3dff-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a3dff-122">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a3dff-122">Run-time requirements</span></span>

<span data-ttu-id="a3dff-123">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.</span><span class="sxs-lookup"><span data-stu-id="a3dff-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3dff-124">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a3dff-124">In this section</span></span>



| <span data-ttu-id="a3dff-125">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a3dff-125">Topic</span></span>                                 | <span data-ttu-id="a3dff-126">Description</span><span class="sxs-lookup"><span data-stu-id="a3dff-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3dff-127">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="a3dff-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="a3dff-128">Informations générales sur l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="a3dff-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="a3dff-129">Référence</span><span class="sxs-lookup"><span data-stu-id="a3dff-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="a3dff-130">Documentation des types de données, des structures, des fonctions et des notifications de l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="a3dff-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

