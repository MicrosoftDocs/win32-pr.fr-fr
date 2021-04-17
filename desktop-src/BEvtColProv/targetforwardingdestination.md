---
description: Destinations connues contenant les données collectées. Disponible uniquement si le collecteur est en cours d’exécution avec le journal d’état activé.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: TargetForwardingDestination, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482793"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="752c8-104">TargetForwardingDestination, classe</span><span class="sxs-lookup"><span data-stu-id="752c8-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="752c8-105">Destinations connues contenant les données collectées.</span><span class="sxs-lookup"><span data-stu-id="752c8-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="752c8-106">Disponible uniquement si le collecteur est en cours d’exécution avec le journal d’état activé.</span><span class="sxs-lookup"><span data-stu-id="752c8-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="752c8-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="752c8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="752c8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="752c8-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="752c8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="752c8-109">Members</span></span>

<span data-ttu-id="752c8-110">La classe **TargetForwardingDestination** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="752c8-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="752c8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="752c8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="752c8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="752c8-112">Properties</span></span>

<span data-ttu-id="752c8-113">La classe **TargetForwardingDestination** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="752c8-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="752c8-114">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="752c8-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-117">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-118">Hôte : informations de port du point de terminaison sur le côté du collecteur.</span><span class="sxs-lookup"><span data-stu-id="752c8-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-119">**Ordinateur**</span><span class="sxs-lookup"><span data-stu-id="752c8-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-122">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-123">Nom de l’ordinateur cible, tel que déterminé par le collecteur en fonction de sa configuration.</span><span class="sxs-lookup"><span data-stu-id="752c8-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="752c8-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-125">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="752c8-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-127">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-128">Horodateur de l’établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="752c8-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-129">**Destination**</span><span class="sxs-lookup"><span data-stu-id="752c8-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-132">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-133">Destination des données.</span><span class="sxs-lookup"><span data-stu-id="752c8-133">Destination of the data.</span></span> <span data-ttu-id="752c8-134">La signification dépend du type de redirecteur.</span><span class="sxs-lookup"><span data-stu-id="752c8-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="752c8-135">Il peut s’agir d’un nom de fichier ou d’une autre identification.</span><span class="sxs-lookup"><span data-stu-id="752c8-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-136">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="752c8-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-139">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-140">Modèle utilisé pour générer la destination des données.</span><span class="sxs-lookup"><span data-stu-id="752c8-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="752c8-141">La signification dépend du type et de la configuration du redirecteur.</span><span class="sxs-lookup"><span data-stu-id="752c8-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="752c8-142">Pour une destination fixe, est identique à la destination elle-même.</span><span class="sxs-lookup"><span data-stu-id="752c8-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="752c8-143">Pour la destination avec une rotation des fichiers, contient les caractères de modèle qui seront remplacés par l’index réel dans la destination.</span><span class="sxs-lookup"><span data-stu-id="752c8-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-144">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="752c8-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-145">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="752c8-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-147">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-148">Horodateur de la suppression de la connexion.</span><span class="sxs-lookup"><span data-stu-id="752c8-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-149">**Error**</span><span class="sxs-lookup"><span data-stu-id="752c8-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-152">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-153">Message d’erreur si une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="752c8-153">Error message if an error was encountered.</span></span> <span data-ttu-id="752c8-154">Sinon, est vide.</span><span class="sxs-lookup"><span data-stu-id="752c8-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="752c8-155">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="752c8-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-158">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-159">Type du redirecteur (par exemple, « ETL »).</span><span class="sxs-lookup"><span data-stu-id="752c8-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="752c8-160">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="752c8-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-163">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-164">Informations de point de terminaison de l’ordinateur cible, dans un format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="752c8-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="752c8-165">Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .</span><span class="sxs-lookup"><span data-stu-id="752c8-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="752c8-166">Par exemple, « 127.0.0.1:50000 ».</span><span class="sxs-lookup"><span data-stu-id="752c8-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="752c8-167">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="752c8-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-170">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-171">GUID SMBIOS de l’ordinateur cible (s’il est connu).</span><span class="sxs-lookup"><span data-stu-id="752c8-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="752c8-172">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="752c8-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752c8-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-175">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-176">Adresse MAC de l’ordinateur cible (si connue).</span><span class="sxs-lookup"><span data-stu-id="752c8-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="752c8-177">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="752c8-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752c8-178">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="752c8-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="752c8-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752c8-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="752c8-180">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="752c8-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="752c8-181">Horodateur du moment où ce changement d’État a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="752c8-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="752c8-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="752c8-182">Requirements</span></span>



| <span data-ttu-id="752c8-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="752c8-183">Requirement</span></span> | <span data-ttu-id="752c8-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="752c8-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752c8-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="752c8-185">Minimum supported client</span></span><br/> | <span data-ttu-id="752c8-186">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="752c8-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="752c8-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="752c8-187">Minimum supported server</span></span><br/> | <span data-ttu-id="752c8-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="752c8-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="752c8-189">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="752c8-189">Namespace</span></span><br/>                | <span data-ttu-id="752c8-190">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="752c8-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="752c8-191">MOF</span><span class="sxs-lookup"><span data-stu-id="752c8-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="752c8-192"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="752c8-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="752c8-193">DLL</span><span class="sxs-lookup"><span data-stu-id="752c8-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="752c8-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="752c8-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

