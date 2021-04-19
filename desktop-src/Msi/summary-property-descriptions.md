---
description: Les propriétés de résumé des packages d’installation, des transformations et des correctifs sont décrites dans les tableaux suivants.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descriptions des propriétés de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537074"
---
# <a name="summary-property-descriptions"></a>Descriptions des propriétés de synthèse

Les propriétés de résumé des packages d’installation, des transformations et des correctifs sont décrites dans les tableaux suivants. Notez que la signification d’une propriété de résumé particulière peut être différente selon que la base de données appartient à un package d’installation, à une transformation ou à un package de correctifs. Pour plus d’informations sur les ID de propriété, les PID et les types, consultez [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Packages d’installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Summary, propriété</th>
<th>Signification de cette propriété dans une base de données d’installation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Intitulé</strong></a></td>
<td>Description de ce fichier sous la forme d’un package d’installation. La description doit inclure la &quot; <a href="about-the-installer-database.md">base de données d’installation de</a>l’expression.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Objet</strong></a></td>
<td>Nom du produit installé par ce package. Il doit s’agir du même nom que dans la propriété <a href="productname.md"><strong>ProductName</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Auteur</strong></a></td>
<td>Nom du fabricant de ce produit. Il doit s’agir du même nom que dans la propriété <a href="manufacturer.md"><strong>Manufacturer</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Mots clés</strong></a></td>
<td>Liste de mots clés qui peuvent être utilisés par les navigateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier. Les mots clés doivent inclure le &quot; programme d’installation &quot; et les mots clés spécifiques au produit.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commentaires</strong></a></td>
<td>Contient l’expression : &quot; cette base de données du programme d’installation contient la logique et les données requises pour installer <<em>nom du produit</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modèle</strong></a> (obligatoire)</td>
<td>La plateforme et les langages compatibles avec ce package d’installation. Consultez <a href="template-summary.md"><strong>template</strong></a> pour la syntaxe.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Dernier enregistrement par</strong></a></td>
<td>Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation. Cette propriété doit avoir la valeur null dans une base de données d’expédition finale. Le programme d’installation définit cette propriété sur la valeur de la propriété <a href="logonuser.md"><strong>LogonUser</strong></a> au cours d’une <a href="administrative-installation.md"><strong>installation d’administration</strong></a>. Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numéro de révision</strong></a> (obligatoire)</td>
<td>Contient le <a href="package-codes.md">Code du package</a> du programme d’installation.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Dernière impression</strong></a></td>
<td>Peut être défini sur la date et l’heure d’une <a href="administrative-installation.md">installation d’administration</a> à enregistrer lors de la création de l’image administrative.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Créer une date/heure</strong></a></td>
<td>Heure et date de création de la base de données du programme d’installation.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Heure/date du dernier enregistrement</strong></a></td>
<td>Date et heure système actuelles au moment de la dernière sauvegarde de la base de données du programme d’installation. Initialement null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Nombre de pages</strong></a> (obligatoire)</td>
<td>Contient une valeur utilisée pour identifier la version minimale du programme d’installation requise par ce package d’installation. Par exemple, si le package requiert au minimum la version 2,0 du programme d’installation, cette propriété doit être définie sur un entier de 200.
<blockquote>
[!Note]<br />
La valeur de cette propriété doit être supérieure ou égale à 200 avec des <a href="64-bit-windows-installer-packages.md">packages de Windows Installer 64 bits</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Nombre de mots</strong></a> (obligatoire)</td>
<td>Type de l’image du fichier source. Stocké à la place de la propriété nombre standard. Cette propriété est un champ de bits. Consultez la rubrique <a href="word-count-summary.md"><strong>nombre de mots</strong></a> pour les valeurs.<br/> À partir de Windows Installer version 4,0 sur Windows Vista, cette propriété comprend des bits pour spécifier si des privilèges élevés sont requis.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Nombre de caractères</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Création de l’application</strong></a></td>
<td>Contient le nom du logiciel utilisé pour créer cette base de données d’installation.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sécurité</strong></a></td>
<td>La valeur de cette propriété doit être 2-recommandée en lecture seule.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Courante</strong></a></td>
<td>Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé. Cette propriété doit être définie avant que toutes les propriétés de chaîne ne soient définies dans les informations de résumé.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformations



| Summary, propriété                                              | Signification de cette propriété dans une transformation                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Intitulé**](title-summary.md)                                | Description de ce fichier en tant que transformation. La description doit inclure la phrase suivante : «[transformer](database-transforms.md)».                                                                                                                                                                     |
| [**Objet**](subject-summary.md)                            | Nom du produit installé par le package d’installation d’origine. Il doit s’agir de la même valeur que la propriété Résumé de l' [**objet**](subject-summary.md) dans le package d’installation d’origine.                                                                                            |
| [**Auteur**](author-summary.md)                              | Nom du fabricant de cette transformation.                                                                                                                                                                                                                                                   |
| [**Mots clés**](keywords-summary.md)                          | Liste de mots clés qui peuvent être utilisés par les navigateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier. Les mots clés doivent inclure « programme d’installation », ainsi que des mots clés spécifiques au produit.                                                                                                                             |
| [**Commentaires**](comments-summary.md)                          | Contient l’expression : « cette transformation contient la logique et les données requises pour installer <*nom de produit*> ».                                                                                                                                                                                     |
| [**Modèle**](template-summary.md) (obligatoire)               | Les versions de plateforme et de langage compatibles avec cette transformation. Cette valeur peut être laissée vide s’il n’existe aucune restriction. Vous ne pouvez spécifier qu’un seul langage pour une transformation. Pour plus d’informations sur la syntaxe, consultez [**modèle**](template-summary.md).                                |
| [**Dernier enregistrement par**](last-saved-by-summary.md)                | ID de la plateforme et de la langue que la base de données a après avoir été transformée. La propriété [**Résumé du modèle**](template-summary.md) de la nouvelle base de données doit être définie sur les mêmes valeurs.                                                                                              |
| [**Numéro de révision**](revision-number-summary.md) (obligatoire) | Liste des GUID de code de produit et de la version des produits nouveaux et originaux et du GUID du code de mise à niveau. La liste est séparée par des points-virgules, comme suit. *Original : code* du produit original-version du produit ; *New-Product Code New-Product-version*; *Mettre à niveau le code*<br/>                       |
| [**Dernière impression**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Créer une date/heure**](create-time-date-summary.md)          | Date et heure de création de la transformation.                                                                                                                                                                                                                                                 |
| [**Heure/date du dernier enregistrement**](last-saved-time-date-summary.md)  | Date et heure système actuelles au moment où la transformation a été enregistrée. Initialement null.                                                                                                                                                                                                             |
| [**Nombre de pages**](page-count-summary.md) (obligatoire)           | Valeur utilisée pour indiquer la version minimale du programme d’installation requise pour traiter la transformation. La valeur doit être définie sur la plus grande des deux valeurs de propriété du [**nombre de pages**](page-count-summary.md) qui appartiennent aux bases de données utilisées pour générer la transformation.                                 |
| [**Nombre de mots**](word-count-summary.md) (obligatoire)           | Null                                                                                                                                                                                                                                                                                              |
| [**Nombre de caractères**](character-count-summary.md)            | Cette partie du flux d’informations de résumé est divisée en mots de 2 16 bits. Le mot supérieur contient des [*indicateurs de validation de transformation*](t-gly.md). Le mot inférieur contient des [*indicateurs de condition d’erreur de transformation*](t-gly.md). |
| [**Création de l’application**](creating-application-summary.md)  | Contient le nom du logiciel utilisé pour créer cette transformation.                                                                                                                                                                                                                                  |
| [**Sécurité**](security-summary.md)                          | La valeur de cette propriété doit être en lecture seule appliquée à 4.                                                                                                                                                                                                                                      |
| [**Courante**](codepage-summary.md)                          | Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé. Cette propriété doit être définie avant de pouvoir définir des propriétés de chaîne dans les informations de résumé.                                                                                                                    |



 

