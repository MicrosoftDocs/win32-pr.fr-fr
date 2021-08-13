---
description: Windows Les événements offrent un moyen centralisé et standard pour les applications (et le système d’exploitation) d’enregistrer des événements logiciels et matériels importants.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: journalisation des événements (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c1aa4808727a220ec104cb3e7bfdff2741dcb2366ca1468288a082baab813b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636923"
---
# <a name="event-logging-windows-installer"></a>journalisation des événements (Windows Installer)

les [événements de Windows](../events/windows-events.md) offrent un moyen centralisé et standard pour les applications (et le système d’exploitation) d’enregistrer des événements logiciels et matériels importants. Le service de journalisation des événements stocke les événements de diverses sources dans une collection unique appelée *Journal des événements*. avant Windows Vista, vous utiliseriez [Suivi d’v nements pour Windows](../etw/event-tracing-portal.md) (ETW) ou la [journalisation des événements](../eventlog/event-logging.md) pour consigner les événements. Windows Vista a introduit un nouveau modèle d’événement qui unifie à la fois ETW et l’API du [journal des événements Windows](../wes/windows-event-log.md) .

Le programme d’installation écrit également des entrées dans le journal des événements. Ces événements d’enregistrement, tels que les suivants :

-   La réussite ou l’échec de l’installation ; suppression ou réparation d’un produit.
-   Erreurs qui se produisent pendant la configuration du produit.
-   Détection de données de configuration endommagées.

Si une grande quantité d’informations est écrite, le fichier journal des événements peut être saturé et le programme d’installation affiche le message « le fichier journal de l’application est plein ».

Le programme d’installation peut écrire les entrées suivantes dans le journal des événements. Tous les messages du journal des événements ont un ID d’événement unique. Toutes les erreurs générales créées dans la [table d’erreurs](error-table.md) et retournées pour une installation qui échouent sont consignées dans le journal des événements d’application avec un ID de message égal à l’erreur + 10 000. Par exemple, le numéro d’erreur dans la table d’erreurs pour une installation effectuée avec succès est 1707. La réussite de l’installation est consignée dans le journal des événements de l’application avec l’ID de message 11707 (1707 + 10 000).

pour plus d’informations sur l’activation de la journalisation documentée sur l’ordinateur d’un utilisateur lors de la résolution des problèmes de déploiement, consultez [Windows Installer meilleures pratiques](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>ID de l’événement</th>
<th>Message</th>
<th>Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>Échec de la détection du produit « %1 », fonctionnalité « %2 » lors de la demande pour le composant « %3 »</td>
<td>Un message d’avertissement. Pour plus d’informations, consultez <a href="searching-for-a-broken-feature-or-component.md">recherche d’une fonctionnalité ou d’un composant endommagé</a>.</td>
</tr>
<tr class="even">
<td>1002</td>
<td>Valeur inattendue ou manquante (nom : ' %1 ', valeur : ' %2 ') dans la clé' %3 '</td>
<td>Message d’erreur indiquant qu’une valeur inattendue ou manquante s’est produite.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Sous-clé inattendue ou manquante « %1 » dans la clé « %2 »</td>
<td>Message d’erreur indiquant qu’une sous-clé est manquante ou inattendue.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>échec de la détection du produit « %1 », fonctionnalité « %2 », composant « %3 » <strong>. remarque :</strong> à partir de Windows Installer version 2,0, ce message est : échec de la détection du produit « %1 », de la fonctionnalité « %2 », du composant « %3 ». La ressource' %4 'n’existe pas.<br/></td>
<td>Un message d’avertissement. Voir aussi <a href="searching-for-a-broken-feature-or-component.md">recherche d’une fonctionnalité ou d’un composant endommagé</a>.</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>L’opération d’installation a initié un redémarrage</td>
<td>Message d’information indiquant que l’installation a initié un redémarrage du système.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Impossible d’effectuer la vérification de la signature numérique pour le cabinet' %1 '. WinVerifyTrust n’est pas disponible sur l’ordinateur.</td>
<td>Message d'avertissement. Un cabinet a été créé dans la <a href="msidigitalsignature-table.md">table MsiDigitalSignature</a> pour effectuer une vérification de <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> . Cette action n’a pas pu être effectuée, car les dll de chiffrement appropriées ne sont pas installées sur l’ordinateur.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>L’installation de %1 n’est pas autorisée par la stratégie de restriction logicielle. le Windows Installer autorise uniquement l’exécution d’éléments non restreints. Le niveau d’autorisation renvoyé par la stratégie de restriction logicielle était de %2.</td>
<td>Message d’erreur indiquant que l’administrateur a configuré une stratégie de restriction logicielle pour interdire cette installation.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>L’installation de %1 n’est pas autorisée en raison d’une erreur dans le traitement de la stratégie de restriction logicielle. L’objet ne peut pas être approuvé.</td>
<td>Message d’erreur indiquant qu’il y a eu des problèmes lors de la tentative de vérification du package en fonction de la stratégie de restriction logicielle.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>cette version de Windows ne prend pas en charge le déploiement de packages 64 bits. Le script « %1 » est destiné à un package 64 bits.</td>
<td>Message d’erreur indiquant que les scripts des packages 64 bits peuvent uniquement être exécutés sur un ordinateur 64 bits.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Rapport d’exceptions non gérées}</td>
<td>Message d’erreur pour une exception non gérée, il s’agit du rapport.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Les informations du proxy du programme d’installation ne sont pas inscrites correctement</td>
<td>Message d’erreur indiquant que les informations de proxy n’ont pas été inscrites correctement.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Échec de la connexion au serveur. Erreur :% d</td>
<td>Message d’information indiquant que l’installation n’a pas pu se connecter au serveur.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Échec de la détection du produit « %1 », fonctionnalité « %2 », composant « %3 ». La ressource' %4 'dans un composant d’exécution à partir de la source n’a pas pu être localisée, car aucune source valide et accessible n’a été trouvée.</td>
<td>Message d'avertissement. Pour plus d’informations, consultez <a href="searching-for-a-broken-feature-or-component.md">recherche d’une fonctionnalité ou d’un composant endommagé</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>Le SID de l’utilisateur est passé de « %1 » à « %2 », mais l’application gérée et les clés de données utilisateur ne peuvent pas être mises à jour. Erreur = « %3 ».</td>
<td>Message d’erreur indiquant qu’une erreur s’est produite lors de la tentative de mise à jour de l’inscription de l’utilisateur après la modification du SID de l’utilisateur.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>L’application' %1 'ne peut pas être installée, car elle n’est pas compatible avec cette version de Windows.</td>
<td>Message d’erreur indiquant que l’installation est incompatible avec la version en cours d’exécution de Windows. Contactez le fabricant du logiciel en cours d’installation pour une mise à jour.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Produit : %1-la mise à jour' %2 'a été supprimée avec succès.</td>
<td>Message d’information indiquant que le programme d’installation a supprimé la mise à jour. <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Produit : %1-Impossible de supprimer la mise à jour' %2 '. Code d’erreur %3. Des informations supplémentaires sont disponibles dans le fichier journal %4.</td>
<td>Message d’erreur indiquant que le programme d’installation n’a pas pu supprimer la mise à jour. Des informations supplémentaires sont disponibles dans le fichier journal. <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Produit : %1-Impossible de supprimer la mise à jour' %2 '. Code d’erreur %3.</td>
<td>Message d’erreur indiquant que le programme d’installation n’a pas pu supprimer la mise à jour. Pour plus d’informations sur l’activation de la journalisation, consultez <a href="windows-installer-best-practices.md">activer la journalisation détaillée sur l’ordinateur de l’utilisateur lors du dépannage du déploiement.</a> <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Produit : %1-mise à jour' %2 'correctement installée.</td>
<td>Message d’information indiquant que le programme d’installation a installé la mise à jour avec succès. <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Produit : %1-Impossible d’installer la mise à jour' %2 '. Code d’erreur %3. Des informations supplémentaires sont disponibles dans le fichier journal %4.</td>
<td>Message d’erreur indiquant que le programme d’installation n’a pas pu installer la mise à jour. Des informations supplémentaires sont disponibles dans le fichier journal. <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1 024</td>
<td>Produit : %1-Impossible d’installer la mise à jour' %2 '. Code d’erreur %3.</td>
<td>Message d’erreur indiquant que le programme d’installation n’a pas pu installer la mise à jour. Pour plus d’informations sur la façon d’activer la journalisation, consultez <a href="windows-installer-best-practices.md">activer la journalisation détaillée sur l’ordinateur de l’utilisateur lors du dépannage du déploiement.</a> <strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Produit : %1. Le fichier %2 est utilisé par le processus suivant : nom : %3, ID %4.</td>
<td><strong>Windows Installer 2,0 :</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Le programme d’installation a déterminé que sa clé de registre de données de configuration n’était pas correctement sécurisée. Le propriétaire de la clé doit être un système local ou Builtin\administrateurs. La clé existante sera supprimée et recréée avec les paramètres de sécurité appropriés.</td>
<td>Message d’avertissement. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Le programme d’installation a déterminé qu’une sous-clé de Registre %1 dans ses données de configuration n’a pas été correctement sécurisée. Le propriétaire de la clé doit être un système local ou Builtin\administrateurs. La sous-clé existante et tout son contenu seront supprimés.</td>
<td>Message d’avertissement. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Le programme d’installation a déterminé que son dossier de cache de données de configuration n’a pas été correctement sécurisé. Le propriétaire de la clé doit être un système local ou Builtin\administrateurs. Le dossier existant sera supprimé et recréé avec les paramètres de sécurité appropriés.</td>
<td>message d’avertissement<strong><a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> non disponible.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Produit : %1. Redémarrage requis.</td>
<td>Message d’avertissement indiquant qu’un redémarrage du système est nécessaire pour terminer l’installation et que le redémarrage a été différé ultérieurement. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Produit : %1. l’application a essayé d’installer une version plus récente du fichier Windows protégé %2. Vous devrez peut-être mettre à jour votre système d’exploitation pour que cette application fonctionne correctement. (Version du package : %3, version protégée du système d’exploitation : %4).</td>
<td>message d’avertissement indiquant que l’installation a tenté de remplacer un fichier critique protégé par <a href="windows-resource-protection-on-windows-vista.md">Protection des ressources Windows</a>. Une mise à jour du système d’exploitation peut être nécessaire pour utiliser cette application. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Produit : %1. L’assembly' %2 'du composant' %3 'est en cours d’utilisation.</td>
<td>Message d’avertissement indiquant que l’installation a tenté de mettre à jour un assembly en cours d’utilisation. Le système doit être redémarré pour terminer la mise à jour de cet assembly. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Une erreur s’est produite lors de l’actualisation des variables d’environnement mises à jour pendant l’installation de « %1 ».</td>
<td>Message d’avertissement indiquant que certains utilisateurs ayant ouvert une session sur l’ordinateur peuvent avoir besoin de se déconnecter et de se reconnecter pour terminer la mise à jour des variables d’environnement. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>Produit : %1. Version : %2. Langue : %3. Installation terminée avec l’État : %4. Fabricant : %5.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/> Champ 5- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Le champ 5 n’est pas disponible.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Produit : %1. Version : %2. Langue : %3. Suppression terminée avec l’État : %4. Fabricant : %5.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/> Champ 5- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Le champ 5 n’est pas disponible.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Produit : %1. Version : %2. Langue : %3. La modification de la configuration s’est terminée avec l’État %4. Fabricant : %5.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Champ 5- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Le champ 5 n’est pas disponible.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Produit : %1. Version : %2. Langue : %3. Mise à jour : %4. L’installation de la mise à jour est terminée avec l’État : %5. Fabricant : %6.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Champ 4 : nom convivial de l’utilisateur si la <a href="msipatchmetadata-table.md">table MsiPatchMetadata</a> est présente dans le package de correctifs. Dans le cas contraire, il s’agit du GUID du code correctif du correctif.<br/> Champ 5 : état de l’installation des mises à jour.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/> Champ 6- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Champ 6 non disponible.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Produit : %1. Version : %2. Langue : %3. Mise à jour : %4. Suppression de la mise à jour terminée avec l’État : %5. Fabricant : %6.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Champ 4 : nom convivial de l’utilisateur si la <a href="msipatchmetadata-table.md">table MsiPatchMetadata</a> est présente dans le package de correctifs. Dans le cas contraire, il s’agit du GUID du code correctif du correctif.<br/> Champ 5 : état de la suppression des mises à jour.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/> Champ 6- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Champ 6 non disponible.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Produit : %1. Version : %2. Langue : %3. Redémarrage requis. Type de redémarrage : %4. Raison du redémarrage : %5. Fabricant : %6.</td>
<td>Champ 1-champ <a href="productname.md"><strong>NomProduit</strong></a> 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Champ 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Champ 4-une constante indiquant le type de redémarrage : <br/> <dl> <strong>msirbRebootImmediate</strong> (1)-il y a eu un redémarrage immédiat de l’ordinateur.<br />
<strong>msirbRebootDeferred</strong> (2)-un utilisateur ou un administrateur a différé un redémarrage requis de l’ordinateur à l’aide de l’interface utilisateur ou du <a href="reboot.md"><strong>redémarrage</strong></a>= ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0)-redémarrage requis pour une raison non spécifiée.<br />
<strong>msirbRebootInUseFilesReason</strong> (1) : un redémarrage était nécessaire pour remplacer les fichiers en cours d’utilisation.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2) : le package contient une action <a href="schedulereboot-action.md">ScheduleReboot</a> .<br />
<strong>msirbRebootForceRebootReason</strong> (3) : le package contient une action <a href="forcereboot-action.md">ForceReboot</a> .<br />
<strong>msirbRebootCustomActionReason</strong> (4) : action personnalisée appelée fonction <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode</strong></a> .<br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 et versions antérieures</a>:</strong> Non disponible.<br/> Champ 6- <a href="manufacturer.md"> <strong>fabricant</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 et versions antérieures</a>:</strong> Champ 6 non disponible.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>Le programme d’installation a rencontré une erreur inattendue lors de l’installation de ce package. Il s'agit peut-être d'un problème lié au package. Le code d’erreur est [1]. {{Les arguments sont : [2], [3], [4]}}</td>
<td>Message d’erreur indiquant qu’une erreur interne s’est produite. Le texte de ce message est basé sur le texte créé pour l’erreur 5 dans la table des erreurs.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Produit [2] : l’opération d’installation s’est terminée correctement</td>
<td>Message d’information indiquant que l’installation du produit a réussi.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Produit [2] : échec de l’opération d’installation</td>
<td>Message d’erreur indiquant que l’installation du produit a échoué.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Produit [2]--la configuration s’est terminée avec succès.</td>
<td>Message d’information indiquant la réussite de la configuration du produit.</td>
</tr>
</tbody>
</table>



 

Vous pouvez importer des chaînes d’erreurs localisées pour des événements dans votre base de données à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Le kit de développement logiciel (SDK) comprend des chaînes de ressources localisées pour chacune des langues listées dans la section [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) . Si les chaînes d’erreur correspondant aux événements ne sont pas remplies, le programme d’installation charge les chaînes localisées pour la langue spécifiée par la propriété [**ProductLanguage**](productlanguage.md) .

 

 
