---
description: La communication avec un périphérique réseau à l’aide de l’interface WMI SNMP requiert la configuration des services de l’appareil, du SNMP et de WMI. Les informations contenues dans cette rubrique expliquent comment configurer l’environnement SNMP WMI.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configuration de l’environnement WMI SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320666"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="2ba45-104">Configuration de l’environnement WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="2ba45-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="2ba45-105">La communication avec un périphérique réseau à l’aide de l’interface WMI SNMP requiert la configuration des services de l’appareil, du SNMP et de WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba45-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="2ba45-106">Les informations contenues dans cette rubrique expliquent comment configurer l’environnement SNMP WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba45-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="2ba45-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="2ba45-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="2ba45-108">Installation du fournisseur SNMP</span><span class="sxs-lookup"><span data-stu-id="2ba45-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="2ba45-109">Le service SNMP n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ba45-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="2ba45-110">Vous pouvez activer le service SNMP et le fournisseur SNMP WMI via le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="2ba45-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="2ba45-111">N’oubliez pas que le service SNMP doit être activé et en cours d’exécution pour que le fournisseur SNMP SNMP fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2ba45-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="2ba45-112">À compter de Windows Vista, utilisez la procédure suivante pour installer le fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="2ba45-113">**Pour installer le fournisseur SNMP**</span><span class="sxs-lookup"><span data-stu-id="2ba45-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="2ba45-114">Dans le **panneau de configuration**, sélectionnez **programmes**.</span><span class="sxs-lookup"><span data-stu-id="2ba45-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="2ba45-115">Sous **programmes et fonctionnalités**, sélectionnez **activer ou désactiver des fonctionnalités Windows**.</span><span class="sxs-lookup"><span data-stu-id="2ba45-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="2ba45-116">Dans la liste des fonctionnalités Windows, faites défiler jusqu’à **fonctionnalité SNMP** , puis développez la liste pour voir le **fournisseur SNMP SNMP**.</span><span class="sxs-lookup"><span data-stu-id="2ba45-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="2ba45-117">Activez la case à cocher du **fournisseur SNMP WMI**.</span><span class="sxs-lookup"><span data-stu-id="2ba45-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="2ba45-118">La case à cocher de la **fonctionnalité SNMP** est automatiquement activée, car le fournisseur requiert SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="2ba45-119">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ba45-119">Click **OK**.</span></span>
6.  <span data-ttu-id="2ba45-120">À partir d’une invite de commandes ou du menu **Démarrer** , exécutez services. msc et vérifiez que le service SNMP est démarré.</span><span class="sxs-lookup"><span data-stu-id="2ba45-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="2ba45-121">Création d’un espace de noms SNMP</span><span class="sxs-lookup"><span data-stu-id="2ba45-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="2ba45-122">Un espace de noms SNMP définit une vue d’un périphérique réseau.</span><span class="sxs-lookup"><span data-stu-id="2ba45-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="2ba45-123">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="2ba45-124">La procédure suivante décrit comment créer un [*espace de noms*](gloss-n.md)WMI SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="2ba45-125">**Pour créer un espace de noms SNMP**</span><span class="sxs-lookup"><span data-stu-id="2ba45-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="2ba45-126">Créez une instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) en compilant un fichier [*format MOF*](gloss-m.md) . mof ou en utilisant l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="2ba45-127">Pour plus d’informations, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="2ba45-128">Associez les [*qualificateurs*](gloss-q.md) du fournisseur SNMP à la définition de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2ba45-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="2ba45-129">Les qualificateurs du fournisseur SNMP contiennent des informations de contexte spécifiques à l’implémentation et des propriétés de transport qui définissent la façon dont le fournisseur SNMP accède à un périphérique SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="2ba45-130">Pour plus d’informations, consultez [**qualificateurs spécifiques au fournisseur SNMP**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="2ba45-131">Utilisez l’outil en ligne de commande [mofcomp](mofcomp.md) pour charger le code MOF dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba45-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="2ba45-132">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="2ba45-133">L’exemple de code MOF suivant définit l' \\ espace de noms SNMP avec un sous-ensemble des qualificateurs qui peuvent être associés à un espace de noms SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="2ba45-134">Insertion de données MIB SNMP dans WMI</span><span class="sxs-lookup"><span data-stu-id="2ba45-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="2ba45-135">En tant que fournisseur, le fournisseur SNMP agit comme un pont entre les données SNMP et les classes WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba45-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="2ba45-136">Par conséquent, vous devez avoir des classes dans WMI qui représentent différents aspects d’un périphérique SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="2ba45-137">Pour ce faire, vous devez utiliser le compilateur de module d’informations SNMP ([Smi2smir](smi2smir.md)) pour compiler les informations de gestion SNMP du format SNMP vers les définitions de schéma CIM équivalentes.</span><span class="sxs-lookup"><span data-stu-id="2ba45-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="2ba45-138">Vous pouvez ensuite diriger la sortie du compilateur d’informations dans une base de données de schéma SNMP appelée « référentiel d’informations de module SNMP (stockage SMIR) » ou à plusieurs types de fichiers MOF.</span><span class="sxs-lookup"><span data-stu-id="2ba45-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="2ba45-139">Le compilateur s’exécute en mode de ligne de commande, en utilisant un fichier MIB comme entrée.</span><span class="sxs-lookup"><span data-stu-id="2ba45-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="2ba45-140">La commande suivante charge le fichier MIB spécifié dans stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="2ba45-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="2ba45-141">\**Smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="2ba45-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="2ba45-142">Configuration des communautés SNMP</span><span class="sxs-lookup"><span data-stu-id="2ba45-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="2ba45-143">En guise de mesure de sécurité, la communauté SNMP « public » n’est pas créée par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ba45-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="2ba45-144">Vous pouvez créer la communauté comme décrit dans [paramètres du registre des communautés](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="2ba45-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="2ba45-145">Si vous n’avez pas de communauté, créez la communauté « public » pour accéder au fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="2ba45-146">Génération de fichiers MOF à partir de fichiers MIB</span><span class="sxs-lookup"><span data-stu-id="2ba45-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="2ba45-147">Les commandes suivantes sont un exemple de génération de fichiers MOF à partir des fichiers MIB qui sont installés lors de l’installation du fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="2ba45-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="2ba45-148">**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="2ba45-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="2ba45-149">**Smi2smir/g** *... \\ . \\ hostmib. MIB* **>** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="2ba45-150">**Smi2smir/g** *... \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="2ba45-151">**Smi2smir/g** *... \\ . \\ nipx. MIB* **>** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="2ba45-152">**Smi2smir/g** *... \\ . \\ MIB II \_ .* mib MIB II **>** *\_ . mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="2ba45-153">**Smi2smir/g** *... \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="2ba45-154">**Smi2smir/g** *... \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="2ba45-155">**Smi2smir/g** *... \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="2ba45-156">**Smi2smir/g** *... \\ . \\ wfospf. MIB* **>** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="2ba45-157">**Smi2smir/g** *... \\ . \\ DHCP. MIB... \\ . \\ msft. MIB* **>** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="2ba45-158">**Smi2smir/g** *... \\ . \\ WINS. MIB... \\ . \\ msft. MIB* **>** *, WINS. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="2ba45-159">**Smi2smir/g** *... \\ . \\ mipx. MIB... \\ . \\ msft. MIB* **>** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="2ba45-160">**Smi2smir/g** *... \\ . \\ mripsap. MIB... \\ . \\ msft. MIB* **>** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="2ba45-161">**Smi2smir/g** *... \\ . \\ msipbtp. MIB... \\ . \\ msft. MIB* **>** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="2ba45-162">**Smi2smir/g** *... \\ . \\ msiprip2. MIB... \\ . \\ msft. MIB* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="2ba45-163">Ajout de fichiers MOF SNMP à l’espace de stockage WMI</span><span class="sxs-lookup"><span data-stu-id="2ba45-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="2ba45-164">Les commandes suivantes sont un exemple de la façon d’ajouter les fichiers MOF générés à partir des fichiers MIB à l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba45-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="2ba45-165">Si vous souhaitez ajouter les fichiers MOF à la liste des fichiers à restaurer automatiquement dans une récupération de [*référentiel WMI*](gloss-w.md) , ajoutez l’indicateur **-AutoRecover** à la fin de chaque commande.</span><span class="sxs-lookup"><span data-stu-id="2ba45-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="2ba45-166">Pour plus d’informations sur l’outil de ligne de commande WMI Mofcomp.exe, consultez [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="2ba45-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="2ba45-167">**mofcomp** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="2ba45-168">**mofcomp** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="2ba45-169">**mofcomp** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="2ba45-170">**mofcomp** *MIB \_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="2ba45-171">**mofcomp** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="2ba45-172">**mofcomp** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="2ba45-173">**mofcomp** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="2ba45-174">**mofcomp** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="2ba45-175">**mofcomp** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="2ba45-176">**mofcomp** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="2ba45-177">**mofcomp** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="2ba45-178">**mofcomp** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="2ba45-179">**mofcomp** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="2ba45-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba45-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ba45-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba45-181">Accès aux appareils SNMP</span><span class="sxs-lookup"><span data-stu-id="2ba45-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
