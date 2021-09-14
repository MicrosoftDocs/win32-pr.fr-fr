---
description: La table MsiLockPermissionsEx peut être utilisée pour sécuriser les services, les fichiers, les clés de Registre et les dossiers créés.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Table MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233969"
---
# <a name="msilockpermissionsex-table"></a>Table MsiLockPermissionsEx

La table MsiLockPermissionsEx peut être utilisée pour sécuriser les services, les fichiers, les clés de Registre et les dossiers créés.

Un package ne doit pas contenir à la fois la table MsiLockPermissionsEx et la [table LockPermissions](lockpermissions-table.md).

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. ce tableau est recommandé pour les packages destinés à une installation avec Windows Installer 5,0 ou version ultérieure.

La table MsiLockPermissionsEx contient les colonnes suivantes.



| Colonne               | Type                                       | Clé | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | O   | N        |
| LockObject           | [Identificateur](identifier.md)               | N   | N        |
| Table de charge de travail                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Condition            | [Condition](condition.md)                 | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Il s’agit de la clé primaire de cette table.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Cette colonne et la colonne de table spécifient ensemble le fichier, le répertoire, la clé de registre ou le service qui doit être sécurisé. La colonne LockObject est une clé étrangère qui pointe vers la clé primaire de la table spécifiée par la colonne de table.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Cette colonne et la colonne LockObject spécifient le fichier, le répertoire, la clé de registre ou le service qui doit être sécurisé. Dans la colonne table, entrez file, Registry, CreateFolder ou ServiceInstall pour spécifier un LockObject listé dans la table [file](file-table.md), la [table Registry](registry-table.md), la [table CreateFolder](createfolder-table.md)ou la [table ServiceInstall](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Entrez la chaîne SDDL pour indiquer les autorisations à appliquer à l’objet sélectionné. Le SDDL doit être fourni au [format de chaîne de descripteur de sécurité](../secauthz/security-descriptor-string-format.md).

Cela ne prend pas en charge les propriétés privées ou publiques.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Cette colonne contient une expression conditionnelle utilisée pour déterminer s’il faut appliquer l’autorisation spécifiée. Si la condition prend la **valeur false**, l’autorisation n’est pas appliquée. Si la condition prend la **valeur true**, l’autorisation est appliquée.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur la sécurisation des services, des fichiers, des clés de Registre et des dossiers créés, consultez [sécurisation des ressources](securing-resources-.md).

Utilisez la table MsiLockPermissionsEx pour sécuriser les objets d’un compte d’utilisateur en cours de création au cours de l’installation. Le compte d’utilisateur doit déjà exister lorsque l’installation sécurise l’objet. Créez le compte d’utilisateur avant d’installer le fichier, la clé de Registre, le dossier ou le service sécurisé.

si une paire LockObject et Table dans cette table possède plusieurs expressions conditionnelles qui ont la valeur true, l’installation échoue et Windows Installer retourne un message d’erreur 1942.

si la chaîne [FormattedSDDLText](formattedsddltext.md) dans le champ SDDLText ne peut pas être résolue en une chaîne SDDL valide, l’installation échoue et Windows Installer retourne un message d’erreur 1943.

si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur un fichier ou un dossier, l’installation échoue et Windows Installer renvoie un message d’erreur 1926.

si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur une clé de registre, l’installation échoue et Windows Installer renvoie un message d’erreur 1401.

si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur un service, l’installation échoue et Windows Installer renvoie un message d’erreur 1944.

## <a name="validation"></a>Validation

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
