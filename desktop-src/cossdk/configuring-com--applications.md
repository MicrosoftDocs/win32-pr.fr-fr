---
description: Une application COM+ est essentiellement une construction déclarative qui vous permet de configurer un nombre quelconque de composants en commun. Par exemple, vous pouvez configurer les composants d’une application avec une stratégie de sécurité commune.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configuration des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372d15e00898d88b3aed13ca2edaa03bc8a666ceb62dc1389af3e8f6959c971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916929"
---
# <a name="configuring-com-applications"></a>Configuration des applications COM+

Une application COM+ est essentiellement une construction déclarative qui vous permet de configurer un nombre quelconque de composants en commun. Par exemple, vous pouvez configurer les composants d’une application avec une stratégie de sécurité commune.

La configuration est un élément essentiel du processus de développement pour les applications COM+. La façon dont vous configurez une application détermine la façon dont COM+ fournit des services pour celle-ci et comment elle se comporte quand elle est exécutée.

Vous pouvez configurer des applications COM+ à l’aide de l’outil d’administration Services de composants ou des objets et interfaces d’administration pouvant faire l’objet d’un script qui fournissent la fonctionnalité sous-jacente de l’outil d’administration. Pour plus d’informations sur l’exécution de l’administration par script, consultez automatisation de l' [administration com+](automating-com--administration.md).

Vous pouvez configurer des éléments aux niveaux suivants dans les applications COM+ :

