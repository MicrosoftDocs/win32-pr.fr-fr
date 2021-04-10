---
description: Les propriétés d’informations récapitulatives suivantes doivent être définies dans chaque package d’installation, à l’aide d’un outil logiciel permettant d’accéder à l’interface IStream du flux d’informations de synthèse.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Ajout d’informations de résumé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115386"
---
# <a name="adding-summary-information"></a>Ajout d’informations de résumé

Les propriétés d’informations récapitulatives suivantes doivent être définies dans chaque package d’installation, à l’aide d’un outil logiciel permettant d’accéder à l’interface **IStream** du [flux d’informations de synthèse](summary-information-stream.md). Par exemple, vous pouvez utiliser l’outil Msiinfo.exe fourni avec le kit de développement logiciel (SDK) Windows Installer pour définir ces propriétés. Si ces propriétés ne sont pas définies, le package ne réussira pas la [validation du package](package-validation.md).



| Propriété informations de synthèse                                                   | Données                                   | Notes                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modèle**](template-summary.md)(plateforme et langue)<br/>         | ; 1033                                  | Plateforme et langage utilisé par la base de données. Si la spécification de la plateforme est manquante dans la valeur de la propriété Résumé du [**modèle**](template-summary.md) , le programme d’installation suppose l’architecture Intel. La propriété [**ProductLanguage**](productlanguage.md) de la base de données est généralement utilisée pour cette propriété Summary. L’ID de langue de l’exemple indique que le package utilise l’anglais (États-Unis). |
| [**Numéro de révision**](revision-number-summary.md)(code de package)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Il s’agit du [GUID](guid.md) du code du package qui identifie de façon unique l’exemple de package. Si vous reproduisez cet exemple, utilisez un utilitaire tel que GUIDGEN pour générer un GUID différent pour votre package. Les résultats de GUIDGEN contiennent des caractères minuscules, Notez que vous devez remplacer tous les caractères minuscules par des majuscules pour un code de package valide. Consultez [codes de package](package-codes.md).             |
| [**Nombre de pages**](page-count-summary.md)(version minimale du programme d’installation)<br/> | 200                                    | Pour un minimum Windows Installer 2,0, cette propriété doit être définie sur l’entier 200.                                                                                                                                                                                                                                                                                                                 |
| [**Nombre de mots**](word-count-summary.md)(type de source)<br/>            | 0                                      | Le type de source globale pour le package est un nom de fichier long et non compressé. Pour plus d’informations, consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md) , ainsi que la description de la colonne Attributes de la [table file](file-table.md) .                                                                                                                                |



 

Les autres propriétés du flux d’informations de résumé ne sont pas requises, mais doivent être définies pour l’exemple MNP2000.msi.



| Propriété informations de synthèse                                 | Données                                                                             | Notes                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Intitulé**](title-summary.md)                               | Base de données d’installation                                                            | Informe les utilisateurs que cette base de données est destinée à une installation plutôt qu’à une transformation ou un correctif.                        |
| [**Objet**](subject-summary.md)                           | MNP2000                                                                          | Les explorateurs de fichiers peuvent afficher ce fichier comme produit à installer avec cette base de données.                                  |
| [**Mots clés**](keywords-summary.md)                         | Programme d’installation, MSI, base de données                                                         | Les explorateurs de fichiers capables d’effectuer des recherches par mot clé peuvent rechercher ces mots.                                    |
| [**Auteur**](author-summary.md)                             | Microsoft Corporation                                                            | Nom du fabricant du produit.                                                                                |
| [**Commentaires**](comments-summary.md)                         | Cette base de données du programme d’installation contient la logique et les données requises pour installer le bloc-notes. | Informe les utilisateurs sur l’objectif de cette base de données.                                                                  |
| [**Création de l’application**](creating-application-summary.md) | Orca                                                                             | Application utilisée pour créer la base de données d’installation. L’exemple spécifie l’éditeur de base de données Orca comme exemple. |
| [**Sécurité**](security-summary.md)                         | 0                                                                                | L’exemple de base de données est en lecture-écriture illimité.                                                                    |



 

Vous n’avez pas besoin des propriétés définir le [**dernier enregistrement par**](last-saved-by-summary.md), [**date et heure**](last-saved-time-date-summary.md)de [**création**](create-time-date-summary.md), date de la dernière [**impression**](last-printed-summary.md), [**nombre de caractères**](character-count-summary.md)et résumé de la [**page de codes**](codepage-summary.md) pour terminer cet exemple de base de données. L’exemple s’appuie sur l’outil d’édition de base de données pour définir et mettre à jour ces propriétés facultatives.

Par exemple, pour utiliser MsiInfo pour ajouter les informations de résumé à l’exemple, accédez au répertoire contenant la base de données et utilisez la ligne de commande suivante. Ne réutilisez pas l’exemple d’ID de package indiqué ci-dessous.

**Msiinfo.exe MNP2000.msi-T « base de données d’installation »-J subject-A « Microsoft Corporation »-K « programme d’installation, MSI, base de données «-O » cette base de données du programme d’installation contient la logique et les données requises pour installer le bloc-notes.»-P ; 1033-V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3}-G 200-W 0-N Orca**

Pour plus d’informations sur le résumé, consultez [à propos du flux d’informations de synthèse](about-the-summary-information-stream.md), [utilisation du flux d’informations résumées](using-the-summary-information-stream.md)et [Référence du flux d’informations de synthèse](summary-information-stream-reference.md).

Pour obtenir une liste complète de toutes les propriétés des informations de résumé et des descriptions des propriétés de [synthèse](summary-property-descriptions.md) pour leur description, consultez la [propriété flux d’informations](summary-information-stream-property-set.md) de résumé définie.

[Continuer](importing-the-user-interface.md)

 

 




