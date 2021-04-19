---
description: Le tableau suivant montre le jeu de propriétés de flux d’informations de synthèse, qui comprend les propriétés, leurs ID de propriété, PID et types correspondants.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Jeu de propriétés du flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3929e4180a85a8f154c0a0352ddd1f9a052769ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536222"
---
# <a name="summary-information-stream-property-set"></a>Jeu de propriétés du flux d’informations de synthèse

Le tableau suivant montre le jeu de propriétés de flux d’informations de synthèse, qui comprend les propriétés, leurs ID de propriété, PID et types correspondants. Pour plus d’informations sur la façon dont le programme d’installation utilise ces propriétés, consultez [descriptions des propriétés récapitulatives](summary-property-descriptions.md). Pour plus d’informations sur les fonctions de programme d’installation de Windows utilisées pour configurer les propriétés des informations de résumé, consultez [utilisation du flux d’informations de synthèse](using-the-summary-information-stream.md).



| Nom de la propriété                                                | ID de propriété        | PID | Type         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Courante**](codepage-summary.md)                         | \_page de codes PID      | 1   | VT \_ I2       |
| [**Intitulé**](title-summary.md)                               | \_titre PID         | 2   | VT- \_ LPSTR    |
| [**Objet**](subject-summary.md)                           | \_objet PID       | 3   | VT- \_ LPSTR    |
| [**Auteur**](author-summary.md)                             | \_auteur PID        | 4   | VT- \_ LPSTR    |
| [**Mots clés**](keywords-summary.md)                         | \_Mots clés PID      | 5   | VT- \_ LPSTR    |
| [**Commentaires**](comments-summary.md)                         | \_Commentaires PID      | 6   | VT- \_ LPSTR    |
| [**Modèle**](template-summary.md)                         | \_modèle PID      | 7   | VT- \_ LPSTR    |
| [**Dernier enregistrement par**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT- \_ LPSTR    |
| [**Numéro de révision**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT- \_ LPSTR    |
| [**Dernière impression**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | de VT \_ fileTime |
| [**Créer une date/heure**](create-time-date-summary.md)         | PID \_ créer \_ DTM   | 12  | de VT \_ fileTime |
| [**Heure/date de la dernière sauvegarde**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | de VT \_ fileTime |
| [**Nombre de pages**](page-count-summary.md)                     | PID \_ PageCount     | 14  | VT \_       |
| [**Nombre de mots**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_       |
| [**Nombre de caractères**](character-count-summary.md)           | ID de la PID \_     | 16  | VT \_       |
| [**Création de l’application**](creating-application-summary.md) | PID \_ appname       | 18  | VT- \_ LPSTR    |
| [**Sécurité**](security-summary.md)                         | \_sécurité PID      | 19  | VT \_       |



 

Le programme d’installation de gère actuellement trois formats de stockage pour les packages d’installation, les transformations et les packages de correctifs. Le CLSID du stockage est défini sur la classe de format appropriée pour le format particulier, indépendamment des informations de résumé pour le stockage.

 

 



