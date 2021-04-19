---
description: Découvrez comment utiliser des appareils NVMe à haut débit à partir de votre application Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Utilisation des lecteurs NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521474"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="da9fa-103">Utilisation des lecteurs NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-103">Working with NVMe drives</span></span>

<span data-ttu-id="da9fa-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="da9fa-104">**Applies to:**</span></span>

-   <span data-ttu-id="da9fa-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="da9fa-105">Windows 10</span></span>
-   <span data-ttu-id="da9fa-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="da9fa-106">Windows Server 2016</span></span>

<span data-ttu-id="da9fa-107">Découvrez comment utiliser des appareils NVMe à haut débit à partir de votre application Windows.</span><span class="sxs-lookup"><span data-stu-id="da9fa-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="da9fa-108">L’accès aux appareils est activé via **StorNVMe.sys**, le pilote intégré introduit pour la première fois dans Windows Server 2012 R2 et Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="da9fa-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="da9fa-109">Elle est également disponible pour les appareils Windows 7 via un correctif logiciel de base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="da9fa-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="da9fa-110">Dans Windows 10, plusieurs nouvelles fonctionnalités ont été introduites, notamment un mécanisme direct pour les commandes NVMe spécifiques au fournisseur et les mises à jour des IOCTL existants.</span><span class="sxs-lookup"><span data-stu-id="da9fa-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="da9fa-111">Cette rubrique fournit une vue d’ensemble des API d’utilisation générale que vous pouvez utiliser pour accéder aux lecteurs NVMe dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="da9fa-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="da9fa-112">Elle décrit également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="da9fa-112">It also describes:</span></span>