-   [Paramètres au niveau de l’Application](#application-level-settings)
-   [Paramètres au niveau du composant (au niveau de la classe)](#component-level-class-level-settings)
-   [Paramètre au niveau de l’interface](#interface-level-setting)
-   [Paramètre au niveau de la méthode](#method-level-setting)
-   [Rubriques connexes](#related-topics)

La façon dont vous installez les composants dans une application peut affecter la façon dont vous pouvez les configurer. Vous devez toujours installer les composants dans des applications COM+ (au lieu de les importer). L’installation des composants les enregistre entièrement, ainsi que les interfaces et les bibliothèques de types, dans la base de données d’inscription de classe COM+ (RegDB) afin que vous puissiez les configurer.

## <a name="application-level-settings"></a>Application-Level Paramètres



| Attribut                                                                                        | Description                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Activation](context-activation.md)<br/>                                                  | Spécifie le type d’application : application serveur ou application de bibliothèque.<br/>                                                                                                            |
| [Activation des vérifications d’accès](enabling-access-checks-for-an-application.md)<br/>               | Active et désactive la vérification de la sécurité.<br/>                                                                                                                                                      |
| [Niveau de sécurité](setting-a-security-level-for-access-checks.md)<br/>                      | Spécifie que les contrôles d’accès seront effectués au niveau du processus (niveaux de contrôle d’accès générés à partir des rôles) ou à la fois au niveau du processus et au niveau du composant (sécurité complète basée sur les rôles).<br/> |
| [Niveau d'authentification](setting-an-authentication-level-for-a-server-application.md)<br/>  | Définit le niveau d’authentification utilisé pour les appels dans l’application.<br/>                                                                                                                        |
| [Niveau d’emprunt d’identité](setting-an-impersonation-level.md)<br/>                             | Définit le niveau d’emprunt d’identité utilisé pour les appels à d’autres applications.<br/>                                                                                                                        |
| [Queuing](creating-queuable-components.md)<br/>                                           | Spécifie que les composants de l’application utiliseront les services de mise en file d’attente.<br/>                                                                                                                         |
| [Activer CRM](configuring-com--crm-components.md)<br/>                                     | Permet l’utilisation de gestionnaires de ressources de compensation.<br/>                                                                                                                                           |
| [Exécuter l’application en tant que service](com--applications-running-as-service-applications.md)<br/> | Configure et implémente une application serveur COM+ en tant que service NT.<br/>                                                                                                                    |
| [Service SOAP COM+](com--soap-service.md)<br/>                                            | Expose une application COM+ en tant que service Web XML.<br/>                                                                                                                                        |
| [Regroupement d’applications](com--application-pooling.md)<br/>                                   | Ajoute l’extensibilité pour les processus monothread et s’intègre au service de recyclage des applications COM+.<br/>                                                                               |
| [Recyclage d’applications](com--application-recycling.md)<br/>                               | Augmente la stabilité de l’application en arrêtant en douceur un processus associé à une application et en le redémarrant.<br/>                                                                  |
| [Vidage de processus](what-s-new-in-com--1-5.md)<br/>                                         | Vide la totalité de l’état d’un processus sans l’arrêter, à des fins de débogage.<br/>                                                                                                      |
| Arrêt du processus serveur<br/>                                                               | Arrête un processus après une période d’inactivité spécifiée.<br/>                                                                                                                                      |
| Autorisations<br/>                                                                           | Désactive les modifications apportées aux paramètres de configuration, y compris la suppression.<br/>                                                                                                                          |
| Identité de sécurité<br/>                                                                     | Spécifie l’identité sous laquelle l’application s’exécute.<br/>                                                                                                                                 |
| Lancer dans le débogueur<br/>                                                                    | Spécifie que l’application sera lancée dans un débogueur, avec les paramètres de ligne de commande spécifiés par l’utilisateur.<br/>                                                                                |
| Activer la prise en charge de 3 Go<br/>                                                                    | Permet l’utilisation de l’espace d’adressage de mémoire de processus étendu.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level (au niveau de la classe) Paramètres



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transactions</a><br/></td>
<td>Définit les spécifications automatiques des transactions désactivées, non prises en charge, prises en charge, obligatoires ou nouvelles.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Synchronisation</a><br/></td>
<td>Définit les exigences de synchronisation désactivées, non prises en charge, prises en charge, obligatoires ou nouvelles.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">Activation juste-à-temps</a><br/></td>
<td>Active l’activation juste-à-temps.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Mise en pool d’objets</a><br/></td>
<td>Active le regroupement d’objets. La taille minimale et maximale du pool et les valeurs de délai d’attente des objets sont configurables.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Construction d’objets</a><br/></td>
<td>Active la construction d’objets paramétrables avec une chaîne de constructeur spécifiée administrativement. <br/>
<blockquote>
[!Note]<br />
La chaîne du constructeur ne doit pas être utilisée pour stocker des informations sensibles à la sécurité.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Contrôles d’accès au niveau du composant</a><br/></td>
<td>Active ou désactive la vérification de la sécurité basée sur les rôles au niveau du composant.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Attribution de rôle déclarative</a><br/></td>
<td>Active l’attribution explicite des rôles au composant.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Classe d’exceptions de mise en file d’attente</a><br/></td>
<td>Indique une classe d’exception pour la gestion des échecs côté client.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Statistiques et événements d’instrumentation</a><br/></td>
<td>Active la création de rapports détaillés sur les événements système et les statistiques d’objets.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Contexte d’activation</a><br/></td>
<td>Active l’activation forcée d’un objet dans le contexte de l’appelant ou le contexte par défaut.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Création de composants privés</a><br/></td>
<td>Marque le composant comme privé pour l’application. Un composant privé peut être vu et activé uniquement par d’autres composants de la même application.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Paramètre Interface-Level



| Attribut                                                                                           | Description                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Mis en file d'attente.](creating-queuable-components.md)<br/>                                               | Indique une interface de mise en file d’attente, définie dans IDL.<br/>                                                                       |
| [Attribution de rôle déclarative](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Active l’attribution explicite des rôles à l’interface, ainsi que les rôles hérités implicitement à partir du niveau du composant.<br/> |



 

## <a name="method-level-setting"></a>Paramètre Method-Level



| Attribut                                                                                           | Description                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminé automatiquement](enabling-auto-done-for-a-method.md)<br/>                                         | Désactive automatiquement l’objet sur le retour de la méthode et vote dans la transaction.<br/>                                                       |
| [Attribution de rôle déclarative](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Active l’attribution explicite des rôles à la méthode ainsi que les rôles hérités implicitement des niveaux interface et composant.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Automatisation de l’administration COM+](automating-com--administration.md)
</dt> <dt>

[Création d’applications COM+](creating-com--applications.md)
</dt> <dt>

[Déploiement d’applications COM+](deploying-com--applications.md)
</dt> </dl>

 

 




