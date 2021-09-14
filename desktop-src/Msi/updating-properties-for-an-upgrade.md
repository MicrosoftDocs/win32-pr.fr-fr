---
description: Étant donné que la mise à niveau modifie le nom du fichier .msi et modifie le code du composant de certains composants, le code du produit de la mise à niveau doit être modifié par rapport à celui du produit d’origine.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Mise à jour des propriétés d’une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223092"
---
# <a name="updating-properties-for-an-upgrade"></a>Mise à jour des propriétés d’une mise à niveau

Étant donné que la mise à niveau modifie le nom du fichier .msi et modifie le code du composant de certains composants, le code du produit de la mise à niveau doit être modifié par rapport à celui du produit d’origine. Pour obtenir une description des cas où une mise à niveau est nécessaire pour modifier la propriété [**ProductCode**](productcode.md) , consultez [modification du code du produit](changing-the-product-code.md). Une mise à niveau qui modifie la valeur ProductCode est appelée [mise à niveau majeure](major-upgrades.md).

La propriété [**ProductName**](productname.md) du package de mise à niveau, la propriété [**ProductVersion**](productversion.md) , la propriété [**ProductLanguage**](productlanguage.md) et la propriété [**UpgradeCode**](upgradecode.md) peuvent être modifiées, ou rester inchangées, à partir du produit d’origine. en fonction des valeurs de ces propriétés, Windows Installer peut déterminer s’il faut appliquer les futurs packages de mise à niveau à la mise à niveau actuelle.

La propriété spécifiée dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md) doit être ajoutée à la propriété [**SecureCustomProperties**](securecustomproperties.md) .

Utilisez votre éditeur de base de données pour ouvrir MNP2001.msi et entrez les données suivantes dans la [table des propriétés](property-table.md). La liste fournit des liens vers les rubriques de référence pour les propriétés du programme d’installation intégrées. Les noms de propriété qui ne sont pas des liens sont des propriétés définies par l’auteur. La plupart des propriétés ont été importées à partir de Uisample.msi fourni avec le kit de développement logiciel (SDK). Pour plus d’informations, consultez [importation de l’interface utilisateur](importing-the-user-interface.md).

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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**Réf**](productid.md)                   | Aucun                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Installation                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | réparation                                  |
| Programme d’installation                                            | Programme d’installation                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistant                                           | Assistant Installation                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continuer](updating-sequence-tables-for-an-upgrade.md)

 

 



