---
description: 'Le processus d’installation réussit deux phases : l’acquisition et l’exécution. En cas d’échec de l’installation, une phase de restauration peut se produire.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mécanisme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544732"
---
# <a name="installation-mechanism"></a><span data-ttu-id="3bc77-104">Mécanisme d’installation</span><span class="sxs-lookup"><span data-stu-id="3bc77-104">Installation Mechanism</span></span>

<span data-ttu-id="3bc77-105">Le processus d’installation réussit deux phases : l’acquisition et l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3bc77-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="3bc77-106">En cas d’échec de l’installation, une phase de restauration peut se produire.</span><span class="sxs-lookup"><span data-stu-id="3bc77-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="3bc77-107">Acquisition</span><span class="sxs-lookup"><span data-stu-id="3bc77-107">Acquisition</span></span>

<span data-ttu-id="3bc77-108">Au début de la phase d’acquisition, une application ou un utilisateur demande au programme d’installation d’installer une fonctionnalité ou une application.</span><span class="sxs-lookup"><span data-stu-id="3bc77-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="3bc77-109">Le programme d’installation parcourt ensuite les actions spécifiées dans les tables de séquence de la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="3bc77-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="3bc77-110">Ces actions interrogent la base de données d’installation et génèrent un script qui fournit une procédure pas-à-pas pour effectuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="3bc77-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="3bc77-111">Exécution</span><span class="sxs-lookup"><span data-stu-id="3bc77-111">Execution</span></span>

<span data-ttu-id="3bc77-112">Pendant la phase d’exécution, le programme d’installation transmet les informations à un processus avec des privilèges élevés et exécute le script.</span><span class="sxs-lookup"><span data-stu-id="3bc77-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="3bc77-113">Restauration</span><span class="sxs-lookup"><span data-stu-id="3bc77-113">Rollback</span></span>

<span data-ttu-id="3bc77-114">Si une installation échoue, le programme d’installation restaure l’état d’origine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3bc77-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="3bc77-115">Quand le programme d’installation traite le script d’installation, il génère simultanément un script de restauration.</span><span class="sxs-lookup"><span data-stu-id="3bc77-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="3bc77-116">En plus du script de restauration, le programme d’installation enregistre une copie de chaque fichier qu’il supprime pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="3bc77-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="3bc77-117">Ces fichiers sont conservés dans un répertoire système masqué.</span><span class="sxs-lookup"><span data-stu-id="3bc77-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="3bc77-118">Une fois l’installation terminée, le script de restauration et les fichiers enregistrés sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="3bc77-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="3bc77-119">Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="3bc77-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



