---
description: Récupère les données de transfert d’un ordinateur cible.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: TargetForwarding, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522908"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="3a011-103">TargetForwarding, classe</span><span class="sxs-lookup"><span data-stu-id="3a011-103">TargetForwarding class</span></span>

<span data-ttu-id="3a011-104">Récupère les données de transfert d’un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3a011-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="3a011-105">Plusieurs redirecteurs peuvent être configurés sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3a011-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="3a011-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3a011-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a011-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a011-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a><span data-ttu-id="3a011-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3a011-108">Members</span></span>

<span data-ttu-id="3a011-109">La classe **TargetForwarding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a011-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="3a011-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a011-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a011-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a011-111">Properties</span></span>

<span data-ttu-id="3a011-112">La classe **TargetForwarding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a011-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a011-113">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="3a011-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-116">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-117">Informations de point de terminaison du serveur collecteur.</span><span class="sxs-lookup"><span data-stu-id="3a011-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="3a011-118">Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .</span><span class="sxs-lookup"><span data-stu-id="3a011-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-119">**Ordinateur**</span><span class="sxs-lookup"><span data-stu-id="3a011-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-122">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-123">Nom d’ordinateur de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3a011-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="3a011-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-125">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a011-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-127">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-128">Horodateur qui indique quand la connexion a été établie pour les données de transfert.</span><span class="sxs-lookup"><span data-stu-id="3a011-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-129">**Destination**</span><span class="sxs-lookup"><span data-stu-id="3a011-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-132">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-133">Destination des données de transfert, par exemple un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3a011-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-134">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="3a011-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-137">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-138">Format utilisé pour générer la destination des données de transfert.</span><span class="sxs-lookup"><span data-stu-id="3a011-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-139">**Error**</span><span class="sxs-lookup"><span data-stu-id="3a011-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-142">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-143">Message d’erreur qui décrit une erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="3a011-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="3a011-144">Cette propriété est vide si aucune erreur n’a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="3a011-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-145">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="3a011-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-148">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-149">Type de fichier qui contient les données de transfert, telles que ETL.</span><span class="sxs-lookup"><span data-stu-id="3a011-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-150">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="3a011-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-153">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-154">Informations de point de terminaison de l’ordinateur cible, dans un format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a011-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="3a011-155">Cette propriété est mise en forme en tant que chaîne d' *hôte*:*port* .</span><span class="sxs-lookup"><span data-stu-id="3a011-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="3a011-156">Par exemple, « 127.0.0.1:50000 ».</span><span class="sxs-lookup"><span data-stu-id="3a011-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="3a011-157">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="3a011-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-160">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-161">**GUID** SMBIOS de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3a011-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="3a011-162">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="3a011-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a011-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a011-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a011-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a011-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a011-165">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a011-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a011-166">Adresse MAC de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3a011-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a011-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a011-167">Requirements</span></span>



| <span data-ttu-id="3a011-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a011-168">Requirement</span></span> | <span data-ttu-id="3a011-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a011-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a011-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a011-170">Minimum supported client</span></span><br/> | <span data-ttu-id="3a011-171">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a011-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3a011-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a011-172">Minimum supported server</span></span><br/> | <span data-ttu-id="3a011-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3a011-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="3a011-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a011-174">Namespace</span></span><br/>                | <span data-ttu-id="3a011-175">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="3a011-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="3a011-176">MOF</span><span class="sxs-lookup"><span data-stu-id="3a011-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a011-177"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a011-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a011-178">DLL</span><span class="sxs-lookup"><span data-stu-id="3a011-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a011-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a011-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3a011-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a011-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a011-181">Fournisseur WMI du collecteur d’événements de démarrage</span><span class="sxs-lookup"><span data-stu-id="3a011-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

