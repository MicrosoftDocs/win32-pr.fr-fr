---
description: Utilisé pour sécuriser des parties individuelles d’une application dans un environnement verrouillé. Il peut être utilisé avec l’installation des fichiers, les clés de Registre et les dossiers créés.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Table LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524636"
---
# <a name="lockpermissions-table"></a>Table LockPermissions

La table LockPermissions est utilisée pour sécuriser des parties individuelles d’une application dans un environnement verrouillé. Il peut être utilisé avec l’installation des fichiers, les clés de Registre et les dossiers créés.

Un package destiné à être installé dans Windows Server 2008 R2 ou Windows 7 doit utiliser la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) au lieu de la table LockPermissions. Windows Installer versions antérieures à Windows Installer 5,0 ignorent la table MsiLockPermissionsEx. Windows Installer 5,0 peut installer un package qui contient la table LockPermissions. À compter de Windows Installer 5,0, l’installation d’un package qui contient à la fois la table MsiLockPermissionsEx et la table LockPermissions échoue et retourne Windows Installer message d’erreur 1941.

La table LockPermissions contient les colonnes suivantes.



| Colonne     | Type                               | Clé | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [Identificateur](identifier.md)       | O   | N        |
| Table de charge de travail      | [Text](text.md)                   | O   | N        |
| Domain     | [Correct](formatted.md)         | O   | O        |
| Utilisateur       | [Correct](formatted.md)         | O   | N        |
| Autorisation | [DoubleInteger](doubleinteger.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Cette colonne et la colonne de table spécifient ensemble le fichier, le répertoire ou la clé de Registre à sécuriser. La colonne LockObject est une clé étrangère qui pointe vers la clé primaire de la table spécifiée par la colonne de table.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Cette colonne et la colonne LockObject spécifient le fichier, le répertoire ou la clé de Registre à sécuriser. Dans la colonne table, entrez file, Registry ou CreateFolder pour spécifier un LockObject listé dans la table [file](file-table.md), la table [Registry](registry-table.md)ou [CreateFolder](createfolder-table.md).

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain
</dt> <dd>

Colonne qui identifie le domaine de l’utilisateur pour lequel les autorisations doivent être définies. Il s’agit du nom d’un ordinateur autonome ou d’un nom de domaine. Le type de données de la colonne est [mis en forme](formatted.md)et vous pouvez utiliser la chaîne \[ % UserDomain \] dans ce champ pour obtenir la valeur de la variable d’environnement UserDomain pour le domaine actuel. Pour faire en sorte que tout autre domaine requiert l’utilisation d' [actions personnalisées](custom-actions.md). Pour plus d’informations, consultez le tableau des actions personnalisées.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Utilisateur
</dt> <dd>

Colonne qui identifie le nom localisé de l’utilisateur pour lequel les autorisations doivent être définies. Ce nom doit se trouver sur l’ordinateur ou le domaine. L’installation échoue si l’ordinateur ou le contrôleur de domaine ne reconnaît pas la combinaison de domaine et d’utilisateur, ou si l’identificateur de sécurité (SID) de l’utilisateur ne peut pas être récupéré. Plusieurs utilisateurs peuvent être spécifiés pour un seul LockObject.

Les noms d’utilisateur courants « tout le monde » et « administrateurs » peuvent être entrés en anglais et mappés à des SID connus. LocalSystem reçoit un contrôle total sur tous les descripteurs de sécurité créés par le biais de la table LockPermissions. Vous pouvez utiliser la propriété [**ComputerName**](computername.md), la propriété [**LogonUser**](logonuser.md) ou la [**propriété UserName**](username.md) dans ce champ pour accéder à l’utilisateur actuel. Une action personnalisée est nécessaire pour entrer le nom localisé d’un autre utilisateur ou groupe.

Vous pouvez utiliser plusieurs enregistrements avec des entrées de données et des entrées de table identiques (mais différentes entrées utilisateur) pour spécifier des listes de contrôle d’accès pour plusieurs utilisateurs.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Autorisées
</dt> <dd>

Colonne qui identifie la description entière des privilèges système. Les éléments suivants fournissent les valeurs les plus couramment utilisées (une liste complète existe dans Winnt. h).



| Privilège                                                              | Description                     |
|------------------------------------------------------------------------|---------------------------------|
| GÉNÉRIQUE \_ tout<br/> 0X10000000<br/> 268435456<br/>     | Accès en lecture, écriture et exécution |
| \_Exécution générique<br/> 0X20000000<br/> 536870912<br/> | Exécuter l’accès                  |
| \_écriture générique<br/> 0X40000000<br/> 1073741824<br/>  | Accès en écriture                    |



 

Vous ne pouvez pas spécifier une \_ lecture générique dans la colonne autorisation. Toute tentative d’opération échouera. Au lieu de cela, vous devez spécifier une valeur telle que \_ lecture clé ou fichier \_ générique \_ lecture.

La valeur null entrée dans cette colonne est réservée à une utilisation ultérieure.

</dd> </dl>

## <a name="remarks"></a>Notes

Les actions [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)et [CreateFolders](createfolders-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

L’autorisation ne peut être définie que dans la table LockPermissions pour les utilisateurs qui existent déjà sur l’ordinateur ou le domaine. Une tentative de définition d’autorisations pour un utilisateur inconnu entraîne l’échec de l’installation, même si ce compte d’utilisateur est créé lors de l’installation par une action personnalisée différée.

Il est recommandé que le groupe local de l’administrateur système soit inclus dans toutes les listes de contrôle d’accès (ACL). Cela permet de s’assurer que l’administrateur système peut accéder aux objets et les gérer.

Chaque fichier, clé de registre ou répertoire figurant dans la table LockPermissions reçoit un descripteur de sécurité explicite, qu’il remplace ou non un objet existant. Le Windows Installer tente de préserver la sécurité sur les objets qui existent déjà sur le système. Si un objet n’est pas listé dans la table LockPermissions et remplace un objet existant, le remplacement obtient les paramètres de sécurité de l’objet qu’il remplace.

Si un objet n’est pas listé dans la table LockPermissions et qu’il ne remplace pas un objet existant, il ne reçoit pas de descripteur de sécurité explicite. L’accès au nouvel objet est basé sur les attributs de son objet parent ou conteneur. Si un objet n’est pas listé dans le tableau et remplace un objet sans descripteur de sécurité explicite, l’accès au nouvel objet est basé sur les attributs de son objet parent ou conteneur.

L’Windows Installer définit la propriété [**UserSid**](usersid.md) sur l’identificateur de sécurité (SID) ou l’utilisateur qui exécute l’installation.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




