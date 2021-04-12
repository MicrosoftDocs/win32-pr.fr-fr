---
description: '\\Bureau du panneau de configuration HKCU \\ .'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393159"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="317b4-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="317b4-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="317b4-104">**\\Bureau du panneau de configuration HKCU \\**</span><span class="sxs-lookup"><span data-stu-id="317b4-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="317b4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="317b4-105">Data type</span></span> | <span data-ttu-id="317b4-106">Plage</span><span class="sxs-lookup"><span data-stu-id="317b4-106">Range</span></span>       | <span data-ttu-id="317b4-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="317b4-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="317b4-108">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="317b4-108">REG\_SZ</span></span>   | <span data-ttu-id="317b4-109">*Nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="317b4-109">*File name*</span></span> | <span data-ttu-id="317b4-110">(aucune)</span><span class="sxs-lookup"><span data-stu-id="317b4-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="317b4-111">Description</span><span class="sxs-lookup"><span data-stu-id="317b4-111">Description</span></span>

<span data-ttu-id="317b4-112">Spécifie le nom du fichier exécutable de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="317b4-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="317b4-113">Modifier la méthode</span><span class="sxs-lookup"><span data-stu-id="317b4-113">Change Method</span></span>

<span data-ttu-id="317b4-114">Pour modifier la valeur de cette entrée, dans Panneau de configuration, double-cliquez sur **affichage**, cliquez sur l’onglet **écran de veille** , puis sélectionnez un écran de veille dans la liste **écran de veille** .</span><span class="sxs-lookup"><span data-stu-id="317b4-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="317b4-115">Vous pouvez également modifier cette entrée à l’aide de la fonction d’interface de programmation d’applications (API) **InstallScreenSaver**, qui est exportée par Desk.cpl.</span><span class="sxs-lookup"><span data-stu-id="317b4-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="317b4-116">Vous pouvez accéder à cette fonction à l’aide de la ligne de commande **rundll32.exe desk.cpl,** *fichier* InstallScreenSaver, où *fichier* est le nom d’un fichier exécutable de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="317b4-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="317b4-117">Méthode d’activation</span><span class="sxs-lookup"><span data-stu-id="317b4-117">Activation Method</span></span>

<span data-ttu-id="317b4-118">Les modifications apportées à cette entrée deviennent effectives lors du prochain démarrage de l’économiseur d’écran par le système.</span><span class="sxs-lookup"><span data-stu-id="317b4-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="317b4-119">Les modifications apportées à cette entrée pendant l’exécution d’un économiseur d’écran n’ont aucun effet sur l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="317b4-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="317b4-120">Notes</span><span class="sxs-lookup"><span data-stu-id="317b4-120">Notes</span></span>

-   <span data-ttu-id="317b4-121">Les systèmes d’exploitation Windows ajoutent cette entrée au registre lorsque vous utilisez l’option **Afficher** du panneau de configuration pour sélectionner un économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="317b4-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="317b4-122">Si vous désactivez tous les économiseurs d’écran en choisissant **(aucun)** dans la liste écran de veille, le système d’exploitation supprime cette entrée du Registre et appelle la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec *uiaction* égal à SPI \_ SETSCREENSAVEACTIVE et *uiParam* égal à **false**.</span><span class="sxs-lookup"><span data-stu-id="317b4-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="317b4-123">Cette entrée peut être remplacée par un paramètre de stratégie de groupe sur les systèmes qui prennent en charge stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="317b4-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="317b4-124">Lorsque le paramètre stratégie de groupe du nom de l’exécutable de l' **économiseur d’écran** est activé, le système ignore cette entrée.</span><span class="sxs-lookup"><span data-stu-id="317b4-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="317b4-125">La configuration de ce paramètre de stratégie est stockée dans l’entrée **SCRNSAVE.EXE** , qui se trouve dans la sous-clé **stratégies** .</span><span class="sxs-lookup"><span data-stu-id="317b4-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
