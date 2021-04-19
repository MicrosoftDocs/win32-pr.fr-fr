---
description: Le contrôle WMI est un composant logiciel enfichable MMC situé dans le panneau de configuration et utilisé pour définir manuellement la sécurité de l’espace de noms WMI sur un ordinateur local. Vous pouvez également définir l’espace de noms par défaut pour les scripts.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Définition de la sécurité de l’espace de noms avec le contrôle WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524693"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="b6215-104">Définition de la sécurité de l’espace de noms avec le contrôle WMI</span><span class="sxs-lookup"><span data-stu-id="b6215-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="b6215-105">Le contrôle WMI est un composant logiciel enfichable MMC situé dans le **panneau** de configuration et utilisé pour définir manuellement la sécurité de l’espace de noms WMI sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b6215-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="b6215-106">Vous pouvez également définir l’espace de noms par défaut pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="b6215-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="b6215-107">La procédure suivante décrit comment localiser le contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="b6215-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="b6215-108">**Pour localiser le contrôle WMI**</span><span class="sxs-lookup"><span data-stu-id="b6215-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="b6215-109">Dans le **panneau de configuration**, double-cliquez sur **Outils d’administration**.</span><span class="sxs-lookup"><span data-stu-id="b6215-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="b6215-110">Dans la fenêtre **Outils d’administration**, double-cliquez sur **Gestion de l’ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="b6215-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="b6215-111">Dans la fenêtre Gestion de l' **ordinateur** , développez l’arborescence **services et applications** , puis double-cliquez sur le **contrôle WMI**.</span><span class="sxs-lookup"><span data-stu-id="b6215-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="b6215-112">Cliquez avec le bouton droit sur l’icône de **contrôle WMI** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b6215-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="b6215-113">La procédure suivante décrit comment utiliser le contrôle WMI pour configurer la sécurité d’un espace de noms en tant que modèle, puis obtenir par programmation les paramètres de sécurité pour définir la sécurité pour d’autres espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="b6215-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="b6215-114">**Pour définir la sécurité de l’espace de noms avec le contrôle WMI**</span><span class="sxs-lookup"><span data-stu-id="b6215-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="b6215-115">Créez un espace de noms à l’aide du code format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b6215-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="b6215-116">Exécutez le contrôle WMI pour définir la sécurité sur le nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b6215-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="b6215-117">Dans le menu **Démarrer** , cliquez sur **exécuter** , tapez **wmimgmt. msc** ou recherchez [le contrôle WMI](#).</span><span class="sxs-lookup"><span data-stu-id="b6215-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="b6215-118">Dans le volet de **contrôle WMI** , cliquez avec le bouton droit sur **contrôle WMI**, choisissez **Propriétés**, puis sélectionnez l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="b6215-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="b6215-119">Accédez au nouvel espace de noms, cliquez sur **sécurité**, puis configurez les groupes et les autorisations pour l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b6215-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="b6215-120">Vous pouvez également utiliser Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) pour définir la sécurité de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b6215-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="b6215-121">Pour plus d’informations, consultez [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="b6215-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="b6215-122">Définition de l’espace de noms par défaut pour les scripts</span><span class="sxs-lookup"><span data-stu-id="b6215-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="b6215-123">Si un script ne se connecte pas explicitement à un espace de noms lors de la connexion à WMI, WMI utilise l’espace de noms par défaut spécifié dans ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="b6215-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="b6215-124">La valeur par défaut se trouve également dans l’entrée du Registre comme suit :</span><span class="sxs-lookup"><span data-stu-id="b6215-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="b6215-125">Étant donné que l’espace de noms par défaut est facile à modifier, soit avec ce contrôle, soit par programmation en appelant des méthodes de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), spécifiez l’espace de noms lors de la connexion à WMI par le biais du [moniker](constructing-a-moniker-string.md) ou des appels à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="b6215-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="b6215-126">Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md) .</span><span class="sxs-lookup"><span data-stu-id="b6215-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="b6215-127">**Pour définir l’espace de noms par défaut pour les scripts**</span><span class="sxs-lookup"><span data-stu-id="b6215-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="b6215-128">Dans la fenêtre **Propriétés du contrôle WMI** , choisissez l’onglet **avancé** .</span><span class="sxs-lookup"><span data-stu-id="b6215-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="b6215-129">Cliquez sur le bouton **modifier** et sélectionnez l’espace de noms à utiliser comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6215-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6215-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6215-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6215-131">Définition des descripteurs de sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="b6215-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
