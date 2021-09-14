---
description: à partir de Windows Vista, wmi contient de nombreuses nouvelles fonctionnalités basées sur les demandes des utilisateurs WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: nouveautés de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918680"
---
# <a name="whats-new-in-windowsvista"></a>nouveautés de Windows Vista

à partir de Windows Vista, wmi contient de nombreuses nouvelles fonctionnalités basées sur les demandes des utilisateurs WMI.

-   [Nouvel outil de dépannage](#new-troubleshooting-tool)
-   [nouvelles fonctionnalités de sécurité dans Windows Vista](#new-security-features-in-windows-vista)
-   [autres nouvelles fonctionnalités de Windows Vista](#other-new-features-in-windows-vista)
-   [Rubriques connexes](#related-topics)

## <a name="new-troubleshooting-tool"></a>Nouvel outil de dépannage

Un nouvel outil de dépannage est disponible au téléchargement.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility
</dt> <dd>

Cet utilitaire examine l’état actuel du service WMI et les composants associés, les paramètres DCOM et les paramètres du Registre sur l’ordinateur local. L’utilitaire signale des problèmes et propose des suggestions de réparation. pour plus d’informations et pour télécharger l’utilitaire, consultez [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>nouvelles fonctionnalités de sécurité dans Windows Vista

la liste suivante répertorie les nouvelles fonctionnalités de sécurité WMI disponibles dans Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Suivi et journalisation des événements
</dt> <dd>

Le service WMI n’utilise plus la plupart des [fichiers journaux WMI](wmi-log-files.md). Au lieu de cela, il utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements sont disponibles par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Wevtutil. Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Définition de la sécurité de l’espace de noms WMI dans le fichier MOF
</dt> <dd>

Le qualificateur **NamespaceSecuritySDDL** peut être utilisé pour sécuriser tout espace de noms. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Audit de sécurité des espaces de noms WMI
</dt> <dd>

WMI utilise les listes de contrôle d’accès système (SACL) pour auditer l’activité de l’espace de noms et signaler les événements dans le journal des événements de sécurité. Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md) et [définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obtenir et définir des méthodes de descripteur de sécurité pour les objets sécurisables
</dt> <dd>

De nouvelles méthodes scriptables pour obtenir et définir des descripteurs de sécurité ont été ajoutées à l' [**\_ imprimante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), au [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service), à [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), à [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)et à [**\_ \_ SystemSecurity**](--systemsecurity.md). Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipuler des descripteurs de sécurité dans des scripts
</dt> <dd>

La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) a des méthodes qui permettent aux scripts de convertir les descripteurs de sécurité binaires des objets sécurisables en objets [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou en chaînes du [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Contrôle de compte d’utilisateur
</dt> <dd>

Le contrôle de compte d’utilisateur (UAC) affecte les données WMI retournées, l’accès à distance et la façon dont les scripts doivent être exécutés. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md). pour plus d’informations sur UAC, consultez [Prise en main avec le contrôle de compte d’utilisateur sur Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>autres nouvelles fonctionnalités de Windows Vista

la liste suivante répertorie les nouvelles fonctionnalités WMI disponibles dans Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nouveaux fournisseurs de données de compteurs de performances
</dt> <dd>

Le processus AutoDiscovery/AutoPurge (ADAP) ne transfère plus les objets de compteur de performance dans les classes de performance WMI de l’espace de stockage WMI. Pour plus d’informations, consultez [bibliothèques de performances et WMI](performance-libraries-and-wmi.md). Le [fournisseur wmiperfclass](wmiperfclass-provider.md) crée les classes de compteur de performance WMI. Les données sont fournies dynamiquement par le [fournisseur WMIPerfInst](wmiperfinst-provider.md)à ces classes de performance WMI.

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexeur pour les collections
</dt> <dd>

La méthode [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) retourne l’objet associé à un index spécifié dans une collection.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Prise en charge D’ipv6 et IPv4
</dt> <dd>

Le [fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI et les classes de réseau fournissent des données pour les adresses IPv4. depuis Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6. Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Modifications apportées aux connexions à distance
</dt> <dd>

la connexion à un espace de noms WMI sur un ordinateur distant exécutant Windows Vista peut nécessiter des modifications des paramètres pour [Windows pare-feu](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [le contrôle de compte d’utilisateur](/previous-versions/aa905108(v=msdn.10))ou DCOM. Pour plus d’informations, consultez [connexion à WMI à distance à partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Modifications apportées à [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

pour les systèmes qui s’exécutent sur le système d’exploitation Windows Vista et versions ultérieures, cette classe retourne uniquement les mises à jour fournies par la fonction de maintenance basée sur les composants (CBS). Ces mises à jour ne sont pas répertoriées dans le registre. les mises à jour fournies par Windows Installer (MSI) ou le [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) ne sont pas retournées par [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Activation et désactivation d’une carte réseau
</dt> <dd>

[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) dispose de nouvelles méthodes pour activer et désactiver la carte réseau.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Modifications du fournisseur de programme d’installation
</dt> <dd>

[**Win32 \_ Le produit**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) a de nouvelles propriétés et méthodes pour fournir des données supplémentaires sur le produit.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nouvelles classes de moniteur d’affichage
</dt> <dd>

Les [classes d’affichage de surveillance](/windows/desktop/WmiCoreProv/wmi-core-provider-) contiennent des données fournies par le [fournisseur WDM](/windows/desktop/WmiCoreProv/wdm-provider) qui fournit des données sur les moniteurs d’affichage.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Fournisseur d’interface de gestion de plateforme intelligente
</dt> <dd>

Le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI fournit des données à partir des opérations du contrôleur de gestion de la carte de configuration (BMC) au système d’exploitation. Le fournisseur fournit des informations aux classes d’informations de gestion de plateforme intelligentes, qui fournissent des données de capteurs et des données de message du journal des événements système (SEL) BMC.

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Détection des hyperthreads et processeurs multicœurs
</dt> <dd>

[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) Le processeur ComputerSystem et le [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor) possèdent de nouvelles propriétés qui vous permettent d’écrire des scripts pour déterminer si le système informatique dispose de processeurs multicœur ou hyperthreading.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Messages d’événement
</dt> <dd>

Windows Vista a de nouveaux messages d’événement. Pour plus d’informations, consultez [événements WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Améliorations de l’inventaire
</dt> <dd>

De nombreuses classes de matériel ont subi des modifications pour améliorer l’inventaire matériel. Par exemple, une propriété de numéro de série a été ajoutée à [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) et [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nouveaux modèles d’hébergement de fournisseur
</dt> <dd>

de nouveaux modèles d’hébergement de fournisseur ont été ajoutés pour Windows Vista. Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 
