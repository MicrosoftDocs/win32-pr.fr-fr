---
description: La table d’erreurs permet de rechercher les modèles de mise en forme des messages d’erreur lors du traitement des erreurs avec un jeu de codes d’erreur, mais sans un jeu de modèles de mise en forme (situation normale).
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Table des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203208"
---
# <a name="error-table"></a>Table des erreurs

La table d’erreurs permet de rechercher les modèles de mise en forme des messages d’erreur lors du traitement des erreurs avec un jeu de codes d’erreur, mais sans un jeu de modèles de mise en forme (situation normale).

La table d’erreurs contient les colonnes suivantes.



| Colonne  | Type                     | Clé | Nullable |
|---------|--------------------------|-----|----------|
| Error   | [Integer](integer.md)   | O   | N        |
| Message | [Modèle](template.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs
</dt> <dd>

Pour obtenir la liste des numéros d’erreur et des messages, consultez [Windows Installer des messages d’erreur](windows-installer-error-messages.md) .

Le numéro d’erreur doit être un entier non négatif.

La plage comprise entre 25000 et 30000 est réservée aux erreurs des actions personnalisées. Les auteurs d’actions personnalisées peuvent utiliser cette plage pour leurs actions personnalisées.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Message
</dt> <dd>

Cette colonne contient le modèle de mise en forme des erreurs localisables. La table d’erreurs est générée par le processus de génération initial pour contenir les modèles de format de débogage.

Le tableau suivant répertorie les messages réservés. Pour obtenir la liste des codes d’erreur internes et de livraison, consultez [Windows Installer des messages d’erreur](windows-installer-error-messages.md).



| Error | Message                                                    | Notes                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Erreur irrécupérable :}}                                          | Préfixe d’en-tête pour les erreurs irrécupérables (INSTALLMESSAGE \_ FATALEXIT). Le texte entouré d’accolades doubles {{Text}} est visible uniquement dans le fichier journal. Le texte n’est pas affiché à l’utilisateur dans l’interface utilisateur.                  |
| 1     | Erreur \[ 1 \] .                                               | Préfixe d’en-tête pour les erreurs ( \_ erreur INSTALLMESSAGE)                                                                                                                                                             |
| 2     | Avertissement \[ 1 \] .                                             | Préfixe d’en-tête pour les avertissements (INSTALLMESSAGE \_ Warning)                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Information \[ 1 \] .                                                | Préfixe d’en-tête pour les messages d’information (INSTALLMESSAGE \_ info)                                                                                                                                              |
| 5     | Erreur interne \[ 1 \] . \[2 \] {, \[ 3 \] } {, \[ 4 \] }              | Préfixe d’en-tête pour les erreurs internes                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Disque plein :}}                                            | Préfixe d’en-tête pour les erreurs d’espace disque insuffisant (INSTALLMESSAGE \_ OUTOFDISKSPACE). Le texte entouré d’accolades doubles {{Text}} est visible uniquement dans le fichier journal. Le texte n’est pas affiché à l’utilisateur dans l’interface utilisateur. |
| 8     | Heure de l’action \[ \] : \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } {, \[ 3 \] } {, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Type de message : \[ 1 \] , argument : \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = Début de l’écriture dans le journal : \[ date/ \] \[ heure\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = Arrêt de la journalisation : \[ date/ \] \[ heure\] ===                 |                                                                                                                                                                                                              |
| 14    | Heure de début de l’action \[ \] : \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | Heure de fin de l’action \[ \] : \[ 1 \] . Valeur de retour \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Durée restante : { \[ 1 \] Min} { \[ 2 \] s}                    |                                                                                                                                                                                                              |
| 17    | Mémoire insuffisante. Arrêter les autres applications avant de réessayer |                                                                                                                                                                                                              |
| 18    | Le programme d’installation ne répond plus                          |                                                                                                                                                                                                              |
| 19    | Le programme d’installation s’est arrêté prématurément                           |                                                                                                                                                                                                              |
| 20    | Veuillez patienter pendant que Windows configure \[ ProductName \] ...    |                                                                                                                                                                                                              |
| 21    | Collecte des informations requises...                          |                                                                                                                                                                                                              |
| 22    | Suppression des versions antérieures de cette application...             |                                                                                                                                                                                                              |
| 23    | Préparation de la suppression des versions antérieures de cette application...  |                                                                                                                                                                                                              |
| 32    | L' \[ installation de {ProductName \] } s’est terminée correctement.            |                                                                                                                                                                                                              |
| 33    | Échec de l’installation de { \[ ProductName \] }.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Le modèle n’inclut pas la mise en forme du numéro d’erreur dans le champ 1. Lors du traitement de l’erreur, le programme d’installation joint un préfixe d’en-tête au modèle en fonction du type de message. Ces en-têtes sont également stockés dans la table des erreurs.

Le texte entouré d’accolades doubles {{Text}} est visible uniquement dans le fichier journal. Le texte n’est pas affiché à l’utilisateur dans l’interface utilisateur.

Vous pouvez importer une table d’erreurs localisée dans votre base de données à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Le kit de développement logiciel (SDK) comprend une table d’erreurs localisée pour chacune des langues listées dans la section [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) . Si la table d’erreurs n’est pas remplie, le programme d’installation charge les chaînes localisées pour la langue spécifiée par la propriété [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



