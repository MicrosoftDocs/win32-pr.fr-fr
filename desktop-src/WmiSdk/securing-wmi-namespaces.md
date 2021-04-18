---
description: L’accès aux espaces de noms WMI et à leurs données est contrôlé par les descripteurs de sécurité.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sécurisation des espaces de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519020"
---
# <a name="securing-wmi-namespaces"></a>Sécurisation des espaces de noms WMI

L’accès aux espaces de noms WMI et à leurs données est contrôlé par les [*descripteurs de sécurité*](gloss-s.md). Vous pouvez protéger les données de vos [*espaces de noms*](gloss-n.md) en ajustant le descripteur de sécurité de l’espace de noms pour contrôler qui a accès aux données et aux méthodes. Pour plus d’informations, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).


Les rubriques suivantes décrivent la sécurité de l’espace de noms WMI et expliquent comment contrôler l’accès aux espaces de noms.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> <dd>

La sécurité des espaces de noms WMI repose sur des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) d’utilisateur Windows standard et des listes de contrôle d’accès. Les administrateurs et les utilisateurs ont des autorisations par défaut différentes.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md)
</dt> <dd>

Une fois qu’un espace de noms existe dans le référentiel WMI, vous pouvez modifier la sécurité de l’espace de noms à l’aide du contrôle WMI ou en appelant les méthodes de [**\_ \_ SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Le qualificateur **RequiresEncryption** sur un espace de noms exige que le script ou l’application cliente WMI utilise le niveau d’authentification qui chiffre les appels de procédure distante. Les demandes de données entrantes et les rappels asynchrones doivent être chiffrés.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Établissement de l’héritage de la sécurité des espaces de noms](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Création d’un espace de noms avec l’API WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
