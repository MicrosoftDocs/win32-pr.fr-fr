---
description: Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: TargetForwardingHistory, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111655"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="495b3-103">TargetForwardingHistory, classe</span><span class="sxs-lookup"><span data-stu-id="495b3-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="495b3-104">Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="495b3-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="495b3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="495b3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="495b3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="495b3-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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

## <a name="members"></a><span data-ttu-id="495b3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="495b3-107">Members</span></span>

<span data-ttu-id="495b3-108">La classe **TargetForwardingHistory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="495b3-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="495b3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="495b3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="495b3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="495b3-110">Properties</span></span>

<span data-ttu-id="495b3-111">La classe **TargetForwardingHistory** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="495b3-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="495b3-112">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="495b3-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-115">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-116">Informations de point de terminaison du serveur collecteur.</span><span class="sxs-lookup"><span data-stu-id="495b3-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="495b3-117">Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .</span><span class="sxs-lookup"><span data-stu-id="495b3-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-118">**Ordinateur**</span><span class="sxs-lookup"><span data-stu-id="495b3-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-121">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-122">Nom d’ordinateur de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="495b3-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-123">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="495b3-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-124">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="495b3-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-126">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-127">Horodateur qui indique quand la connexion a été établie pour les données de transfert.</span><span class="sxs-lookup"><span data-stu-id="495b3-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-128">**Destination**</span><span class="sxs-lookup"><span data-stu-id="495b3-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-131">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-132">Destination des données de transfert, par exemple un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="495b3-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-133">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="495b3-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-136">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-137">Format utilisé pour générer la destination des données de transfert.</span><span class="sxs-lookup"><span data-stu-id="495b3-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-138">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="495b3-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-139">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="495b3-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-141">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-142">Horodateur qui indique le moment où la connexion a été déconnectée.</span><span class="sxs-lookup"><span data-stu-id="495b3-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-143">**Error**</span><span class="sxs-lookup"><span data-stu-id="495b3-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-146">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-147">Message d’erreur qui décrit une erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="495b3-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="495b3-148">Cette propriété est vide si aucune erreur n’a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="495b3-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-149">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="495b3-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-152">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-153">Type de fichier qui contient les données de transfert, telles que ETL.</span><span class="sxs-lookup"><span data-stu-id="495b3-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-154">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="495b3-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-157">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-158">Informations de point de terminaison de l’ordinateur cible, dans un format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="495b3-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="495b3-159">Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .</span><span class="sxs-lookup"><span data-stu-id="495b3-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="495b3-160">Par exemple, « 127.0.0.1:50000 ».</span><span class="sxs-lookup"><span data-stu-id="495b3-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="495b3-161">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="495b3-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-164">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-165">**GUID** SMBIOS de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="495b3-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-166">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="495b3-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495b3-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-169">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-170">Adresse MAC de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="495b3-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="495b3-171">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="495b3-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495b3-172">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="495b3-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="495b3-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495b3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495b3-174">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="495b3-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="495b3-175">Horodateur du moment où ce changement d’État a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="495b3-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="495b3-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="495b3-176">Requirements</span></span>



| <span data-ttu-id="495b3-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="495b3-177">Requirement</span></span> | <span data-ttu-id="495b3-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="495b3-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495b3-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495b3-179">Minimum supported client</span></span><br/> | <span data-ttu-id="495b3-180">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="495b3-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="495b3-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495b3-181">Minimum supported server</span></span><br/> | <span data-ttu-id="495b3-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="495b3-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="495b3-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="495b3-183">Namespace</span></span><br/>                | <span data-ttu-id="495b3-184">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="495b3-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="495b3-185">MOF</span><span class="sxs-lookup"><span data-stu-id="495b3-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="495b3-186"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="495b3-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="495b3-187">DLL</span><span class="sxs-lookup"><span data-stu-id="495b3-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="495b3-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="495b3-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="495b3-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="495b3-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495b3-190">Fournisseur WMI du collecteur d’événements de démarrage</span><span class="sxs-lookup"><span data-stu-id="495b3-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