## <a name="patch-packages"></a>Packages de correctifs



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Summary, propriété</th>
<th>Signification de cette propriété dans un package correctif</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Intitulé</strong></a></td>
<td>Description de ce fichier en tant que package correctif. La description doit inclure l’expression : &quot; <a href="patch-packages.md">patch</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Objet</strong></a></td>
<td>Description du correctif qui comprend le nom du produit.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Auteur</strong></a></td>
<td>Nom du fabricant du package de correctifs.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Mots clés</strong></a></td>
<td>Liste délimitée par des points-virgules des sources du correctif.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commentaires</strong></a></td>
<td>Contient l’expression : &quot; ce correctif contient la logique et les données requises pour installer <<em>nom de produit</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modèle</strong></a> (obligatoire)</td>
<td>Liste délimitée par des points-virgules des codes de produit pouvant accepter ce correctif.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Dernier enregistrement par</strong></a></td>
<td>Liste délimitée par des points-virgules de noms de transformations de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numéro de révision</strong></a> (obligatoire)</td>
<td>Contient le code de correctif GUID pour le correctif. Elle peut être suivie d’une liste de GUID de code correctif pour les correctifs supprimés lorsque ce correctif est appliqué. Les codes de correctif sont concaténés, sans délimiteur, en séparant les GUID dans la liste.
<blockquote>
[!Note]<br />
Si le package de correctifs contient une table <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , le correctif ne supprime pas les correctifs figurant après le GUID du correctif actuel.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Dernière impression</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Créer une date/heure</strong></a></td>
<td>Date et heure de création du fichier correctif.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Heure/date du dernier enregistrement</strong></a></td>
<td>Date et heure système actuelles au moment où le package de correctifs a été enregistré. Cette valeur est initialement null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Nombre de pages</strong></a> (obligatoire)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Nombre de mots</strong></a> (obligatoire)</td>
<td>Contient une valeur qui indique la version minimale de Windows Installer requise pour installer le correctif. Un correctif avec une valeur de nombre de mots de 4 requiert Windows Installer version 3,0 ou ultérieure pour appliquer le correctif. La valeur 3 indique que Windows Installer version 2,0 ou ultérieure est requise. La valeur 2 indique que Windows Installer version 1,2 ou ultérieure est requise. La valeur par défaut est 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Nombre de caractères</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Création de l’application</strong></a></td>
<td>Nom du logiciel utilisé pour créer le correctif.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sécurité</strong></a></td>
<td>La valeur de cette propriété doit être en lecture seule appliquée à 4.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Courante</strong></a></td>
<td>Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé. Cette propriété doit être définie avant que toutes les propriétés de chaîne ne soient définies dans les informations de résumé.</td>
</tr>
</tbody>
</table>



 

 

 




