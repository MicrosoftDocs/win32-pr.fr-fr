---
description: Windows Les propriétés du programme d’installation sont des variables globales utilisées par le programme d’installation au cours d’une installation.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Spécification des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f538bb354ef793a54f3eb60ddfe7b75b2aa96310abdd8a7331813d887433816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627799"
---
# <a name="specifying-properties"></a>Spécification des propriétés

Windows Les propriétés du programme d’installation sont des variables globales utilisées par le programme d’installation au cours d’une installation. Consultez les sections sous [Propriétés](properties.md). si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, la [table des propriétés](property-table.md) de votre copie de MNP2000.msi contient déjà de nombreuses propriétés utilisées par l’interface utilisateur. dans cette section, vous allez ajouter des informations supplémentaires au tableau de propriétés spécifique à l’installation de l’exemple de Bloc-notes. Voir aussi le [groupe tables d’informations sur les programmes](program-information-tables-group.md).

cinq propriétés sont requises dans chaque package d’installation, et elles doivent être mises à jour pour l’exemple Bloc-notes dans la [table des propriétés](property-table.md) de MNP2000.msi :

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Fabricant**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Bien que cela ne soit pas obligatoire pour tous les packages d’installation, les applications qui peuvent à l’avenir recevoir une mise à niveau doivent également avoir une propriété [**UpgradeCode**](upgradecode.md) . Consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table des propriétés. La liste fournit des liens vers les rubriques de référence pour les propriétés du programme d’installation intégrées. Les noms de propriété qui ne sont pas des liens sont des propriétés définies par l’auteur. La plupart des propriétés importées à partir de uisample.msi sont destinées à l’exemple d’interface utilisateur. L’interface utilisateur de la section ultérieure de l’exemple d’installation traite de l’interface utilisateur.

[Table de propriétés](property-table.md)



| Propriété                                         | Valeur                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| \_Sauvegarde de stockage en arrière                                 | < &                                |
| \_Recherche ButtonText                               | BR&owse                                   |
| Opération d’annulation de ButtonText \_                               | Annuler                                    |
| La \_ sortie de ButtonText                                 | &quitter                                     |
| Fin de l’exécution de ButtonText \_                               | &terminer                                   |
| Option de l’option ButtonText \_ ignorée                               | &ignorer                                   |
| Installation de ButtonText \_                              | &installer                                  |
| ButtonText \_ suivant                                 | &> suivant                                |
| \_Non-non                                   | &non                                       |
| ButtonText \_ OK                                   | Ok                                        |
| La \_ Suppression de ButtonText                               | &supprimer                                   |
| Réinitialisation de ButtonText \_                                | Réinitialisation &                                    |
| La \_ reprise de ButtonText                               | &Resume                                   |
| \_Nouvelle tentative de ButtonText                                | Nouvelle tentative &                                    |
| \_Réponse ButtonText                               | &retourner                                   |
| ButtonText \_ Oui                                  | &Oui                                      |
| CompleteSetupIcon                                | complet                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | point d’exclamation                                  |
| False                                            | 0                                         |
| Iagree                                           | Non                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Standard                                   |
| [**Fabricant**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**Réf**](productid.md)                   | aucun                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | En cours d'installation                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | réparation                                  |
| Installation                                            | Installation                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistant                                           | Assistant Installation                              |



 

[Continuer](importing-the-installexecutesequence.md)

 

 



