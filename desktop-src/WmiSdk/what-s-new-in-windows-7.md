---
description: Nouveautés de Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Nouveautés de Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530778"
---
# <a name="whats-new-in-windows-7"></a>Nouveautés de Windows 7

## <a name="new-security-feature-in-windows-7"></a>Nouvelle fonctionnalité de sécurité dans Windows 7

La liste suivante répertorie la nouvelle fonctionnalité de sécurité de l’Windows Management Instrumentation (WMI) qui est disponible dans Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Contrôle de la sécurité du fournisseur
</dt> <dd>

Modifications pour améliorer la sécurité du processus hôte du fournisseur partagé WMI (wmiprvse.exe). Ces modifications introduisent trois nouvelles stratégies de groupe et deux modes d’exécution pour l’hôte partagé WMI, qui sont appelés modes sécurisé et compatible. Pour plus d’informations, consultez [clés de Registre pour le contrôle de la sécurité du fournisseur](registry-keys-for-controlling-provider-security-.md).

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Autres fonctionnalités nouvelles ou mises à jour dans Windows 7

La liste suivante répertorie les nouvelles fonctionnalités WMI disponibles dans Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilité du schéma CIM
</dt> <dd>

À compter de Windows 7, WMI est compatible avec la version de schéma Common Information Model (CIM) 2.17.1. Pour plus d’informations, consultez [compatibilité du schéma CIM](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Traversée d’association entre espaces de noms
</dt> <dd>

WMI implémentait un mécanisme standard pour la découverte des profils à l’aide du schéma CIM. Pour plus d’informations, consultez [traversée des associations entre espaces de noms](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Fournisseurs d’associations
</dt> <dd>

Informations sur l’écriture et l’inscription d’un fournisseur d’association. Les fournisseurs d’associations sont utilisés pour exposer des profils standard, comme un profil d’alimentation. Pour plus d’informations, consultez [écriture d’un fournisseur d’associations pour l’interopérabilité](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>État des fonctionnalités facultatives
</dt> <dd>

WMI a implémenté la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Cette classe interroge et retourne l’état des fonctionnalités facultatives présentes sur un ordinateur. Pour obtenir des exemples de requêtes utilisant Windows PowerShell, consultez [interrogation de l’état des fonctionnalités facultatives](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Modification du comportement par défaut de la fonctionnalité de référentiel autorestauration
</dt> <dd>

WMI dispose d’une nouvelle clé de Registre pour activer ou désactiver la fonctionnalité de référentiel de restauration. Pour plus d’informations, consultez [clé de Registre pour la configuration du référentiel](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Nouvelles classes de commandes Windows PowerShell
</dt> <dd>

Les applets de commande Windows PowerShell permettent aux utilisateurs d’effectuer les tâches de bout en bout nécessaires à la gestion des ordinateurs locaux et distants. Pour plus d’informations, consultez [référence managée pour les classes de commande PowerShell WMI](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Nouveau mécanisme de connexion aux ordinateurs distants
</dt> <dd>

Windows PowerShell fournit un mécanisme simple pour se connecter à WMI sur un ordinateur distant. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant à l’aide de PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Modifications apportées aux classes de licences logicielles
</dt> <dd>

Les [classes de licences logicielles](/previous-versions/windows/desktop/sppwmi/software-license-provider-) ont de nouvelles méthodes et propriétés pour fournir davantage de données de licence logicielle. En outre, la classe [**SoftwareLicensingTokenActivationLicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) a été ajoutée.

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Nouvelles classes de contrôle d’alimentation et de budgétisation
</dt> <dd>

Les [classes de contrôle d’alimentation et de budgétisation](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) sont l’interface principale pour la requête d’informations de l’interface de contrôle d’alimentation (PMI) à partir des compteurs d’alimentation sous-jacents sur le système.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Nouvelles classes de stratégie d’alimentation
</dt> <dd>

Les [classes de stratégie d’alimentation](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) permettent la gestion à distance de toutes les infrastructures de stratégie d’alimentation.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Modifications apportées à la classe [**Win32 \_ ServerFeature**](win32-serverfeature.md)
</dt> <dd>

La propriété **ID** de l' [**\_ ServerFeature Win32**](win32-serverfeature.md) a été mise à jour.

</dd> </dl>

Pour plus d’informations sur les nouvelles fonctionnalités des versions précédentes du système d’exploitation, consultez [Nouveautés de Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 
