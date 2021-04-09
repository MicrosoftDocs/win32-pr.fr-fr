---
description: Msiinfo.exe est un utilitaire de ligne de commande qui utilise des fonctions de base de données et des fonctions de programme d’installation pour modifier ou afficher le flux d’informations de synthèse d’une base de données.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867914"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe est un utilitaire de ligne de commande qui utilise des fonctions [de base de données](database-functions.md) et des [fonctions de programme d’installation](installer-functions.md) pour modifier ou afficher le flux d’informations de [synthèse](summary-information-stream.md) d’une base de données.

## <a name="syntax"></a>Syntaxe

**Msiinfo** *{base de données} \[ \[ /b \] /d \] {option} {Data}*

-   La base de données ne peut pas être une base de données en lecture seule.
-   Si aucune donnée ne suit une option, la propriété correspondante est supprimée.
-   Vous pouvez spécifier un maximum de 20 options sur la ligne de commande. Les mêmes propriétés peuvent être spécifiées plusieurs fois.
-   Si les données contiennent un espace, mettez-les entre guillemets. Par exemple, comme/T "MY TITLE".

## <a name="command-line-options"></a>Options de la ligne de commande

Msiinfo.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret. Pour plus d’informations, consultez [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).



| Option | Description                                                                                                                                                                                                                                                                                                                                                      | ID de propriété        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *Aucune* | Si aucune option n’est spécifiée, l’utilitaire affiche les valeurs actuelles des propriétés des informations de résumé.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Affiche des informations sur chaque chaîne dans le pool de chaînes. L’option-b est valide uniquement si-d est également utilisé et que-b doit précéder l’option-d.                                                                                                                                                                                                                 |                    |     |
| -d     | Affiche des informations sur le pool de chaînes. Valide le pool de chaînes et fournit des informations sur la page de codes de la base de données. Notez que la page de codes de la base de données est différente de la page de codes du flux d’informations de synthèse ( \_ page de codes PID). Cette option vérifie également chaque chaîne pour les caractères non valides dans la page de codes de la base de données. |                    |     |
| -i     | Non applicable. Réservé.                                                                                                                                                                                                                                                                                                                                        | \_dictionnaire PID    | 0   |
| -c     | Définit la [**propriété de résumé**](codepage-summary.md)de la page de codes.                                                                                                                                                                                                                                                                                                  | \_page de codes PID      | 1   |
| -T     | Définit la [**propriété de résumé du titre**](title-summary.md).                                                                                                                                                                                                                                                                                                        | \_titre PID         | 2   |
| -j     | Définit la [**propriété de résumé**](subject-summary.md)de l’objet.                                                                                                                                                                                                                                                                                                    | objet ID PID \_    | 3   |
| -a     | Définit la [**propriété de résumé**](author-summary.md)de l’auteur.                                                                                                                                                                                                                                                                                                      | \_auteur PID        | 4   |
| -k     | Définit la [**propriété Résumé des mots clés**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | \_Mots clés PID      | 5   |
| -o     | Définit la [**propriété Résumé des commentaires**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | \_Commentaires PID      | 6   |
| -p     | Définit la [**propriété Résumé du modèle**](template-summary.md).                                                                                                                                                                                                                                                                                                  | \_modèle PID      | 7   |
| -l     | Définit la [**dernière propriété enregistrée par Résumé**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Définit la [**propriété Résumé du numéro de révision**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | Non applicable. Réservé.                                                                                                                                                                                                                                                                                                                                        | PID \_ edittime      | 10  |
| -S     | Définit la [**dernière propriété de résumé imprimée**](last-printed-summary.md). Pour spécifier l’année, le mois, le jour, l’heure, la minute et la seconde, utilisez le format « yyyy/mm/jj hh : mm : SS ». Par exemple, « 1997/06/20 03:25:59 ».                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Définit la [**propriété de résumé de la date/heure de création**](create-time-date-summary.md). Pour spécifier l’année, le mois, le jour, l’heure, la minute et la seconde, utilisez le format « yyyy/mm/jj hh : mm : SS ». Par exemple, « 1997/06/20 03:25:59 ».                                                                                                                                             | PID \_ créer \_ DTM   | 12  |
| -q     | Définit la [**dernière propriété de résumé d’heure/date enregistrée**](last-saved-time-date-summary.md). Pour spécifier l’année, le mois, le jour, l’heure, la minute et la seconde, utilisez le format « yyyy/mm/jj hh : mm : SS ». Par exemple, « 1997/06/20 03:25:59 ».                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Définit la [**propriété de résumé du nombre de pages**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ PageCount     | 14  |
| -w     | Définit la [**propriété de résumé du nombre de mots**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | Définit la [**propriété de résumé du nombre de caractères**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | ID de la PID \_     | 16  |
|        | Non applicable. Réservé.                                                                                                                                                                                                                                                                                                                                        | \_miniature PID     | 17  |
| -n     | Définit la [**propriété de résumé**](creating-application-summary.md)de la création de l’application.                                                                                                                                                                                                                                                                          | PID \_ appname       | 18  |
| -U     | Définit la [**propriété de résumé de sécurité**](security-summary.md).                                                                                                                                                                                                                                                                                                  | \_sécurité PID      | 19  |



 

Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



