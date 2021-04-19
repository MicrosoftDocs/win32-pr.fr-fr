---
description: À compter de Windows Vista, WMI contient de nombreuses nouvelles fonctionnalités basées sur les demandes des utilisateurs WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Nouveautés de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522214"
---
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="44076-103">Nouveautés de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44076-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="44076-104">À compter de Windows Vista, WMI contient de nombreuses nouvelles fonctionnalités basées sur les demandes des utilisateurs WMI.</span><span class="sxs-lookup"><span data-stu-id="44076-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="44076-105">Nouvel outil de dépannage</span><span class="sxs-lookup"><span data-stu-id="44076-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="44076-106">Nouvelles fonctionnalités de sécurité dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44076-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="44076-107">Autres nouvelles fonctionnalités de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44076-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="44076-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44076-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="44076-109">Nouvel outil de dépannage</span><span class="sxs-lookup"><span data-stu-id="44076-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="44076-110">Un nouvel outil de dépannage est disponible au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="44076-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="44076-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span><span class="sxs-lookup"><span data-stu-id="44076-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="44076-112">Cet utilitaire examine l’état actuel du service WMI et les composants associés, les paramètres DCOM et les paramètres du Registre sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="44076-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="44076-113">L’utilitaire signale des problèmes et propose des suggestions de réparation.</span><span class="sxs-lookup"><span data-stu-id="44076-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="44076-114">Pour plus d’informations et pour télécharger l’utilitaire, consultez [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="44076-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="44076-115">Nouvelles fonctionnalités de sécurité dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44076-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="44076-116">La liste suivante répertorie les nouvelles fonctionnalités de sécurité WMI disponibles dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44076-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="44076-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Suivi et journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="44076-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="44076-118">Le service WMI n’utilise plus la plupart des [fichiers journaux WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="44076-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="44076-119">Au lieu de cela, il utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements sont disponibles par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="44076-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="44076-120">Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="44076-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Définition de la sécurité de l’espace de noms WMI dans le fichier MOF</span><span class="sxs-lookup"><span data-stu-id="44076-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="44076-122">Le qualificateur **NamespaceSecuritySDDL** peut être utilisé pour sécuriser tout espace de noms.</span><span class="sxs-lookup"><span data-stu-id="44076-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="44076-123">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="44076-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Audit de sécurité des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="44076-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="44076-125">WMI utilise les listes de contrôle d’accès système (SACL) pour auditer l’activité de l’espace de noms et signaler les événements dans le journal des événements de sécurité.</span><span class="sxs-lookup"><span data-stu-id="44076-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="44076-126">Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md) et [définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="44076-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obtenir et définir des méthodes de descripteur de sécurité pour les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="44076-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="44076-128">De nouvelles méthodes scriptables pour obtenir et définir des descripteurs de sécurité ont été ajoutées à l' [**\_ imprimante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), au [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service), à [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), à [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)et à [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="44076-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="44076-129">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="44076-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipuler des descripteurs de sécurité dans des scripts</span><span class="sxs-lookup"><span data-stu-id="44076-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="44076-131">La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) a des méthodes qui permettent aux scripts de convertir les descripteurs de sécurité binaires des objets sécurisables en objets [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou en chaînes du [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="44076-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="44076-132">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="44076-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="44076-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="44076-134">Le contrôle de compte d’utilisateur (UAC) affecte les données WMI retournées, l’accès à distance et la façon dont les scripts doivent être exécutés.</span><span class="sxs-lookup"><span data-stu-id="44076-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="44076-135">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="44076-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="44076-136">Pour plus d’informations sur UAC, consultez [prise en main avec le contrôle de compte d’utilisateur sur Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="44076-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="44076-137">Autres nouvelles fonctionnalités de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44076-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="44076-138">La liste suivante répertorie les nouvelles fonctionnalités WMI disponibles dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44076-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="44076-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nouveaux fournisseurs de données de compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="44076-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="44076-140">Le processus AutoDiscovery/AutoPurge (ADAP) ne transfère plus les objets de compteur de performance dans les classes de performance WMI de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="44076-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="44076-141">Pour plus d’informations, consultez [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="44076-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="44076-142">Le [fournisseur wmiperfclass](wmiperfclass-provider.md) crée les classes de compteur de performance WMI.</span><span class="sxs-lookup"><span data-stu-id="44076-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="44076-143">Les données sont fournies dynamiquement par le [fournisseur WMIPerfInst](wmiperfinst-provider.md)à ces classes de performance WMI.</span><span class="sxs-lookup"><span data-stu-id="44076-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexeur pour les collections</span><span class="sxs-lookup"><span data-stu-id="44076-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="44076-145">La méthode [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) retourne l’objet associé à un index spécifié dans une collection.</span><span class="sxs-lookup"><span data-stu-id="44076-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="44076-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Prise en charge D’ipv6 et IPv4</span><span class="sxs-lookup"><span data-stu-id="44076-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="44076-147">Le [fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI et les classes de réseau fournissent des données pour les adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="44076-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="44076-148">À compter de Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="44076-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="44076-149">Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="44076-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Modifications apportées aux connexions à distance</span><span class="sxs-lookup"><span data-stu-id="44076-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="44076-151">La connexion à un espace de noms WMI sur un ordinateur distant exécutant Windows Vista peut nécessiter des modifications des paramètres du [pare-feu Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), du [contrôle de compte d’utilisateur](/previous-versions/aa905108(v=msdn.10))ou de DCOM.</span><span class="sxs-lookup"><span data-stu-id="44076-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="44076-152">Pour plus d’informations, consultez [connexion à WMI à distance à partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="44076-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Modifications apportées à [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="44076-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="44076-154">Pour les systèmes qui s’exécutent sur le système d’exploitation Windows Vista et versions ultérieures, cette classe retourne uniquement les mises à jour fournies par la fonction de maintenance basée sur les composants (CBS).</span><span class="sxs-lookup"><span data-stu-id="44076-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="44076-155">Ces mises à jour ne sont pas répertoriées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="44076-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="44076-156">Les mises à jour fournies par Windows Installer (MSI) ou le [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) ne sont pas retournées par [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span><span class="sxs-lookup"><span data-stu-id="44076-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="44076-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Activation et désactivation d’une carte réseau</span><span class="sxs-lookup"><span data-stu-id="44076-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="44076-158">[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) dispose de nouvelles méthodes pour activer et désactiver la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="44076-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="44076-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Modifications du fournisseur de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="44076-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="44076-160">[**Win32 \_ Le produit**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) a de nouvelles propriétés et méthodes pour fournir des données supplémentaires sur le produit.</span><span class="sxs-lookup"><span data-stu-id="44076-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="44076-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nouvelles classes de moniteur d’affichage</span><span class="sxs-lookup"><span data-stu-id="44076-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="44076-162">Les [classes d’affichage de surveillance](/windows/desktop/WmiCoreProv/wmi-core-provider-) contiennent des données fournies par le [fournisseur WDM](/windows/desktop/WmiCoreProv/wdm-provider) qui fournit des données sur les moniteurs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="44076-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="44076-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Fournisseur d’interface de gestion de plateforme intelligente</span><span class="sxs-lookup"><span data-stu-id="44076-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="44076-164">Le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI fournit des données à partir des opérations du contrôleur de gestion de la carte de configuration (BMC) au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="44076-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="44076-165">Le fournisseur fournit des informations aux classes d’informations de gestion de plateforme intelligentes, qui fournissent des données de capteurs et des données de message du journal des événements système (SEL) BMC.</span><span class="sxs-lookup"><span data-stu-id="44076-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="44076-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Détection des hyperthreads et processeurs multicœurs</span><span class="sxs-lookup"><span data-stu-id="44076-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="44076-167">[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) Le processeur ComputerSystem et le [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor) possèdent de nouvelles propriétés qui vous permettent d’écrire des scripts pour déterminer si le système informatique dispose de processeurs multicœur ou hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="44076-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="44076-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Messages d’événement</span><span class="sxs-lookup"><span data-stu-id="44076-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="44076-169">Windows Vista comporte de nouveaux messages d’événement.</span><span class="sxs-lookup"><span data-stu-id="44076-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="44076-170">Pour plus d’informations, consultez [événements WMI](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="44076-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="44076-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Améliorations de l’inventaire</span><span class="sxs-lookup"><span data-stu-id="44076-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="44076-172">De nombreuses classes de matériel ont subi des modifications pour améliorer l’inventaire matériel.</span><span class="sxs-lookup"><span data-stu-id="44076-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="44076-173">Par exemple, une propriété de numéro de série a été ajoutée à [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) et [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span><span class="sxs-lookup"><span data-stu-id="44076-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="44076-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nouveaux modèles d’hébergement de fournisseur</span><span class="sxs-lookup"><span data-stu-id="44076-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="44076-175">De nouveaux modèles d’hébergement de fournisseur ont été ajoutés pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44076-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="44076-176">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="44076-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="44076-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44076-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44076-178">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="44076-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
