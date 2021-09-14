---
description: La table ServiceInstall est utilisée pour installer un service et contient les colonnes suivantes.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Table ServiceInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230003"
---
# <a name="serviceinstall-table"></a>Table ServiceInstall

La table ServiceInstall est utilisée pour installer un service et contient les colonnes suivantes.



| Colonne         | Type                               | Clé | Nullable |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [Identificateur](identifier.md)       | O   | N        |
| Nom           | [Correct](formatted.md)         | N   | N        |
| DisplayName    | [Correct](formatted.md)         | N   | O        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Correct](formatted.md)         | N   | O        |
| Les dépendances   | [Correct](formatted.md)         | N   | O        |
| StartName      | [Correct](formatted.md)         | N   | O        |
| Mot de passe       | [Correct](formatted.md)         | N   | O        |
| Arguments      | [Correct](formatted.md)         | N   | O        |
| Composant\_    | [Identificateur](identifier.md)       | N   | N        |
| Description    | [Correct](formatted.md)         | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

Il s’agit de la clé primaire pour la table.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne est la chaîne qui donne le nom du service à installer. La chaîne a une longueur maximale de 256 caractères. La base de données du gestionnaire de contrôle des services conserve la casse des caractères dans le nom du service, mais les comparaisons de noms de service ne respectent pas la casse. Les barres obliques (/) et les barres obliques inverses ( \\ ) sont des caractères de nom de service non valides.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>NomComplet
</dt> <dd>

Cette colonne est la chaîne localisable que les programmes de l’interface utilisateur utilisent pour identifier le service. La chaîne a une longueur maximale de 256 caractères. Le gestionnaire de contrôle des services conserve la casse du nom complet, mais les comparaisons de noms d’affichage ne respectent pas la casse.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

Cette colonne est un jeu d’indicateurs binaires qui spécifient le type de service. L’un des types de service suivants doit être spécifié dans cette colonne.



| Type de service                | Valeur      | Description                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Processus propre à Win32 de service \_   | 0x00000010 | Service Microsoft Win32 qui exécute son propre processus.                                                                                                                                                                         |
| \_Processus de \_ partage \_ Win32 du service | 0x00000020 | Service Win32 qui partage un processus.                                                                                                                                                                                       |
| \_processus interactif de service \_  | 0x00000100 | Service Win32 qui interagit avec le bureau. Cette valeur ne peut pas être utilisée seule et doit être ajoutée à l’un des deux types précédents. La colonne StartName doit avoir la valeur LocalSystem ou null lors de l’utilisation de cet indicateur.<br/> |



 

Les types de service suivants ne sont pas pris en charge.



| Type de service               | Valeur      | Description                   |
|-------------------------------|------------|-------------------------------|
| \_pilote du noyau de service \_       | 0x00000001 | Service de pilote.             |
| \_pilote du \_ système de fichiers du service \_ | 0x00000002 | Service de pilote de système de fichiers. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Cette colonne est un jeu d’indicateurs binaires qui spécifient à quel moment démarrer le service. L’un des types suivants de démarrage du service doit être spécifié dans cette colonne.



| Type de démarrage du service  | Valeur      | Description                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| \_démarrage automatique du service \_   | 0x00000002 | Un service démarre au démarrage du système.                                                              |
| \_début de la demande de service \_ | 0x00000003 | Un service démarre lorsque le gestionnaire de contrôle des services appelle la fonction [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) . |
| SERVICE \_ désactivé      | 0x00000004 | Spécifie un service qui ne peut plus être démarré.                                                         |



 

la Windows Installer ne peut pas utiliser les options de démarrage du service \_ \_ de démarrage et du système de service \_ \_ .

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Cette colonne spécifie l’action effectuée par le programme de démarrage si le service ne parvient pas à démarrer au démarrage. Ces valeurs affectent les événements StartService ServiceControl pour les services installés. L’un des indicateurs de contrôle d’erreur suivants doit être spécifié dans cette colonne.

L’ajout de la constante **msidbServiceInstallErrorControlVital** (value = 0x08000) aux indicateurs dans le tableau suivant spécifie que l’installation globale doit échouer si le service ne peut pas être installé dans le système.



| Indicateur de contrôle d’erreur       | Valeur      | Action du programme de démarrage                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| erreur de SERVICE \_ \_ ignorée   | 0x00000000 | Journalise l’erreur et poursuit l’opération de démarrage.                                                                                                                                       |
| erreur de SERVICE \_ \_ normale   | 0x00000001 | Journalise l’erreur, affiche une boîte de message et poursuit l’opération de démarrage.                                                                                                                    |
| erreur de SERVICE \_ \_ critique | 0x00000003 | Journalise l’erreur si elle est possible et que le système est redémarré avec la dernière configuration connue. Si la dernière bonne configuration connue est en cours de démarrage, l’opération de démarrage échoue. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Cette colonne contient la chaîne qui nomme le groupe d’ordre de chargement dont ce service est membre. Spécifiez NULL ou une chaîne vide si le service n’appartient pas à un groupe.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dépendent
</dt> <dd>

