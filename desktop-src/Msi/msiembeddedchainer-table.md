---
description: Utilisez ce tableau pour créer une installation de plusieurs packages.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Table MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011862"
---
# <a name="msiembeddedchainer-table"></a>Table MsiEmbeddedChainer

Utilisez ce tableau pour créer une [installation de plusieurs packages](multiple-package-installations.md). chaque ligne de la table MsiEmbeddedChainer fait référence à une autre fonction définie par l’utilisateur qui peut être utilisée pour installer plusieurs packages Windows Installer à partir d’un package unique. les [fichiers exécutables](executable-files.md) des fonctions définies par l’utilisateur sont stockés dans le package Windows Installer.

**[Windows Installer 4,0 ou version antérieure](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 4,5.

**Windows Server 2008 R2 avec le rôle [Services Bureau à distance](../termserv/terminal-services-portal.md) activé :** Non pris en charge. L’installation de plusieurs packages à l’aide de la table MsiEmbeddedChainer échoue si le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) est activé.

Pour installer plusieurs packages à partir d’un seul package, l’une des fonctions définies par l’utilisateur figurant dans la table MsiEmbeddedChainer doit avoir une instruction conditionnelle dans le champ condition qui évalue l’exécution de l’action. Si plusieurs fonctions ont une condition qui est évaluée pour s’exécuter, une seule fonction peut s’exécuter. Ce cas est une erreur, et il n’est pas garanti que la fonction s’exécutera. Si d’autres actions personnalisées sont nécessaires à l’installation, celles-ci doivent être créées dans la [table CustomAction](customaction-table.md) et les tables de séquences.

Les fonctions doivent rejoindre l’installation actuelle en appelant la fonction [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) et doivent appeler la fonction [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) pour valider l’installation de plusieurs packages. Si les fonctions retournent avant l’appel de **MsiEndTransaction**, le programme d’installation restaure toutes les installations.

La table MsiEmbeddedChainer contient les colonnes suivantes.



| Colonne             | Type                             | Clé : | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificateur](identifier.md)     | O   | N        |
| Condition          | [Condition](condition.md)       | N   | O        |
| CommandLine        | [Correct](formatted.md)       | N   | O        |
| Source             | [CustomSource](customsource.md) | N   | N        |
| Type               | [Integer](integer.md)           | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

Clé primaire de la table. Cette valeur est un identificateur unique pour la fonction définie par l’utilisateur décrite par cette ligne.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Instruction conditionnelle pour l’exécution de la fonction définie par l’utilisateur. Vous pouvez activer ou désactiver les fonctions listées dans la table MsiEmbeddedChainer à l’aide d’une transformation qui modifie les valeurs de propriété évaluées par ce champ. Pour plus d’informations, consultez [utilisation des propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine
</dt> <dd>

La valeur de ce champ fait partie de la chaîne de ligne de commande transmise au fichier exécutable identifié dans la colonne source. Le programme d’installation ajoute la valeur de ce champ au descripteur de transaction pour générer la ligne de commande. Si la valeur de cette colonne est null, la ligne de commande se compose uniquement du descripteur de transaction.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code
</dt> <dd>

Emplacement du fichier exécutable pour la fonction définie par l’utilisateur. Si la valeur de la colonne type est 2, cette colonne peut contenir une clé externe dans la [table binaire](binary-table.md). Si la valeur de la colonne type est 18, cette colonne peut contenir une clé externe dans la [table file](file-table.md). Si la valeur de la colonne type est 50, cette colonne peut contenir une clé externe dans la [table de propriétés](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Les fonctions répertoriées dans le tableau MsiEmbeddedChainer sont décrites à l’aide des types numériques d’actions personnalisées suivants. Cette colonne peut contenir uniquement les valeurs des trois types numériques suivants : toute autre combinaison d’indicateurs d’action personnalisée est ignorée.



| Type d’action personnalisé                                 | Indicateurs d’action personnalisée                                                | Valeur hexadécimale | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Type d’action personnalisé 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Type d’action personnalisée 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Type d’action personnalisé 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

la Windows Installer n’empêche pas les fonctions définies par l’utilisateur dans ce tableau de s’exécuter pendant la publication de l’application. Vous pouvez utiliser une instruction conditionnelle dans la colonne condition pour empêcher l’exécution d’une fonction pendant la publication.

le Windows Installer fournit également un gestionnaire d’interface utilisateur externe non incorporé pour générer une interface utilisateur riche en plus du package Windows Installer. pour plus d’informations sur l’utilisation d’un gestionnaire d’interface utilisateur externe avec le Windows Installer, consultez [surveillance d’une Installation à l’aide de MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

Le [tableau MsiPackageCertificate](msipackagecertificate-table.md) répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent une installation de plusieurs packages. Vous pouvez utiliser ce tableau pour réduire le nombre de fois où votre installation de plusieurs packages affiche une invite de [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) qui requiert une réponse d’un administrateur.

 

 
