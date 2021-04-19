---
description: La sécurité WMI est axée sur la protection de l’accès aux données de l’espace de noms. WMI accorde d’abord l’accès aux groupes d’utilisateurs, comme spécifié par le contrôle WMI et les paramètres DCOM, puis les fournisseurs déterminent si l’utilisateur doit avoir accès aux données de l’espace de noms.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Maintenance de la sécurité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522109"
---
# <a name="maintaining-wmi-security"></a>Maintenance de la sécurité WMI

La sécurité WMI est axée sur la protection de l’accès aux données de l’espace de noms. WMI accorde d’abord l’accès aux groupes d’utilisateurs, comme spécifié par le [*contrôle WMI*](gloss-w.md) et les paramètres DCOM, puis les fournisseurs déterminent si l’utilisateur doit avoir accès aux données de l’espace de noms.

Les sections suivantes sont présentées dans cette rubrique :

-   [Sécurité des espaces de noms](#namespace-security)
-   [Paramètres de sécurité DCOM (Distributed Component Object Model).](#distributed-component-object-model-dcom-security-settings)
-   [WMI, hôtes de service partagés et authentification](#wmi-shared-service-hosts-and-authentication)
-   [Sécurité pour les scripts et les applications clients WMI](#security-for-wmi-client-scripts-and-applications)
-   [Rubriques connexes](#related-topics)

## <a name="namespace-security"></a>Sécurité des espaces de noms

La sécurité de l’espace de noms dépend des identificateurs de sécurité d’utilisateur Windows standard [*(SID)*](gloss-s.md) et du [*descripteur de sécurité*](gloss-s.md) pour l’espace de noms WMI.

Vous pouvez définir la sécurité de l’espace de noms en effectuant les actions suivantes :

-   Accordez ou refusez des droits d’accès à des espaces de noms pour les utilisateurs à l’aide du contrôle WMI ou lors de la création de l’espace de noms. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md) et [définition de la sécurité de l’espace de noms lorsque l’espace de noms est créé](setting-namespace-security-when-the-namespace-is-created.md).
-   Utilisez l’onglet sécurité du contrôle WMI pour établir un audit de sécurité. L’audit de sécurité génère des entrées de journal des événements lorsqu’un utilisateur échoue ou réussit dans une action auditée, telle que l’écriture de données dans un objet WMI ou la lecture du descripteur de sécurité. Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).
-   Utilisez le fichier MOF qui définit l’espace de noms pour demander à un utilisateur d’établir une connexion chiffrée. Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Paramètres de sécurité DCOM (Distributed Component Object Model).

La sécurité DCOM requiert un paramètre d’authentification et un paramètre d’emprunt d’identité. L’authentification signifie qu’un processus s’identifie à un autre. L’emprunt d’identité identifie l’autorité qu’un client accorde à un serveur pour appeler des processus différents. Au cours d’une vérification de sécurité, le serveur emprunte l’identité du client. Pour plus d’informations, consultez [sécurisation des clients et fournisseurs C++](securing-c---clients-and-providers.md) ou [sécurisation des clients de script](securing-scripting-clients.md).

Les scripts et les applications C/C++/C définissent les niveaux d’authentification et d’emprunt d’identité lorsqu’ils se connectent à un espace de noms WMI, ou ils utilisent les paramètres par défaut. Les connexions aux ordinateurs distants requièrent des paramètres différents de ceux des espaces de noms WMI sur l’ordinateur local. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, hôtes de service partagés et authentification

WMI réside dans un hôte de service partagé avec plusieurs autres services s’exécutant sous le compte NetworkService. Dans un processus Svchost, WMI partage la même authentification que les autres processus de l’hôte.

Les dll de fournisseur sont chargées dans des processus hôtes de service distincts de WMI. La propriété **HostingModel** de la classe système [**\_ \_ Win32Provider**](--win32provider.md) qui représente un fournisseur spécifie le compte système sous lequel le fournisseur s’exécute. La définition de cette propriété entraîne le chargement du fournisseur dans un processus hôte partagé qui a un niveau de privilège spécifié. Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Sécurité pour les scripts et les applications clients WMI

Les scripts et les applications doivent établir la sécurité appropriée pour se connecter aux espaces de noms WMI sur des ordinateurs locaux et distants. Pour plus d’informations, consultez [sécurisation des clients et fournisseurs C++](securing-c---clients-and-providers.md), [sécurisation des clients de script](securing-scripting-clients.md)et [sécurisation des événements WMI](securing-wmi-events.md).

Le tableau suivant répertorie les rubriques relatives à la maintenance de la sécurité WMI.



| Rubrique                                                                                              | Description                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)                                             | Vous pouvez limiter l’accès aux données de l’espace de noms aux utilisateurs autorisés par le biais du contrôle WMI.                                                                                      |
| [Sécurisation de votre fournisseur](securing-your-provider.md)                                               | Informations sur l’écriture de fournisseurs sécurisés.                                                                                                                           |
| [Sécurisation des clients et des fournisseurs C++](securing-c---clients-and-providers.md)                       | Les fournisseurs C++ et les applications clientes doivent effectuer la plupart des opérations pour maintenir la sécurité WMI.                                                         |
| [Sécurisation des clients de script](securing-scripting-clients.md)                                       | Les scripts et les applications Visual Basic (clients Automation) doivent définir une sécurité appropriée pour accéder aux données et aux événements WMI.                                        |
| [Sécurisation des événements WMI](securing-wmi-events.md)                                                     | Les événements WMI sont remis par le fournisseur d’événements à un consommateur temporaire ou permanent. Les événements sont remis sous la forme d’une instance d’une classe d’événements.               |
| [Modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md) | Avec les autorisations appropriées, vous pouvez appeler des méthodes sur les objets WMI qui représentent des objets sécurisables qui lisent ou modifient les descripteurs de sécurité sur des objets sécurisables. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

 