Cette colonne est une liste de noms de services ou de groupes de commandes de charge que le système doit démarrer avant ce service. Séparez les noms dans la liste par des valeurs NULL. Si le service n’a pas de dépendances, spécifiez NULL ou une chaîne vide. Utilisez la syntaxe \[ ~ \] pour insérer une valeur null. La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.

Par exemple, pour exiger que le système démarre Service1 et Service2, avant de démarrer le service figurant dans la colonne ServiceInstall, entrez Service1 \[ ~ \] Service2 \[ ~ \] \[ ~ \] dans la colonne dépendances. Les identificateurs Service1 et Service2 doivent se trouver dans la clé primaire de la table ou être le nom du service déjà installé.

Vous devez préfixer les noms de groupes avec + pour qu’ils puissent être distingués d’un nom de service. Pour exiger que le système démarre Service1 et au moins un membre du groupe de commandes myGroup avant de démarrer le service figurant dans la colonne ServiceInstall, entrez Service1 \[ ~ \] + myGroup \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

Le service est connecté sous le nom donné par la chaîne de cette colonne. Si le type de service est SERVICE \_ Win32 \_ propre \_ , utilisez un nom de compte sous la forme : nom_domaine \\ nom_utilisateur. Si le compte appartient au domaine intégré, il est autorisé à le spécifier. \\ Nom d’utilisateur. Le compte LocalSystem doit être utilisé si le type de service est SERVICE \_ de partage Win32 de service \_ \_ ou \_ processus interactif de service \_ . La fonction [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) utilise le compte LocalSystem si StartName est spécifié comme null et que la plupart des services laissent donc cette colonne vide.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>De
</dt> <dd>

Cette chaîne est le mot de passe du nom de compte spécifié dans la colonne StartName. Notez que l’utilisateur doit disposer des autorisations pour ouvrir une session en tant que service. Le service n’a pas de mot de passe si StartName a la valeur null ou est une chaîne vide. Le StartName de LocalSystem est null et, par conséquent, le mot de passe de cette instance est null, donc la plupart des services ne remplissent pas cette colonne.

Notez qu’après la suppression d’un service qui a été installé avec un nom d’utilisateur et un mot de passe, le programme d’installation ne peut pas restaurer le service sans utiliser d’abord une action personnalisée pour obtenir le mot de passe. Le programme d’installation peut obtenir toutes les informations nécessaires sur le service, à l’exception du mot de passe, qui est stocké dans une partie protégée du système. L’action personnalisée acquiert le mot de passe en invitant l’utilisateur, en lisant une propriété dans la base de données ou en lisant un fichier. L’action personnalisée doit ensuite appeler [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)pour fournir le mot de passe, avant de réinstaller le service.

Windows Le programme d’installation n’écrit pas la valeur entrée dans le champ de mot de passe dans le fichier journal.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments
</dt> <dd>

Cette colonne contient les arguments de ligne de commande ou les propriétés nécessaires pour exécuter le service.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe vers la colonne de l’une des [tables de composants](component-table.md). Notez que pour installer ce service à l’aide de la table InstallService, le chemin d’accès de ce composant doit être le fichier exécutable du service.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Cette colonne contient une description localisable pour le service en cours de configuration. Si cette colonne est laissée vide, le programme d’installation utilise la description existante du service, s’il en existe une. pour plus d’informations, consultez \_ DESCRIPTION du SERVICE dans le kit de développement logiciel (SDK) de Microsoft Windows. Pour effacer une description existante, entrez « \[ ~ \] » dans cette colonne. Cela donne une description vide pour un service nouveau ou existant.

</dd> </dl>

## <a name="remarks"></a>Notes

L’action [InstallServices](installservices-action.md) dans les [*tables de séquence*](s-gly.md) traite les informations de cette table. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

Cette table possède la plupart des paramètres de la fonction Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) .

Bien qu’il soit possible d’utiliser l’interface utilisateur pour spécifier qu’un service doit être installé en tant qu’exécution à partir de la source, le programme d’installation ne prend pas en charge ce type d’installation. Les services qui s’exécutent avec le niveau de privilège du système local doivent être installés pour être exécutés à partir du disque dur local. Évitez d’installer des services qui empruntent l’identité des privilèges d’un utilisateur particulier, car cela peut écrire des données de sécurité dans un journal ou dans le registre système. Cela peut potentiellement créer un problème de sécurité, un conflit de mot de passe ou la perte de données de configuration lors du redémarrage du système.

Pour supprimer un service pendant une désinstallation, il doit exister un enregistrement correspondant pour le service dans la [table ServiceControl](servicecontrol-table.md) et l’indicateur **msidbServiceControlEventUninstallDelete** doit apparaître dans la colonne d’événement. Le programme d’installation ne supprime pas un service de la table ServiceInstall lors de la désinstallation sans cette entrée dans la table ServiceControl.

Pour plus d’informations sur la sécurisation d’un service, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
