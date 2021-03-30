---
description: Montre comment utiliser les \_ API NotifyIcon Shell et Shell \_ NotifyIconGetRect pour afficher une icône de notification.
title: NotificationIcon, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973290"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="e2c9b-103">NotificationIcon, exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-103">NotificationIcon Sample</span></span>

<span data-ttu-id="e2c9b-104">Montre comment utiliser les API [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) et [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) pour afficher une icône de notification.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="e2c9b-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e2c9b-106">Description</span><span class="sxs-lookup"><span data-stu-id="e2c9b-106">Description</span></span>](#description)
-   [<span data-ttu-id="e2c9b-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2c9b-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e2c9b-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e2c9b-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e2c9b-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="e2c9b-111">Description</span><span class="sxs-lookup"><span data-stu-id="e2c9b-111">Description</span></span>

<span data-ttu-id="e2c9b-112">Outre l’utilisation de l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) et de l’interpréteur de commandes shell [**\_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) pour afficher une icône de notification, cet exemple montre également comment afficher une fenêtre complète, un menu contextuel et une notification de bulles.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="e2c9b-113">[**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) est disponible uniquement sur Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2c9b-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e2c9b-114">Requirements</span></span>



| <span data-ttu-id="e2c9b-115">Produit</span><span class="sxs-lookup"><span data-stu-id="e2c9b-115">Product</span></span>                                | <span data-ttu-id="e2c9b-116">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="e2c9b-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e2c9b-117">Windows</span><span class="sxs-lookup"><span data-stu-id="e2c9b-117">Windows</span></span>                                | <span data-ttu-id="e2c9b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2c9b-118">Windows 7</span></span>               |
| <span data-ttu-id="e2c9b-119">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="e2c9b-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e2c9b-120">7.0</span><span class="sxs-lookup"><span data-stu-id="e2c9b-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e2c9b-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-121">Downloading the Sample</span></span>

| <span data-ttu-id="e2c9b-122">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e2c9b-122">Location</span></span>      | <span data-ttu-id="e2c9b-123">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="e2c9b-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c9b-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="e2c9b-124">GitHub</span></span>  | [<span data-ttu-id="e2c9b-125">Exemple NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="e2c9b-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="e2c9b-126">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-126">Building the Sample</span></span>

<span data-ttu-id="e2c9b-127">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="e2c9b-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="e2c9b-128">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="e2c9b-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="e2c9b-129">Entrez `msbuild NotificationIcon.sln`.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="e2c9b-130">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="e2c9b-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="e2c9b-131">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="e2c9b-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="e2c9b-132">Double-cliquez sur l’icône du fichier NotificationIcon. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="e2c9b-133">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e2c9b-134">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e2c9b-134">Running the Sample</span></span>

1.  <span data-ttu-id="e2c9b-135">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="e2c9b-136">Sur la ligne de commande, entrez `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="e2c9b-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="e2c9b-137">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de NotificationIcon.exe.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="e2c9b-138">Les icônes de notification spécifiées avec un GUID sont protégées contre l’usurpation en validant qu’une seule application les enregistre.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="e2c9b-139">Cette inscription est effectuée la première fois que vous appelez l’interface \_ NotifyIcon de l’interpréteur de commandes (NIM \_ Add,...) et le nom du chemin d’accès complet de l’application appelante est stocké.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="e2c9b-140">Si, par la suite, vous déplacez votre fichier binaire vers un emplacement différent, le système n’autorise pas l’ajout de l’icône.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="e2c9b-141">Pour plus d’informations, consultez [**\_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes.</span><span class="sxs-lookup"><span data-stu-id="e2c9b-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



