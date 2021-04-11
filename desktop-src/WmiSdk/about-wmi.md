---
description: WMI est l’implémentation Microsoft de WBEM (Web-Based Enterprise Management), qui est une initiative de l’industrie pour développer une technologie standard permettant d’accéder aux informations de gestion dans un environnement d’entreprise.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: À propos de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320342"
---
# <a name="about-wmi"></a>À propos de WMI

WMI est l’implémentation Microsoft de WBEM (Web-Based Enterprise Management), qui est une initiative de l’industrie pour développer une technologie standard permettant d’accéder aux informations de gestion dans un environnement d’entreprise. WMI utilise la norme industrielle CIM (Common Information Model) pour représenter les systèmes, applications, réseaux, périphériques et autres composants managés. Le modèle CIM est développé et géré par la[DMTF](https://www.dmtf.org/standards/wsman)(Distributed Management Task Force).

> [!Note]  
> La nouvelle génération de WMI, connue sous le nom d’infrastructure de gestion Windows (MI), est actuellement disponible. MI est entièrement compatible avec les versions précédentes de WMI et fournit un hôte de fonctionnalités et d’avantages qui facilitent la conception et le développement de fournisseurs et de clients. Par exemple, de nombreux fournisseurs plus récents sont écrits à l’aide de MI Framework, mais ils sont accessibles à l’aide de scripts et d’applications WMI. Pour plus d’informations sur les différences entre les deux technologies, consultez [Pourquoi utiliser mi ?](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Gestion des systèmes d’ordinateurs distants avec WMI

WMI permet d’obtenir des données de gestion d’ordinateurs distants. Les connexions WMI à distance sont effectuées via DCOM. Une alternative consiste à utiliser Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)), qui obtient les données de gestion WMI à distance à l’aide du protocole basé sur SOAP WS-Management.

## <a name="programming-with-wmi"></a>Programmation avec WMI

Les applications de gestion ou les scripts peuvent obtenir des données ou effectuer des opérations via WMI dans différents langages. Pour plus d’informations, consultez la section audience pour les développeurs dans [Windows Management Instrumentation](wmi-start-page.md).

De nombreuses fonctionnalités de Windows ont des fournisseurs WMI associés, comme le [fournisseur données de configuration de démarrage (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) ou le [fournisseur de volume de stockage](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). Les fournisseurs WMI implémentent la fonctionnalité décrite par les méthodes et propriétés des classes WMI pour gérer les fonctionnalités Windows associées. Pour plus d’informations, consultez [fournisseurs WMI](wmi-providers.md) et [classes WMI](wmi-classes.md).

Pour plus d’informations sur la façon d’écrire un fournisseur pour fournir des données à partir de nouveaux matériels ou applications, consultez la page [fourniture de données à WMI](providing-data-to-wmi.md).

Pour plus d’informations sur l’implémentation de cette technologie, consultez [utilisation de WMI](using-wmi.md).

Le tableau suivant répertorie les rubriques incluses dans cette section.



| Section                                                                                                | Description                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveautés de WMI](what-s-new-in-wmi.md)                                                             | Nouvelles fonctionnalités de WMI.                                                                                                                                                                                                                              |
| [Disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md) | Certains composants ne sont plus disponibles ou sont disponibles en tant qu’installation facultative.                                                                                                                                                             |
| [Architecture WMI](wmi-architecture.md)                                                               | Une application de gestion communique avec WMI à l’aide d’une variété d’interfaces, telles que Visual Basic, C++, ODBC et ActiveX. Toutes les interfaces WMI sont basées sur le modèle COM (Component Object Model).                                              |
| [Common Information Model (CIM)](common-information-model.md)                                               | Modèle de programmation indépendant du langage qui utilise des techniques orientées objet pour décrire une entreprise.                                                                                                                                          |
| [Format MOF (Managed Object Format)](managed-object-format--mof-.md)                                               | Format qui vous permet de créer du code lisible par l’homme, que le système d’exploitation peut traduire en un ensemble de classes CIM. Vous pouvez utiliser les nouvelles classes pour modéliser et contrôler les nouvelles technologies d’une entreprise.                                 |
| [Contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md)                                       | Le contrôle de compte d’utilisateur (UAC) affecte les données WMI retournées, l’accès à distance et la façon dont les scripts doivent être exécutés. Pour plus d’informations, consultez [prise en main avec le contrôle de compte d’utilisateur sur Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md)                                 | WMI utilise des procédures et des objets de sécurité Windows standard pour contrôler et protéger l’accès aux objets sécurisables tels que les espaces de noms WMI, les imprimantes, les services et les applications DCOM.                                                                      |
| [Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)                                     | Les données des compteurs de performances système sont disponibles dans les classes WMI.                                                                                                                                                                            |
| [Prise en charge D’ipv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | Le [fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI et les classes de réseau fournissent des données pour les adresses IPv4. À compter de Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.                                       |
| [Format de date et d’heure](date-and-time-format.md)                                                       | WMI utilise les formats de date et d’heure définis par la spécification CIM de la force de gestion distribuée. Pour plus d’informations, consultez [DMTF](https://www.dmtf.org/).                                                          |
| [Écriture de scripts pour l’accès à WMI](scripting-access-to-wmi.md)                                                 | Écrire des scripts WMI pour effectuer des tâches de gestion.                                                                                                                                                                                                    |
| [Résolution des problèmes WMI](wmi-troubleshooting.md)                                                         | Lors de l’accès aux données WMI locales ou distantes dans une application ou un script, vous pouvez recevoir des erreurs allant des classes manquantes à l’accès refusé. Des options de débogage et des classes de dépannage sont également disponibles pour les fournisseurs.                           |
| [Informations complémentaires](further-information.md)                                                         | Sites Web, ouvrages et articles sur WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> <dt>

[Référence WMI](wmi-reference.md)
</dt> </dl>

 

 
