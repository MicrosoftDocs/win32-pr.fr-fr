---
description: le WiSumInf.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple de script peut être utilisé pour gérer le flux d’informations de synthèse d’un package de Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Gérer les informations récapitulatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ff360bd56dabc57b3a7ffccdba8c4f90346193
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021355"
---
# <a name="manage-summary-information"></a>Gérer les informations récapitulatives

le WiSumInf.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple de script peut être utilisé pour gérer le [flux d’informations de synthèse](summary-information-stream.md) d’un package de Windows Installer.

L’exemple illustre l’utilisation de :

-   [**Propriété SummaryInformation (objet installer)**](installer-summaryinformation.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)

l’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiSumInf.vbs \[ chemin d’accès à la propriété de base de données \] \[ = valeur\]**

spécifiez le chemin d’accès à la base de données Windows Installer. Si aucun autre argument n’est spécifié, le script répertorie toutes les propriétés de résumé du package. Spécifiez une liste de propriétés et valeurs de résumé à mettre à jour à l’aide de la propriété format = value. Vous pouvez spécifier la propriété par le nom ou la valeur PID indiquée ci-dessous. Les champs de date et d’heure utilisent le format de paramètres régionaux actuel, ou « Now » ou « date ». Pour plus d’informations, consultez [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).



| PID | Nom        | Description                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Page de codes ANSI des chaînes de texte dans les informations récapitulatives. Pour plus d’informations, consultez propriété Résumé de la [**page de codes**](codepage-summary.md) .                                                                                                                                                           |
| 2   | Intitulé       | Type de Windows Installer package. Pour plus d’informations, consultez la [**propriété Summary de titre**](title-summary.md).                                                                                                                                                                                    |
| 3   | Objet     | Nom complet du produit. Pour plus d’informations, consultez la [**propriété Résumé**](subject-summary.md)de l’objet.                                                                                                                                                                                               |
| 4   | Auteur      | Creator, généralement le nom du fournisseur. Pour plus d’informations, consultez [**propriété Summary**](author-summary.md)de l’auteur.                                                                                                                                                                                     |
| 5   | Mots clés    | Liste des mots clés à utiliser par l’Explorateur de fichiers. Pour plus d’informations, consultez la [**propriété Résumé des mots clés**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Commentaires    | Description du rôle ou de l’utilisation du package. Pour plus d’informations, consultez la [**propriété Résumé des commentaires**](comments-summary.md).                                                                                                                                                                       |
| 7   | Modèle    | Plateformes et langages pris en charge. Pour plus d’informations, consultez [**propriété Résumé du modèle**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Défini uniquement par le programme d’installation. Pour plus d’informations, consultez [**dernier enregistrement par la propriété Summary**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Révision    | GUID du code du package. Pour plus d’informations, consultez la [**propriété Résumé du numéro de révision**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Affiche     | Date et heure de l’image d’installation. Pour plus d’informations, consultez [**dernière propriété de résumé imprimé**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Date de création     | Date et heure de création du package. Pour plus d’informations, consultez la rubrique relative [**à la propriété Résumé de la date/heure de création**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Enregistré       | Date et heure de la dernière modification du package. Pour plus d’informations, consultez la [**propriété Résumé de l’heure/date du dernier enregistrement**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Pages       | version minimale de Windows Installer requise pour ce package. Pour plus d’informations, consultez [**propriété de résumé du nombre de pages**](page-count-summary.md).                                                                                                                                             |
| 15  | Cherché       | Type d’image du fichier source. Pour plus d’informations, consultez [**propriété de résumé du nombre de mots**](word-count-summary.md). à partir de Windows Installer version 4,0 sur Windows Vista et Windows Server 2008, cette propriété comprend des bits pour spécifier si des privilèges élevés sont requis.<br/> |
| 16  | Caractères  | Utilisé uniquement pour les transformations. [**Nombre de caractères**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Application | Application associée à ce fichier, par exemple « Windows Installer ». Pour plus d’informations, consultez [**Creating application Summary Property**](creating-application-summary.md).                                                                                                                        |
| 19  | Sécurité    | Paramètre de sécurité. Pour plus d’informations, consultez [**Security Summary Property**](security-summary.md).                                                                                                                                                                                               |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 