-   <span data-ttu-id="da9fa-113">Envoi d’une commande NVMe spécifique à un fournisseur avec [transfert direct](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="da9fa-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="da9fa-114">Comment [Envoyer une commande d’identification, d’obtention de fonctionnalités ou d’obtention de pages de journal](#protocol-specific-queries) au lecteur NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="da9fa-115">Obtention d' [informations de température](#temperature-queries) à partir d’un lecteur NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="da9fa-116">Comment exécuter des commandes de modification de comportement, telles que la [définition de seuils de température](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="da9fa-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="da9fa-117">API pour l’utilisation des lecteurs NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="da9fa-118">Vous pouvez utiliser les API d’utilisation générale suivantes pour accéder aux lecteurs NVMe dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="da9fa-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="da9fa-119">Ces API se trouvent dans **winioctl. h** pour les applications en mode utilisateur, et **ntddstor. h** pour les pilotes en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="da9fa-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="da9fa-120">Pour plus d’informations sur les fichiers d’en-tête, consultez [fichiers d’en-tête](#header-files).</span><span class="sxs-lookup"><span data-stu-id="da9fa-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="da9fa-121">[**IOCTL \_ \_ \_ Commande de protocole de stockage**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : utilisez cette IOCTL avec la structure de **\_ \_ commande du protocole de stockage** pour émettre des commandes NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="da9fa-122">Cette IOCTL active l’interconnexion NVMe et prend en charge le journal des effets de commande dans NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="da9fa-123">Vous pouvez l’utiliser avec des commandes spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="da9fa-124">Pour plus d’informations, consultez [mécanisme direct](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="da9fa-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="da9fa-125">[**Stockage \_ \_Commande de protocole**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : cette structure de mémoire tampon d’entrée comprend un champ **ReturnStatus** qui peut être utilisé pour signaler les valeurs d’État suivantes.</span><span class="sxs-lookup"><span data-stu-id="da9fa-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="da9fa-126">**État du protocole de stockage \_ \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="da9fa-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="da9fa-127">**État du protocole de stockage \_ \_ \_ réussite**</span><span class="sxs-lookup"><span data-stu-id="da9fa-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="da9fa-128">**\_erreur d' \_ État du protocole de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="da9fa-129">**demande d’État du protocole de stockage \_ \_ \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="da9fa-130">**État du protocole de stockage \_ \_ \_ sans \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="da9fa-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="da9fa-131">**État du protocole de stockage \_ \_ \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="da9fa-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="da9fa-132">**\_dépassement des \_ données d’État du protocole de stockage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="da9fa-133">**État du protocole de stockage- \_ \_ \_ ressources insuffisantes \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="da9fa-134">**État du protocole de stockage \_ \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="da9fa-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="da9fa-135">[**IOCTL \_ \_ \_ Propriété de requête de stockage**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : utilisez cette IOCTL avec la structure de **\_ \_ requête de propriété de stockage** pour récupérer les informations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da9fa-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="da9fa-136">Pour plus d’informations, consultez requêtes [spécifiques au protocole](#protocol-specific-queries) et [requêtes de température](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="da9fa-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="da9fa-137">[**Stockage \_ \_Requête de propriété**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : cette structure comprend les champs **PropertyId** et **AdditionalParameters** pour spécifier les données à interroger.</span><span class="sxs-lookup"><span data-stu-id="da9fa-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="da9fa-138">Dans le champ **PropertyId** , utilisez l’énumération de l' **\_ \_ ID de propriété de stockage** pour spécifier le type de données.</span><span class="sxs-lookup"><span data-stu-id="da9fa-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="da9fa-139">Utilisez le champ **AdditionalParameters** pour spécifier plus de détails, en fonction du type de données.</span><span class="sxs-lookup"><span data-stu-id="da9fa-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="da9fa-140">Pour les données spécifiques au protocole, utilisez la structure de **\_ \_ \_ données spécifique au protocole de stockage** dans le champ **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="da9fa-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="da9fa-141">Pour les données de température, utilisez la structure d' **\_ \_ informations** sur la température du stockage dans le champ **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="da9fa-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="da9fa-142">[**Stockage \_ \_ID de propriété**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : cette énumération comprend de nouvelles valeurs qui permettent à la **\_ \_ \_ propriété de requête de stockage IOCTL** d’extraire des informations relatives au protocole et à la température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="da9fa-143">**StorageAdapterProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="da9fa-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="da9fa-144">**StorageDeviceProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="da9fa-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="da9fa-145">Utilisez l’un de ces ID de propriété spécifiques au protocole en association avec des **\_ \_ \_ données de protocole de stockage** pour récupérer des données spécifiques au protocole dans la structure du [**\_ \_ \_ descripteur des données de protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="da9fa-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="da9fa-146">**StorageAdapterTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="da9fa-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="da9fa-147">**StorageDeviceTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="da9fa-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="da9fa-148">Utilisez l’un de ces ID de propriété de température pour récupérer les données de température dans la structure du [**\_ \_ \_ descripteur des données de température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="da9fa-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="da9fa-149">[**Stockage \_ \_ \_ Données spécifiques au protocole**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : permet de récupérer les données spécifiques à NVMe lorsque cette structure est utilisée pour le champ **AdditionalParameters** de la **\_ \_ requête de propriété de stockage** et qu’une valeur enum de [**\_ \_ \_ \_ type de données NVMe du protocole de stockage**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="da9fa-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="da9fa-150">Utilisez l’une des valeurs **de \_ \_ type de \_ données \_ NVME du protocole de stockage** suivantes dans le champ **DataType** de la structure de **\_ \_ \_ données spécifique au protocole de stockage** :</span><span class="sxs-lookup"><span data-stu-id="da9fa-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="da9fa-151">Utilisez **NVMeDataTypeIdentify** pour identifier les données du contrôleur ou identifier les données de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="da9fa-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="da9fa-152">Utilisez **NVMeDataTypeLogPage** pour accéder aux pages de journal (y compris les données d’intégrité/de santé).</span><span class="sxs-lookup"><span data-stu-id="da9fa-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="da9fa-153">Utilisez **NVMeDataTypeFeature** pour récupérer les fonctionnalités du lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="da9fa-154">[**Stockage \_ \_Informations de température**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : cette structure est utilisée pour stocker des données de température spécifiques.</span><span class="sxs-lookup"><span data-stu-id="da9fa-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="da9fa-155">Elle est utilisée dans le **\_ \_ \_ descripteur des données de TEMERATURE de stockage** pour retourner les résultats d’une requête de température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="da9fa-156">[**IOCTL \_ \_Seuil de \_ température \_ du jeu de stockage**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : utilisez cette IOCTL avec la structure du **\_ \_ seuil de température de stockage** pour définir les seuils de température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="da9fa-157">Pour plus d’informations, consultez [commandes de changement de comportement](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="da9fa-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="da9fa-158">[**Stockage \_ \_Seuil de température**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : cette structure est utilisée comme mémoire tampon d’entrée pour spécifier le seuil de température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="da9fa-159">Le champ de **surseuil** (booléen) spécifie si le champ de **seuil** est la valeur de seuil supérieur ou non (dans le cas contraire, il s’agit de la valeur de seuil).</span><span class="sxs-lookup"><span data-stu-id="da9fa-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="da9fa-160">Mécanisme de transfert</span><span class="sxs-lookup"><span data-stu-id="da9fa-160">Pass-through mechanism</span></span>

<span data-ttu-id="da9fa-161">Les commandes qui ne sont pas définies dans la spécification NVMe sont les plus difficiles à gérer par le système d’exploitation hôte : l’hôte n’a pas d’informations sur les effets que les commandes peuvent avoir sur l’appareil cible, l’infrastructure exposée (espaces de noms/tailles de bloc) et son comportement.</span><span class="sxs-lookup"><span data-stu-id="da9fa-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="da9fa-162">Pour mieux transporter de telles commandes spécifiques à des appareils via la pile de stockage Windows, un nouveau mécanisme direct permet de transférer les commandes spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="da9fa-163">Ce canal direct vous aide également à développer des outils de gestion et de test.</span><span class="sxs-lookup"><span data-stu-id="da9fa-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="da9fa-164">Toutefois, ce mécanisme direct nécessite l’utilisation du journal des effets de commande.</span><span class="sxs-lookup"><span data-stu-id="da9fa-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="da9fa-165">En outre, StoreNVMe.sys nécessite que toutes les commandes, et non pas uniquement les commandes de transfert, soient décrites dans le journal des effets de commande.</span><span class="sxs-lookup"><span data-stu-id="da9fa-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da9fa-166">StorNVMe.sys et Storport.sys bloquent toute commande sur un appareil s’il n’est pas décrit dans le journal des effets de commande.</span><span class="sxs-lookup"><span data-stu-id="da9fa-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="da9fa-167">Prise en charge du journal des effets de commande</span><span class="sxs-lookup"><span data-stu-id="da9fa-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="da9fa-168">Le journal des effets de commande (comme décrit dans commandes prises en charge et effets, section 5.10.1.5 de la [spécification NVMe 1,2](https://nvmexpress.org/specifications)) permet de décrire les effets des commandes spécifiques au fournisseur, ainsi que les commandes définies par la spécification.</span><span class="sxs-lookup"><span data-stu-id="da9fa-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="da9fa-169">Cela facilite la validation de la prise en charge des commandes, ainsi que l’optimisation du comportement des commandes, et doivent donc être implémentées pour l’ensemble des commandes que l’appareil prend en charge.</span><span class="sxs-lookup"><span data-stu-id="da9fa-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="da9fa-170">Les conditions suivantes décrivent le résultat de l’envoi de la commande en fonction de son entrée de journal des effets de commande.</span><span class="sxs-lookup"><span data-stu-id="da9fa-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="da9fa-171">Pour toute commande spécifique décrite dans le journal des effets de commande...</span><span class="sxs-lookup"><span data-stu-id="da9fa-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="da9fa-172">**Pendant**:</span><span class="sxs-lookup"><span data-stu-id="da9fa-172">**While**:</span></span>

-   <span data-ttu-id="da9fa-173">La commande prise en charge (CSUPP) est définie sur « 1 », ce qui signifie que la commande est prise en charge par le contrôleur (bit 01)</span><span class="sxs-lookup"><span data-stu-id="da9fa-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="da9fa-174">Quand CSUPP a la valeur « 0 » (ce qui signifie que la commande n’est pas prise en charge), la commande est bloquée</span><span class="sxs-lookup"><span data-stu-id="da9fa-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="da9fa-175">**Et si** l’une des conditions suivantes est définie :</span><span class="sxs-lookup"><span data-stu-id="da9fa-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="da9fa-176">La modification de la capacité du contrôleur (CCC) est définie sur « 1 », ce qui signifie que la commande peut modifier les fonctionnalités du contrôleur (bit 04)</span><span class="sxs-lookup"><span data-stu-id="da9fa-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="da9fa-177">La modification de l’inventaire des espaces de noms (NIC) est définie sur « 1 », ce qui signifie que la commande peut modifier le nombre, ou les fonctionnalités de plusieurs espaces de noms (bit 03)</span><span class="sxs-lookup"><span data-stu-id="da9fa-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="da9fa-178">La modification de la capacité d’espace de noms (CNSFM) est définie sur « 1 », ce qui signifie que la commande peut modifier les fonctionnalités d’un espace de noms unique (bit 02)</span><span class="sxs-lookup"><span data-stu-id="da9fa-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="da9fa-179">L’exécution de la commande (CSE) a la valeur 001B ou 010b, ce qui signifie que la commande peut être envoyée quand aucune autre commande n’est en suspens au même espace de noms ou à un espace de noms quelconque, et qu’une autre commande ne doit pas être envoyée au même espace de noms ou à un espace de noms jusqu’à ce que cette commande soit terminée (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="da9fa-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="da9fa-180">La commande est **alors** envoyée comme seule commande en suspens pour l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="da9fa-181">**Sinon, si**:</span><span class="sxs-lookup"><span data-stu-id="da9fa-181">**Else if**:</span></span>

-   <span data-ttu-id="da9fa-182">La valeur de l’exécution de la commande est définie sur 001B, ce qui signifie que la commande peut être envoyée lorsqu’il n’existe aucune autre commande en suspens vers le même espace de noms, et qu’une autre commande ne doit pas être envoyée au même espace de noms tant que cette commande n’est pas terminée (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="da9fa-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="da9fa-183">La commande est **alors** envoyée comme seule commande en suspens à l’objet de numéro d’unité logique (LUN).</span><span class="sxs-lookup"><span data-stu-id="da9fa-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="da9fa-184">Dans le **cas contraire**, la commande est envoyée avec d’autres commandes en attente sans inhibition.</span><span class="sxs-lookup"><span data-stu-id="da9fa-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="da9fa-185">Par exemple, si une commande spécifique au fournisseur est envoyée à l’appareil pour récupérer des informations statistiques qui ne sont pas définies par des spécifications, il ne doit y avoir aucun risque de modifier le comportement ou la capacité de l’appareil à exécuter des commandes d’e/s.</span><span class="sxs-lookup"><span data-stu-id="da9fa-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="da9fa-186">De telles demandes peuvent être effectuées en parallèle à des e/s et aucune pause-reprise n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="da9fa-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="da9fa-187">Utilisation \_ de la \_ \_ commande du protocole de stockage ioctl pour envoyer des commandes</span><span class="sxs-lookup"><span data-stu-id="da9fa-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="da9fa-188">Le transfert direct peut être effectué à l’aide de la [**\_ commande de \_ protocole \_ de stockage IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduite dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="da9fa-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="da9fa-189">Cette IOCTL a été conçue pour avoir un comportement similaire à celui des IOCTL pass-through SCSI et ATA existants, pour envoyer une commande incorporée à l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="da9fa-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="da9fa-190">Via cette IOCTL, l’envoi direct peut être envoyé à un périphérique de stockage, y compris un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="da9fa-191">Par exemple, dans NVMe, l’IOCTL autorise l’envoi des codes de commande suivants.</span><span class="sxs-lookup"><span data-stu-id="da9fa-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="da9fa-192">Commandes d’administration spécifiques au fournisseur (C0H – FFh)</span><span class="sxs-lookup"><span data-stu-id="da9fa-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="da9fa-193">Commandes NVMe spécifiques au fournisseur (80h – FFh)</span><span class="sxs-lookup"><span data-stu-id="da9fa-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="da9fa-194">Comme avec toutes les autres IOCTL, utilisez [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) pour envoyer l’IOCTL direct.</span><span class="sxs-lookup"><span data-stu-id="da9fa-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="da9fa-195">L’IOCTL est remplie à l’aide de la structure de mémoire tampon d’entrée de [**\_ \_ commande du protocole de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) trouvée dans **ntddstor. h**.</span><span class="sxs-lookup"><span data-stu-id="da9fa-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="da9fa-196">Renseignez le champ de **commande** avec la commande spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="da9fa-197">La commande spécifique au fournisseur à envoyer doit être renseignée dans le champ en surbrillance ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="da9fa-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="da9fa-198">Notez à nouveau que le journal des effets de commande doit être implémenté pour les commandes directes.</span><span class="sxs-lookup"><span data-stu-id="da9fa-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="da9fa-199">En particulier, ces commandes doivent être signalées telles qu’elles sont prises en charge dans le journal des effets de commande (voir la section précédente pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="da9fa-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="da9fa-200">Notez également que les champs PRP sont spécifiques aux pilotes, ce qui signifie que les applications qui envoient des commandes peuvent les conserver sous la forme 0.</span><span class="sxs-lookup"><span data-stu-id="da9fa-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="da9fa-201">Enfin, cette IOCTL directe est destinée à l’envoi de commandes spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="da9fa-202">Pour envoyer d’autres commandes NVMe d’administration ou non spécifiques à un fournisseur, telles que l’identification, cette IOCTL directe ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="da9fa-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="da9fa-203">Par exemple, **la \_ \_ \_ propriété de requête de stockage IOCTL** doit être utilisée pour identifier ou obtenir des pages de journal.</span><span class="sxs-lookup"><span data-stu-id="da9fa-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="da9fa-204">Pour plus d’informations, consultez la section suivante, [requêtes spécifiques au protocole](/windows).</span><span class="sxs-lookup"><span data-stu-id="da9fa-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="da9fa-205">Ne pas mettre à jour le microprogramme via le mécanisme de transfert</span><span class="sxs-lookup"><span data-stu-id="da9fa-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="da9fa-206">Les commandes de téléchargement et d’activation du microprogramme ne doivent pas être envoyées à l’aide de direct.</span><span class="sxs-lookup"><span data-stu-id="da9fa-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="da9fa-207">**IOCTL \_ La \_ \_ commande de protocole de stockage** doit être utilisée uniquement pour les commandes spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="da9fa-208">Au lieu de cela, utilisez les opérations d’IOCTL de stockage générales suivantes (introduites dans Windows 10) pour éviter les applications directement à l’aide \_ de la version de miniport SCSI de l’IOCTL du microprogramme.</span><span class="sxs-lookup"><span data-stu-id="da9fa-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="da9fa-209">Les pilotes de stockage traduisent l’IOCTL en une commande SCSI ou la \_ version de miniport SCSI de l’IOCTL sur le miniport.</span><span class="sxs-lookup"><span data-stu-id="da9fa-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="da9fa-210">Ces IOCTL sont recommandées pour développer les outils de mise à niveau de microprogramme dans Windows 10 et Windows Server 2016 :</span><span class="sxs-lookup"><span data-stu-id="da9fa-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="da9fa-211">**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="da9fa-212">**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="da9fa-213">**\_ \_ activation du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="da9fa-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="da9fa-214">Pour obtenir des informations de stockage et mettre à jour le microprogramme, Windows prend également en charge les applets de commande PowerShell pour effectuer cette tâche rapidement :</span><span class="sxs-lookup"><span data-stu-id="da9fa-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="da9fa-215">Pour mettre à jour le microprogramme sur NVMe dans Windows 8.1, utilisez le \_ \_ microprogramme de miniport SCSI IOCTL \_ .</span><span class="sxs-lookup"><span data-stu-id="da9fa-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="da9fa-216">Cette IOCTL n’a pas été reportée vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da9fa-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="da9fa-217">Pour plus d’informations, consultez [mise à niveau du microprogramme d’un appareil NVMe dans Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="da9fa-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="da9fa-218">Retour d’erreurs via le mécanisme de transfert</span><span class="sxs-lookup"><span data-stu-id="da9fa-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="da9fa-219">À l’instar des IOCTL SCSI et ATA directe, quand une commande/demande est envoyée au miniport ou au périphérique, l’IOCTL retourne si elle a réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="da9fa-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="da9fa-220">Dans la structure de [**\_ \_ commande du protocole de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , l’IOCTL retourne l’état via le champ **ReturnStatus** .</span><span class="sxs-lookup"><span data-stu-id="da9fa-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="da9fa-221">Exemple : envoi d’une commande spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="da9fa-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="da9fa-222">Dans cet exemple, une commande arbitraire spécifique au fournisseur (0xFF) est envoyée via un transfert vers un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="da9fa-223">Le code suivant alloue une mémoire tampon, Initialise une requête, puis envoie la commande à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="da9fa-224">Dans cet exemple, nous nous attendons à ce que `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` la commande aboutisse à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da9fa-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="da9fa-225">Requêtes spécifiques au protocole</span><span class="sxs-lookup"><span data-stu-id="da9fa-225">Protocol-specific queries</span></span>

<span data-ttu-id="da9fa-226">Windows 8.1 a introduit la [**\_ propriété de \_ requête \_ de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="da9fa-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="da9fa-227">Dans Windows 10, l’IOCTL a été améliorée pour prendre en charge les fonctionnalités NVMe couramment demandées, telles que les **pages de journalisation**, les **fonctionnalités d’extraction** et l' **identification**.</span><span class="sxs-lookup"><span data-stu-id="da9fa-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="da9fa-228">Cela permet la récupération d’informations spécifiques à NVMe à des fins de surveillance et d’inventaire.</span><span class="sxs-lookup"><span data-stu-id="da9fa-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="da9fa-229">La mémoire tampon d’entrée pour la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) ioctl (à partir de Windows 10) est présentée ici.</span><span class="sxs-lookup"><span data-stu-id="da9fa-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="da9fa-230">Lorsque vous utilisez la [**\_ propriété de \_ requête \_ de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour récupérer les informations spécifiques au protocole NVMe dans le [**\_ \_ \_ descripteur des données de protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configurez la structure de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) comme suit :</span><span class="sxs-lookup"><span data-stu-id="da9fa-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="da9fa-231">Allouez une mémoire tampon qui peut contenir à la fois une [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) et une structure de [**\_ \_ \_ données spécifique**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) à un protocole de stockage.</span><span class="sxs-lookup"><span data-stu-id="da9fa-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="da9fa-232">Définissez le champ **PropertyId** sur **StorageAdapterProtocolSpecificProperty** ou **StorageDeviceProtocolSpecificProperty** pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.</span><span class="sxs-lookup"><span data-stu-id="da9fa-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="da9fa-233">Définissez le champ **QueryType** sur **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="da9fa-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="da9fa-234">Remplissez la structure de [**\_ \_ \_ données spécifique au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) avec les valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="da9fa-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="da9fa-235">Le début des **\_ \_ \_ données spécifiques au protocole de stockage** est le champ **AdditionalParameters** de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="da9fa-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="da9fa-236">La [**structure \_ \_ des \_ données spécifiques au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (à partir de Windows 10) est indiquée ici.</span><span class="sxs-lookup"><span data-stu-id="da9fa-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="da9fa-237">Pour spécifier un type d’informations propres au protocole NVMe, configurez la structure de [**\_ \_ \_ données spécifique au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) comme suit :</span><span class="sxs-lookup"><span data-stu-id="da9fa-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="da9fa-238">Définissez le champ **ProtocolType** sur **ProtocolTypeNVMe**.</span><span class="sxs-lookup"><span data-stu-id="da9fa-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="da9fa-239">Définissez le champ **DataType** sur une valeur d’énumération définie par le [**\_ \_ \_ \_ type de données NVME du protocole de stockage**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span><span class="sxs-lookup"><span data-stu-id="da9fa-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="da9fa-240">Utilisez **NVMeDataTypeIdentify** pour identifier les données du contrôleur ou identifier les données de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="da9fa-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="da9fa-241">Utilisez **NVMeDataTypeLogPage** pour accéder aux pages de journal (y compris les données d’intégrité/de santé).</span><span class="sxs-lookup"><span data-stu-id="da9fa-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="da9fa-242">Utilisez **NVMeDataTypeFeature** pour récupérer les fonctionnalités du lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="da9fa-243">Lorsque **ProtocolTypeNVMe** est utilisé comme le **ProtocolType**, les requêtes relatives aux informations spécifiques au protocole peuvent être récupérées en parallèle avec d’autres e/s sur le lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="da9fa-244">Les exemples suivants illustrent des requêtes spécifiques au protocole NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="da9fa-245">Exemple : requête d’identification NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="da9fa-246">Dans cet exemple, la demande d' **identification** est envoyée à un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="da9fa-247">Le code suivant initialise la structure de données de la requête, puis l’envoie à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="da9fa-248">Notez que l’appelant doit allouer une seule mémoire tampon contenant \_ \_ la requête de propriété de stockage et la taille des \_ données spécifiques au protocole de stockage \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="da9fa-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="da9fa-249">Dans cet exemple, il utilise la même mémoire tampon pour l’entrée et la sortie de la requête de propriété.</span><span class="sxs-lookup"><span data-stu-id="da9fa-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="da9fa-250">C’est la raison pour laquelle la mémoire tampon qui a été allouée a une taille de « décalage de champ \_ (requête de propriété de stockage \_ \_ , AdditionalParameters) + sizeof ( \_ données spécifiques au protocole de stockage \_ \_ ) + \_ taille maximale des \_ journaux NVME \_ ».</span><span class="sxs-lookup"><span data-stu-id="da9fa-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="da9fa-251">Bien qu’il soit possible d’allouer des tampons distincts à la fois pour l’entrée et la sortie, nous vous recommandons d’utiliser une seule mémoire tampon pour interroger les informations relatives à NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="da9fa-252">Exemple : requête des pages du journal d’extraction NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="da9fa-253">Dans cet exemple, en fonction de la précédente, la requête _ *obtenir le journal des pages*\* est envoyée à un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="da9fa-254">Le code suivant prépare la structure des données de la requête, puis envoie la commande à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="da9fa-255">Exemple : requête obtenir des fonctionnalités NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="da9fa-256">Dans cet exemple, en fonction de la précédente, la demande _ *obtenir des fonctionnalités*\* est envoyée à un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="da9fa-257">Le code suivant prépare la structure des données de la requête, puis envoie la commande à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="da9fa-258">Ensemble spécifique au protocole</span><span class="sxs-lookup"><span data-stu-id="da9fa-258">Protocol-specific set</span></span>

<span data-ttu-id="da9fa-259">À partir de Windows 10 19H1, le IOCTL_STORAGE_SET_PROPERTY a été amélioré pour prendre en charge les fonctionnalités Set NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="da9fa-260">La mémoire tampon d’entrée pour le IOCTL_STORAGE_SET_PROPERTY est présentée ici :</span><span class="sxs-lookup"><span data-stu-id="da9fa-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="da9fa-261">Quand vous utilisez IOCTL_STORAGE_SET_PROPERTY pour définir la fonctionnalité NVMe, configurez la structure STORAGE_PROPERTY_SET comme suit :</span><span class="sxs-lookup"><span data-stu-id="da9fa-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="da9fa-262">Allouez une mémoire tampon qui peut contenir à la fois une STORAGE_PROPERTY_SET et une structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT ;</span><span class="sxs-lookup"><span data-stu-id="da9fa-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="da9fa-263">Définissez le champ PropertyID sur StorageAdapterProtocolSpecificProperty ou StorageDeviceProtocolSpecificProperty pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.</span><span class="sxs-lookup"><span data-stu-id="da9fa-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="da9fa-264">Remplissez la structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT avec les valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="da9fa-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="da9fa-265">Le début de la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT est le champ AdditionalParameters de STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="da9fa-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="da9fa-266">La structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT est présentée ici.</span><span class="sxs-lookup"><span data-stu-id="da9fa-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="da9fa-267">Pour spécifier un type de fonctionnalité NVMe à définir, configurez la structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT comme suit :</span><span class="sxs-lookup"><span data-stu-id="da9fa-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="da9fa-268">Définissez le champ ProtocolType sur ProtocolTypeNvme ;</span><span class="sxs-lookup"><span data-stu-id="da9fa-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="da9fa-269">Définissez le champ DataType sur la valeur d’énumération NVMeDataTypeFeature définie par STORAGE_PROTOCOL_NVME_DATA_TYPE ;</span><span class="sxs-lookup"><span data-stu-id="da9fa-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="da9fa-270">Les exemples suivants illustrent l’ensemble de fonctionnalités NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="da9fa-271">Exemple : fonctions set de NVMe</span><span class="sxs-lookup"><span data-stu-id="da9fa-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="da9fa-272">Dans cet exemple, la demande Set features est envoyée à un lecteur NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="da9fa-273">Le code suivant prépare la structure de données Set, puis envoie la commande à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="da9fa-274">Requêtes de température</span><span class="sxs-lookup"><span data-stu-id="da9fa-274">Temperature queries</span></span>

<span data-ttu-id="da9fa-275">Dans Windows 10, [**la \_ \_ \_ propriété requête de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) peut également être utilisée pour interroger des données de température à partir d’appareils NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="da9fa-276">Pour récupérer les informations de température d’un lecteur NVMe dans le [**\_ \_ \_ descripteur des données de température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configurez la structure de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) comme suit :</span><span class="sxs-lookup"><span data-stu-id="da9fa-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="da9fa-277">Allouez une mémoire tampon qui peut contenir une structure de [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .</span><span class="sxs-lookup"><span data-stu-id="da9fa-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="da9fa-278">Définissez le champ **PropertyId** sur **StorageAdapterTemperatureProperty** ou **StorageDeviceTemperatureProperty** pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.</span><span class="sxs-lookup"><span data-stu-id="da9fa-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="da9fa-279">Définissez le champ **QueryType** sur **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="da9fa-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="da9fa-280">La structure d' [**\_ \_ informations sur la température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (à partir de Windows 10) est indiquée ici.</span><span class="sxs-lookup"><span data-stu-id="da9fa-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="da9fa-281">Commandes de modification de comportement</span><span class="sxs-lookup"><span data-stu-id="da9fa-281">Behavior changing commands</span></span>

<span data-ttu-id="da9fa-282">Les commandes qui manipulent les attributs de l’appareil ou qui peuvent avoir un impact sur le comportement de l’appareil sont plus difficiles à traiter par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="da9fa-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="da9fa-283">Si les attributs de l’appareil changent au moment de l’exécution pendant le traitement des e/s, des problèmes de synchronisation ou d’intégrité des données peuvent survenir si le traitement n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="da9fa-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="da9fa-284">La commande **Set-featurs** NVMe est un bon exemple de commande de changement de comportement.</span><span class="sxs-lookup"><span data-stu-id="da9fa-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="da9fa-285">Il permet de modifier le mécanisme d’arbitrage et le paramétrage des seuils de température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="da9fa-286">Pour s’assurer que les données en cours ne sont pas menacées lorsque des commandes SET affectant le comportement sont envoyées, Windows suspend toutes les e/s sur l’appareil NVMe, draine les files d’attente et vide les tampons.</span><span class="sxs-lookup"><span data-stu-id="da9fa-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="da9fa-287">Une fois l’exécution de la commande set terminée, l’e/s reprend (si possible).</span><span class="sxs-lookup"><span data-stu-id="da9fa-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="da9fa-288">Si les e/s ne peuvent pas être reprises, une réinitialisation de l’appareil peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="da9fa-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="da9fa-289">Définition des seuils de température</span><span class="sxs-lookup"><span data-stu-id="da9fa-289">Setting temperature thresholds</span></span>

<span data-ttu-id="da9fa-290">Windows 10 a introduit le [**seuil de température du \_ jeu de stockage \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), une ioctl pour l’obtention et la définition des seuils de température.</span><span class="sxs-lookup"><span data-stu-id="da9fa-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="da9fa-291">Vous pouvez également l’utiliser pour récupérer la température actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da9fa-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="da9fa-292">La mémoire tampon d’entrée/sortie pour cette IOCTL est la structure d' [**\_ \_ informations sur la température du stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , à partir de la section de code précédente.</span><span class="sxs-lookup"><span data-stu-id="da9fa-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="da9fa-293">Exemple : définition de la température sur seuil</span><span class="sxs-lookup"><span data-stu-id="da9fa-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="da9fa-294">Dans cet exemple, la température de dépassement du seuil d’un lecteur NVMe est définie.</span><span class="sxs-lookup"><span data-stu-id="da9fa-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="da9fa-295">Le code suivant prépare la commande, puis l’envoie à l’appareil via DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="da9fa-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="da9fa-296">Définition des fonctionnalités spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="da9fa-296">Setting vendor-specific features</span></span>

<span data-ttu-id="da9fa-297">Sans le journal des effets de commande, le pilote n’a aucune connaissance des ramifications de la commande.</span><span class="sxs-lookup"><span data-stu-id="da9fa-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="da9fa-298">C’est la raison pour laquelle le journal des effets de commande est requis.</span><span class="sxs-lookup"><span data-stu-id="da9fa-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="da9fa-299">Il permet au système d’exploitation de déterminer si une commande a un impact important et si elle peut être envoyée en parallèle avec d’autres commandes sur le lecteur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="da9fa-300">Le journal des effets de commandes n’est pas encore suffisamment granulaire pour englober les commandes **Set-features** spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="da9fa-301">Pour cette raison, il n’est pas encore possible d’envoyer des commandes **Set-features** spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="da9fa-302">Toutefois, il est possible d’utiliser le mécanisme de transfert, décrit précédemment, pour envoyer des commandes spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="da9fa-303">Pour plus d’informations, consultez [mécanisme direct](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="da9fa-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="da9fa-304">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="da9fa-304">Header files</span></span>

<span data-ttu-id="da9fa-305">Les fichiers suivants s’appliquent au développement NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="da9fa-306">Ces fichiers sont fournis avec le [Kit de développement logiciel (SDK) Microsoft Windows](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="da9fa-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="da9fa-307">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="da9fa-307">Header file</span></span>    | <span data-ttu-id="da9fa-308">Description</span><span class="sxs-lookup"><span data-stu-id="da9fa-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da9fa-309">**ntddstor. h**</span><span class="sxs-lookup"><span data-stu-id="da9fa-309">**ntddstor.h**</span></span> | <span data-ttu-id="da9fa-310">Définit des constantes et des types pour accéder aux pilotes de la classe de stockage à partir du mode noyau.</span><span class="sxs-lookup"><span data-stu-id="da9fa-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="da9fa-311">**nVMe. h**</span><span class="sxs-lookup"><span data-stu-id="da9fa-311">**nvme.h**</span></span>     | <span data-ttu-id="da9fa-312">Pour d’autres structures de données associées à NVMe.</span><span class="sxs-lookup"><span data-stu-id="da9fa-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="da9fa-313">**winioctl. h**</span><span class="sxs-lookup"><span data-stu-id="da9fa-313">**winioctl.h**</span></span> | <span data-ttu-id="da9fa-314">Pour les définitions globales IOCTL Win32, y compris les API de stockage pour les applications en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da9fa-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
