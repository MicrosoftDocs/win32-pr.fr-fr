---
description: Représente une paire clé/valeur.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529438"
---
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="a27ee-103">MSVM \_ KvpExchangeDataItem, classe</span><span class="sxs-lookup"><span data-stu-id="a27ee-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="a27ee-104">Représente une paire clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="a27ee-104">Represents a key/value pair.</span></span>

<span data-ttu-id="a27ee-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a27ee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a27ee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a27ee-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="a27ee-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a27ee-107">Members</span></span>

<span data-ttu-id="a27ee-108">La classe **MSVM \_ KvpExchangeDataItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a27ee-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="a27ee-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a27ee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a27ee-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a27ee-110">Properties</span></span>

<span data-ttu-id="a27ee-111">La classe **MSVM \_ KvpExchangeDataItem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a27ee-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a27ee-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a27ee-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a27ee-115">A short description of the object.</span></span> <span data-ttu-id="a27ee-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a27ee-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a27ee-117">**Données**</span><span class="sxs-lookup"><span data-stu-id="a27ee-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="a27ee-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-121">Partie valeur de la paire clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="a27ee-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="a27ee-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="a27ee-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-125">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="a27ee-125">A description of the object.</span></span> <span data-ttu-id="a27ee-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a27ee-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a27ee-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a27ee-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-130">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a27ee-130">A display name for the object.</span></span> <span data-ttu-id="a27ee-131">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a27ee-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a27ee-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a27ee-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-135">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="a27ee-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-136">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a27ee-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a27ee-137">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a27ee-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a27ee-138">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a27ee-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a27ee-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-141">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="a27ee-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-142">Partie clé de la paire clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="a27ee-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="a27ee-143">Clé</span><span class="sxs-lookup"><span data-stu-id="a27ee-143">Key</span></span>                                                                                                     | <span data-ttu-id="a27ee-144">Description</span><span class="sxs-lookup"><span data-stu-id="a27ee-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a27ee-145"><dt>"CSDVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="a27ee-146">Chaîne qui représente le dernier Service Pack installé sur le système invité.</span><span class="sxs-lookup"><span data-stu-id="a27ee-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="a27ee-147">Par exemple, « Service Pack 2 ».</span><span class="sxs-lookup"><span data-stu-id="a27ee-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="a27ee-148">Si aucun Service Pack n’a été installé, cette chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="a27ee-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a27ee-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="a27ee-150">Chaîne qui représente le nom DNS complet qui identifie de façon unique l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a27ee-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="a27ee-151">Ce nom est une combinaison du nom d’hôte DNS et du nom de domaine DNS, en utilisant *le format nom d’hôte.* *Nom_domaine*.</span><span class="sxs-lookup"><span data-stu-id="a27ee-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="a27ee-152">Si l’ordinateur local est un nœud dans un cluster, cette valeur est le nom DNS complet du serveur virtuel de cluster.</span><span class="sxs-lookup"><span data-stu-id="a27ee-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="a27ee-153">Cette valeur correspond au nom retourné par la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) lorsque le paramètre *NameType* est « ComputerNameDnsFullyQualified ».</span><span class="sxs-lookup"><span data-stu-id="a27ee-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="a27ee-154"><dt>"IntegrationServicesVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="a27ee-155">Chaîne représentant la version de la Integration Services actuellement installée sur la machine virtuelle invitée (par exemple, « 6.1.7000.0 »).</span><span class="sxs-lookup"><span data-stu-id="a27ee-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a27ee-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="a27ee-157">Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv4 actuellement affectées à la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="a27ee-158">La liste est automatiquement mise à jour chaque fois qu’une modification de configuration TCP/IP se produit sur la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="a27ee-159">Chaque adresse est représentée sous la forme d’une notation décimale à points.</span><span class="sxs-lookup"><span data-stu-id="a27ee-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="a27ee-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="a27ee-161">Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv6 actuellement affectées à la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="a27ee-162">La liste est automatiquement mise à jour chaque fois qu’une modification de configuration TCP/IP se produit sur la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="a27ee-163">Chaque adresse est représentée en notation hexadécimale à deux-points.</span><span class="sxs-lookup"><span data-stu-id="a27ee-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="a27ee-164">Il n’est pas garanti que les listes IPv4 et IPv6 soient synchronisées à tout moment.</span><span class="sxs-lookup"><span data-stu-id="a27ee-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="a27ee-165"><dt>"OSBuildNumber"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="a27ee-166">Chaîne qui représente le numéro de build du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="a27ee-167"><dt>"OSEditionId"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="a27ee-168">Chaîne représentant l’édition (SKU) du système d’exploitation de la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="a27ee-169">Pour obtenir la liste des valeurs possibles, consultez la fonction [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="a27ee-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="a27ee-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="a27ee-171">Chaîne qui représente le nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="a27ee-172">Cette valeur provient de l’entrée de Registre suivante : **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="a27ee-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="a27ee-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="a27ee-174">Chaîne qui représente le numéro de version principale du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="a27ee-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="a27ee-176">Chaîne qui représente le numéro de version mineure du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="a27ee-177"><dt>"OSPlatformId"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="a27ee-178">Chaîne qui représente la plateforme du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="a27ee-179">Les valeurs possibles de la propriété de **données** sont « 1 » pour indiquer un système Windows non pris en charge et « 2 » pour indiquer un système Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a27ee-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="a27ee-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="a27ee-181">Chaîne qui représente la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-181">A string that represents the operating system version.</span></span> <span data-ttu-id="a27ee-182">Le format de cette chaîne est *MajorVersion*. *MinorVersion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="a27ee-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="a27ee-183">Par exemple, « 5.2.3790 » pour Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a27ee-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="a27ee-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="a27ee-185">Chaîne qui représente l’architecture du processeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a27ee-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="a27ee-186">Pour obtenir la liste des valeurs, consultez le membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="a27ee-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="a27ee-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="a27ee-188">Chaîne qui représente le type de produit.</span><span class="sxs-lookup"><span data-stu-id="a27ee-188">A string that represents the product type.</span></span> <span data-ttu-id="a27ee-189">Pour obtenir la liste des valeurs, consultez le membre **wProductType** de la structure [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a27ee-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="a27ee-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="a27ee-191">Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv4 que la pile RDP de l’ordinateur virtuel invité écoute actuellement.</span><span class="sxs-lookup"><span data-stu-id="a27ee-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="a27ee-192">Si la pile RDP n’est pas en cours d’exécution, la chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="a27ee-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="a27ee-193">La liste est automatiquement mise à jour chaque fois qu’une modification de la configuration TCP/IP affecte la pile RDP sur la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="a27ee-194">Chaque adresse est représentée sous la forme d’une notation décimale à points.</span><span class="sxs-lookup"><span data-stu-id="a27ee-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="a27ee-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="a27ee-196">Chaîne qui contient une liste délimitée par des points-virgules des adresses IPv6 sur lesquelles la pile RDP d’ordinateur virtuel invité écoute actuellement.</span><span class="sxs-lookup"><span data-stu-id="a27ee-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="a27ee-197">Si la pile RDP n’est pas en cours d’exécution, la chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="a27ee-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="a27ee-198">La liste est automatiquement mise à jour chaque fois qu’une modification de la configuration TCP/IP affecte la pile RDP sur la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="a27ee-199">Chaque adresse est représentée en notation hexadécimale à deux-points.</span><span class="sxs-lookup"><span data-stu-id="a27ee-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="a27ee-200"><dt>"ServicePackMajor"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="a27ee-201">Chaîne qui représente le numéro de version principale du dernier Service Pack installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="a27ee-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="a27ee-202"><dt>"ServicePackMinor"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="a27ee-203">Chaîne qui représente le numéro de version mineure de la dernière Service Pack installée sur le système.</span><span class="sxs-lookup"><span data-stu-id="a27ee-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="a27ee-204"><dt>"SuiteMask"</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="a27ee-205">Chaîne qui représente les suites de produits disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="a27ee-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="a27ee-206">Cette chaîne est une combinaison de l’une des valeurs du membre **wSuiteMask** de la structure [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a27ee-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="a27ee-207">**Source**</span><span class="sxs-lookup"><span data-stu-id="a27ee-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a27ee-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a27ee-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a27ee-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a27ee-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a27ee-210">Source des données.</span><span class="sxs-lookup"><span data-stu-id="a27ee-210">The source of the data.</span></span>



| <span data-ttu-id="a27ee-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="a27ee-211">Value</span></span>                                                                        | <span data-ttu-id="a27ee-212">Signification</span><span class="sxs-lookup"><span data-stu-id="a27ee-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a27ee-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a27ee-214">« HostExchangeItems » en cas de push par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a27ee-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="a27ee-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a27ee-216">« GuestExchangeItems » en cas de push par l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="a27ee-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="a27ee-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a27ee-218">« GuestIntrinsicExchangeItems » lorsqu’il est automatiquement rempli par la machine virtuelle invitée.</span><span class="sxs-lookup"><span data-stu-id="a27ee-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="a27ee-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="a27ee-220">Indique que l’élément est uniquement un hôte et qu’il n’est pas partagé avec l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="a27ee-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="a27ee-221">Utilisé avec la propriété **HostOnlyItems** de la [**classe \_ KvpExchangeComponentSettingData MSVM**](msvm-kvpexchangecomponentsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a27ee-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a27ee-222">Notes</span><span class="sxs-lookup"><span data-stu-id="a27ee-222">Remarks</span></span>

<span data-ttu-id="a27ee-223">L’accès à la classe **MSVM \_ KvpExchangeDataItem** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a27ee-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a27ee-224">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a27ee-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a27ee-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a27ee-225">Requirements</span></span>



| <span data-ttu-id="a27ee-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a27ee-226">Requirement</span></span> | <span data-ttu-id="a27ee-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="a27ee-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a27ee-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a27ee-228">Minimum supported client</span></span><br/> | <span data-ttu-id="a27ee-229">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a27ee-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a27ee-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a27ee-230">Minimum supported server</span></span><br/> | <span data-ttu-id="a27ee-231">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a27ee-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a27ee-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a27ee-232">Namespace</span></span><br/>                | <span data-ttu-id="a27ee-233">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a27ee-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a27ee-234">MOF</span><span class="sxs-lookup"><span data-stu-id="a27ee-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a27ee-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a27ee-236">DLL</span><span class="sxs-lookup"><span data-stu-id="a27ee-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a27ee-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a27ee-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a27ee-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a27ee-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a27ee-239">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a27ee-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="a27ee-240">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a27ee-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

