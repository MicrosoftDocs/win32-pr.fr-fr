---
description: La table d’environnement est utilisée pour définir les valeurs des variables d’environnement.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Table d’environnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de1fe52e8222bfde3e451b6ccc543511822e0d511a2ce1ce2b6bee8bc4fd117f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129599"
---
# <a name="environment-table"></a>Table d’environnement

La table d’environnement est utilisée pour définir les valeurs des variables d’environnement.

La table d’environnement contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Environnement | [Identificateur](identifier.md) | O   | N        |
| Nom        | [Text](text.md)             | N   | N        |
| Valeur       | [Correct](formatted.md)   | N   | O        |
| Composant\_ | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Environnement
</dt> <dd>

Il s’agit de la clé primaire de la table et est un jeton non localisé.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne est le nom localisable de la variable d’environnement. Les valeurs de clé sont écrites ou supprimées en fonction des caractères du tableau ci-après précédés du nom. Il n’y a aucun effet dans l’ordre des symboles utilisés dans un préfixe.



| Préfixe                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Créez la variable d’environnement si elle n’existe pas, puis définissez-la lors de l’installation. Si la variable d’environnement existe, définissez-la lors de l’installation.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Créez la variable d’environnement si elle n’existe pas, puis définissez-la lors de l’installation. Cela n’a aucun effet sur la valeur de la variable d’environnement si elle existe déjà.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Supprimez la variable d’environnement lorsque le composant est supprimé. Ce symbole peut être combiné avec n’importe quel préfixe.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Supprimez la variable d’environnement pendant une installation. Le programme d’installation supprime uniquement une variable d’environnement pendant une installation si le nom et la valeur de la variable correspondent aux entrées dans les champs nom et valeur de la table d’environnement. Si vous souhaitez supprimer une variable d’environnement, quelle que soit sa valeur, utilisez la syntaxe' ! 'et laissez le champ de valeur vide.                                                                                                                    |
| \*                             | ce préfixe est utilisé avec Windows 2000 pour indiquer que le nom fait référence à une variable d’environnement système. Si aucun astérisque n’est présent, le programme d’installation écrit la variable dans l’environnement de l’utilisateur. Ce symbole peut être combiné avec n’importe quel préfixe. Un package utilisé pour l’installation dans le [contexte d’installation](installation-context.md) par ordinateur doit écrire les variables d’environnement dans l’environnement de l’ordinateur en incluant \* dans la colonne nom. Pour plus d'informations, consultez la section Notes. |
| =-                             | La variable d’environnement est définie sur installer et supprimée lors de la désinstallation. Il s’agit du comportement habituel.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Supprime une variable d’environnement lors d’une installation ou d’une désinstallation.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Ce ne sont pas des préfixes valides                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Si le champ de valeur de la table contient un \[ ~ \] , les caractères de préfixe s’appliquent uniquement à la partie spécifiée de la chaîne. L’utilisation de \[ ~ \] est décrite ci-dessous dans la section colonne de valeur.

La variable d’environnement est supprimée si le champ de valeur de la table est vide. Par conséquent, si le champ valeur est vide, un préfixe = supprime la variable d’environnement lors de l’installation et le préfixe a-supprime toutes les valeurs actuelles lors de la désinstallation.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Cette colonne contient la valeur localisable qui doit être définie en tant que chaîne mise en forme. Consultez [mise en forme](formatted.md). Si ce champ est laissé vide, la variable est supprimée. Si le champ est vide et que la chaîne dans le champ nom est préfixée par le symbole-, la variable est supprimée uniquement lorsque le composant est supprimé.

Pour ajouter une valeur à la fin d’une variable existante, préfixez la chaîne dans ce champ par le caractère null \[ ~ \] et par le caractère de séparation. Par exemple, si le point-virgule est le séparateur choisi : \[ ~ \] ;*Valeur*.

Pour préfixer une valeur au début d’une variable existante, ajoutez la chaîne dans ce champ par le caractère de séparation et le caractère null \[ ~ \] . Par exemple, si le point-virgule est le séparateur choisi : *valeur*; \[ ~ \] .

Si aucun \[ ~ \] n’est présent dans le champ, la chaîne représente la valeur entière à définir ou à supprimer.

Chaque ligne ne peut contenir qu’une seule valeur. Par exemple, la *valeur* d’entrée ; *Valeur* \[ ~ ; \] est supérieur à une valeur et ne doit pas être utilisé, car cela provoque des résultats imprévisibles. *Valeur* d’entrée ; \[ ~ \] n’est qu’une seule valeur.

Si le nom est préfixé avec +, \[ ~ \] ne doit pas être utilisé dans la colonne valeur. Cela est dû au fait que la signification de « + » et de « \[ ~ \] » est clairement exclusive les unes des autres.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe de la première colonne de la [table de composants](component-table.md). Cette colonne fait référence au composant qui contrôle l’installation des valeurs d’environnement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour permettre au programme d’installation de définir des variables d’environnement, les actions [WriteEnvironmentStrings](writeenvironmentstrings-action.md) et [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) doivent être listées dans la [table InstallExecuteSequence](installexecutesequence-table.md).

Notez que les variables d’environnement ne changent pas pour l’installation en cours lors de l’exécution de l’action [WriteEnvironmentStrings](writeenvironmentstrings-action.md) ou [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) . sur Windows 2000, ces informations sont stockées dans le registre et un message avertit le système des modifications lorsque l’installation est terminée. Un nouveau processus, ou un autre processus qui vérifie ces messages, utilise les nouvelles variables d’environnement.

Lors de la modification de la variable d’environnement PATH avec la table d’environnement, n’essayez pas d’entrer explicitement le nouveau chemin d’accès dans le champ valeur. Au lieu de cela, étendez le chemin existant en préfixant ou en ajoutant une valeur et un délimiteur (;) à \[ ~ \] . Si \[ ~ \] n’est pas présent dans le champ de valeur, les informations du chemin d’accès existant sont perdues et l’installation du fichier de .msi peut empêcher le démarrage de l’ordinateur. La variable PATH est généralement définie à l’aide de la syntaxe suivante : \[ ~ \] ; Ajoutée.

Lors de l’exécution d’installations par ordinateur à partir d’un serveur Terminal Server, le programme d’installation écrit les variables d’environnement par utilisateur dans **HKU \\ . \\Environnement par défaut**. Étant donné que les services Terminal Server ne répliquent pas cette section du Registre, l’installation ne définit pas les variables d’environnement par utilisateur. Un package utilisé pour les installations par ordinateur doit écrire des variables d’environnement dans l’environnement de l’ordinateur en incluant \* dans la colonne nom. Si le package peut être installé par utilisateur ou par ordinateur, créez deux composants : (1) un composant par utilisateur avec les entrées de la table d’environnement créées pour les paramètres utilisateur, et (2) un composant par ordinateur avec la table d’environnement créée pour les paramètres de l’ordinateur. Condition l’installation de ce composant à l’aide de la propriété [**Privileged**](privileged.md) .

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




