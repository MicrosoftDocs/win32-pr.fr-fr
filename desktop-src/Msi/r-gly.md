---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868cb5b7-d5ab-41c7-a6d4-d7964a8ff6de
title: R (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f5093064838ff390b2fa1fa8cc38335d4c5db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864845"
---
# <a name="r-windows-installer"></a><span data-ttu-id="805f9-103">R (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="805f9-103">R (Windows Installer)</span></span>

<span data-ttu-id="805f9-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="805f9-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="805f9-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**interface utilisateur réduite**</span><span class="sxs-lookup"><span data-stu-id="805f9-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**reduced UI**</span></span>
</dt> <dd>

<span data-ttu-id="805f9-106">Niveau des fonctionnalités de l' [*interface utilisateur interne*](i-gly.md) du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="805f9-106">Level of the installer's [*internal user interface*](i-gly.md) capabilities.</span></span> <span data-ttu-id="805f9-107">Affiche uniquement les boîtes de dialogue non modales créées.</span><span class="sxs-lookup"><span data-stu-id="805f9-107">Displays only authored modeless dialog boxes.</span></span> <span data-ttu-id="805f9-108">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="805f9-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

</dd> <dt>

<span data-ttu-id="805f9-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**installé**</span><span class="sxs-lookup"><span data-stu-id="805f9-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**reinstall**</span></span>
</dt> <dd>

<span data-ttu-id="805f9-110">Réinstallation partielle ou complète d’une application installée.</span><span class="sxs-lookup"><span data-stu-id="805f9-110">Partial or complete reinstallation of an installed application.</span></span> <span data-ttu-id="805f9-111">Cette opération est couramment effectuée pour réparer une application si des fichiers ou des entrées de Registre sont endommagés ou manquants.</span><span class="sxs-lookup"><span data-stu-id="805f9-111">Commonly done to repair an application if any files or registry entries have become corrupted or are missing.</span></span> <span data-ttu-id="805f9-112">Pour plus d’informations, consultez [réinstallation d’une fonctionnalité ou d’une application](reinstalling-a-feature-or-application.md).</span><span class="sxs-lookup"><span data-stu-id="805f9-112">For more information, see [Reinstalling a Feature or Application](reinstalling-a-feature-or-application.md).</span></span>

</dd> <dt>

<span data-ttu-id="805f9-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**résilience**</span><span class="sxs-lookup"><span data-stu-id="805f9-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**resiliency**</span></span>
</dt> <dd>

<span data-ttu-id="805f9-114">Capacité d’application de la récupération normale d’une erreur sans générer de messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="805f9-114">Application capability of graceful recovery from error without generating error messages.</span></span> <span data-ttu-id="805f9-115">Pour plus d’informations, consultez [résilience](resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="805f9-115">For more information, see [Resiliency](resiliency.md).</span></span>

</dd> <dt>

<span data-ttu-id="805f9-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**instruction**</span><span class="sxs-lookup"><span data-stu-id="805f9-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**rollback**</span></span>
</dt> <dd>

<span data-ttu-id="805f9-117">La restauration automatique de l’état d’origine de l’ordinateur en cas d’échec de l’installation.</span><span class="sxs-lookup"><span data-stu-id="805f9-117">Automatic restoration of the original state of the computer should the installation fail.</span></span> <span data-ttu-id="805f9-118">Pour plus d’informations, consultez [restauration de l’installation (Windows Installer)](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="805f9-118">For more information, see [Rollback Installation (Windows Installer)](rollback-installation.md).</span></span>

</dd> </dl>

 

 



