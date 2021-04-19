---
description: Windows Management Instrumentation (WMI) dispose d’une nouvelle clé de Registre pour activer ou désactiver la fonctionnalité de référentiel de restauration.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Clé de Registre pour la configuration du référentiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524132"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="2fa86-103">Clé de Registre pour la configuration du référentiel</span><span class="sxs-lookup"><span data-stu-id="2fa86-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="2fa86-104">Windows Management Instrumentation (WMI) dispose d’une nouvelle clé de Registre pour activer ou désactiver la fonctionnalité de référentiel de restauration.</span><span class="sxs-lookup"><span data-stu-id="2fa86-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="2fa86-105">Pour plus d’informations sur la restauration de l’espace de stockage WMI, consultez [sauvegarder ou restaurer l’espace de stockage WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="2fa86-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="2fa86-106">Dans Windows 7, le comportement par défaut consiste à restaurer automatiquement un référentiel à partir d’une version sauvegardée en cas de détection d’un dépôt.</span><span class="sxs-lookup"><span data-stu-id="2fa86-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="2fa86-107">WMI fournit la valeur de Registre **AutoRestoreEnabled** pour désactiver cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2fa86-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="2fa86-108">Les clés de Registre pour WMI se trouvent dans le registre de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="2fa86-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="2fa86-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span><span class="sxs-lookup"><span data-stu-id="2fa86-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="2fa86-110">Permet à l’utilisateur de déterminer s’il faut ou non utiliser la fonctionnalité de référentiel autorestauration.</span><span class="sxs-lookup"><span data-stu-id="2fa86-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="2fa86-111">Par défaut, cette clé a la valeur 1 et la fonctionnalité de référentiel de la restauration est activée.</span><span class="sxs-lookup"><span data-stu-id="2fa86-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="2fa86-112">Les paramètres suivants sont possibles :</span><span class="sxs-lookup"><span data-stu-id="2fa86-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="2fa86-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="2fa86-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="2fa86-114">Désactivé</span><span class="sxs-lookup"><span data-stu-id="2fa86-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="2fa86-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="2fa86-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="2fa86-116">activé</span><span class="sxs-lookup"><span data-stu-id="2fa86-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="2fa86-117">La valeur de Registre **AutoRestoreEnabled** peut être modifiée à l’aide de la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="2fa86-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="2fa86-118">Pour plus d’informations, consultez [console de gestion des stratégies de groupe](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="2fa86-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="2fa86-119">Cette procédure fournit des détails sur l’activation ou la désactivation de la fonctionnalité de référentiel de restauration autorestauration :</span><span class="sxs-lookup"><span data-stu-id="2fa86-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="2fa86-120">**Pour modifier la valeur par défaut de la clé **AutoRestoreEnabled** à l’aide de stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="2fa86-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="2fa86-121">Ouvrez la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="2fa86-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="2fa86-122">Créez un objet stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="2fa86-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="2fa86-123">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2fa86-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="2fa86-124">Accédez à Préférences/Paramètres Windows/registre.</span><span class="sxs-lookup"><span data-stu-id="2fa86-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="2fa86-125">Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**.</span><span class="sxs-lookup"><span data-stu-id="2fa86-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="2fa86-126">Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.</span><span class="sxs-lookup"><span data-stu-id="2fa86-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="2fa86-127">Sélectionnez la commande **mettre à jour** .</span><span class="sxs-lookup"><span data-stu-id="2fa86-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="2fa86-128">Sélectionnez le chemin d’accès de clé de Registre suivant : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="2fa86-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="2fa86-129">Dans le champ **nom** , entrez **AutoRestoreEnabled**.</span><span class="sxs-lookup"><span data-stu-id="2fa86-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="2fa86-130">Dans le champ **données** , entrez 0 pour désactiver ou 1 pour activer la fonctionnalité de référentiel de restauration.</span><span class="sxs-lookup"><span data-stu-id="2fa86-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="2fa86-131">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="2fa86-131">Click OK.</span></span>

 

 
