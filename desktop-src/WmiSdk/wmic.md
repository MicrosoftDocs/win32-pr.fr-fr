---
title: wmic
description: L’utilitaire de ligne de commande WMI (WMIC) fournit une interface de ligne de commande pour WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 9fabf53f3f4479bbeb49f7391e4bb6d6608f723e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122477"
---
# <a name="wmic"></a>wmic

l’utilitaire de ligne de commande wmi (WMIC) fournit une interface de ligne de commande pour Windows Management Instrumentation (WMI). WMIC est compatible avec les interpréteurs de commandes et les commandes utilitaires existantes. Voici une rubrique de référence générale pour WMIC. pour plus d’informations et des instructions sur l’utilisation de WMIC, y compris des informations supplémentaires sur les alias, les verbes, les commutateurs et les commandes, consultez [utilisation de Windows Management Instrumentation ligne de commande](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) et [WMIC &mdash; adopter un contrôle de ligne de commande sur WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias est un changement de nom convivial d’une classe, d’une propriété ou d’une méthode qui facilite l’utilisation et la lecture de WMI. Vous pouvez déterminer les alias disponibles pour WMIC via le **/ ?** . Vous pouvez également déterminer les alias pour une classe spécifique à l’aide de la classe **&lt; className &gt; / ?** . Pour plus d’informations, consultez [alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Commutateur

Un commutateur est une option WMIC que vous pouvez définir globalement ou éventuellement. Pour obtenir la liste des commutateurs disponibles, consultez [commutateurs WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbes et adverbes

Pour utiliser des verbes dans WMIC, entrez le nom d’alias suivi du verbe. Si un alias ne prend pas en charge un verbe, vous recevez le message « le fournisseur ne peut pas prendre en charge l’opération tentée ». Pour plus d’informations, consultez [verbes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La plupart des alias prennent en charge les verbes suivants.

### <a name="assoc"></a>Craddock

Retourne le résultat de la `Associators of (<wmi_object>)` requête où *<\_ objet WMI>* correspond au chemin d’accès des objets retournés par les commandes **path** ou **Class** . Les résultats sont des instances associées à l’objet. Lorsque ASSOC est utilisé avec un alias, les classes avec la classe sous-jacente de l’alias sont retournées. Par défaut, la sortie est retournée au format HTML.

Le verbe ASSOC contient les commutateurs suivants.

| Commutateur                         | Description                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS : &lt; className&gt; | Les points de terminaison retournés associés à l’objet source doivent appartenir à la classe spécifiée ou en être dérivés.      |
| /RESULTROLE : &lt; roleName&gt;   | Les points de terminaison retournés doivent jouer un rôle spécifique dans les associations avec l’objet source.                              |
| /ASSOCCLASS : &lt; ASSOCCLASS&gt; | Les points de terminaison retournés doivent être associés à la source par le biais de la classe spécifiée ou de l’une de ses classes dérivées. |

Exemple : **Assoc du système d’exploitation**

### <a name="call"></a>CALL

Exécute une méthode.

Exemple : **service où Caption = 'telnet’appelle STARTSERVICE**

> [!NOTE]  
> Pour déterminer les méthodes disponibles pour une classe donnée, utilisez **/ ?**. Par exemple, **service où Caption = 'telnet’appelle/ ?** répertorie les fonctions disponibles pour la classe de service.

### <a name="create"></a>CREATE

Crée une instance de et définit les valeurs de propriété. Impossible d’utiliser CREATe pour créer une nouvelle classe.

Exemple : **Environment Create Name = "Temp"; VARIABLEVALUE = "nouveau"**

### <a name="delete"></a>Suppression

Supprime l’instance actuelle ou l’ensemble d’instances. La suppression peut être utilisée pour supprimer une classe.

Exemple : **processus où name = "CALC.EXE" Delete**

### <a name="get"></a>GET

Récupérer des valeurs de propriété spécifiques.

La commande dispose des commutateurs suivants.

| Commutateur                               | Description                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | La sortie est mise en forme avec chaque valeur figurant sur une ligne distincte et avec le nom de la propriété.                                           |
| /ALL                                 | La sortie est mise en forme en tant que table.                                                                                                            |
| /TRANSLATE : &lt; table de traduction&gt; | Traduisez la sortie à l’aide de la table de traduction nommée par la commande. Les tables de traduction BasicXml et novirgule sont incluses avec WMIC. |
| /EVERY : &lt; intervalle&gt;              | Répétez la commande toutes les secondes de l' &lt; intervalle &gt; .                                                                                         |
| /FORMAT : &lt; spécificateur de format&gt;     | Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.                                                                                  |

Exemple : **traiter demander un nom**

### <a name="list"></a>Liste

Affiche les données. LIST est le verbe par défaut.

La liste comporte les adverbes suivants.

| Verbe   | Description                                                  |
|----------|--------------------------------------------------------------|
| BRIEF    | Ensemble principal des propriétés.                                  |
| FULL     | Ensemble complet de propriétés. Il s’agit de l’adverbe par défaut pour la liste. |
| INSTANCE | Chemins d’accès d’instance uniquement.                                         |
| STATUT   | État des objets.                                       |
| SYSTEM   | Propriétés système.                                           |

La liste comporte les commutateurs suivants.

| Commutateur                               | Description                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /TRANSLATE : &lt; table de traduction&gt; | Traduisez la sortie à l’aide de la table de traduction nommée par la commande. Les tables de traduction BasicXml et novirgule sont incluses avec WMIC. |
| /EVERY : &lt; intervalle&gt;              | Répétez la commande toutes les secondes de l' &lt; intervalle &gt; .                                                                                         |
| /FORMAT : &lt; spécificateur de format&gt;     | Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.                                                                                  |

Exemple : **Brief (liste de processus** )

### <a name="set"></a>SET

Affecte des valeurs aux propriétés. Exemple : **Environment Set Name = "Temp"**, **VARIABLEVALUE = "New"**

## <a name="switches"></a>Commutateurs

Les commutateurs globaux sont utilisés pour définir les valeurs par défaut de l’environnement WMIC. Vous pouvez afficher la valeur actuelle des conditions définies par ces commutateurs en entrant la commande de **contexte** .

### <a name="namespace"></a>/NAMESPACE

Espace de noms utilisé en général par l’alias. La valeur par défaut est le \\ cimv2 racine.

Exemple : **/Namespace : \\ \\ root**

### <a name="role"></a>/ROLE

L’espace de noms WMIC recherche généralement des alias et d’autres informations WMIC.

Exemple : **/Role : \\ \\ root**

### <a name="node"></a>/NODE

Noms d’ordinateur, délimité par des virgules. Toutes les commandes sont exécutées de façon synchrone sur tous les ordinateurs répertoriés dans cette valeur. Les noms de fichiers doivent être précédés de &. Les noms d’ordinateur dans un fichier doivent être séparés par des virgules ou des lignes distinctes.

### <a name="implevel"></a>/IMPLEVEL

Niveau d'emprunt d'identité.

Exemple : **/IMPLEVEL : Anonymous**

### <a name="authlevel"></a>/AUTHLEVEL

Niveau d’authentification.

Exemple : **/AUTHLEVEL : PKT**

### <a name="locale"></a>/LOCALE

Paramètres régionaux.

Exemple : **/locale : MS \_ 411**

### <a name="privileges"></a>/PRIVILEGES

Activez ou désactivez tous les privilèges.

Exemple : **/privileges : Enable** ou **/privileges : Disable**

### <a name="trace"></a>/TRACE

Affiche la réussite ou l’échec de toutes les fonctions utilisées pour exécuter les commandes WMIC.

Exemple : **/trace : on** ou **/trace : OFF**

### <a name="record"></a>/RECORD

Enregistre toute la sortie dans un fichier XML. La sortie s’affiche également à l’invite de commandes.

Exemple : **/Record :** _MyOutput.xml_

### <a name="interactive"></a>/INTERACTIVE

En règle générale, les commandes DELETE sont confirmées.

Exemple : **/interactive : on** ou **/interactive : OFF**

### <a name="failfast-onofftimeoutinmilliseconds"></a>/FailFast **on** \| **off** \| *TimeoutInMilliseconds*

Si la valeur est ON, les ordinateurs/NODE sont interrogés avant d’envoyer des commandes WMIC à ceux-ci. Si un ordinateur ne répond pas, les commandes WMIC ne lui sont pas envoyées.

Exemple : « /FAILFAST : ON » ou « /FAILFAST : OFF »

**/FAILFAST WMIC : 1000**

### <a name="user"></a>/USER

Nom d’utilisateur utilisé par WMIC lors de l’accès aux ordinateurs/NODE ou aux ordinateurs spécifiés dans les alias. Vous êtes invité à entrer le mot de passe. Un nom d’utilisateur ne peut pas être utilisé avec l’ordinateur local.

Exemple : **/User :**_jdupont_

### <a name="password"></a>/PASSWORD

Mot de passe utilisé par WMIC lors de l’accès aux ordinateurs/NODE. Le mot de passe est visible sur la ligne de commande.

Exemple : **/Password :**_mot_de_passe_

### <a name="output"></a>/OUTPUT

Spécifie un mode pour toutes les redirections de sortie. La sortie n’apparaît pas sur la ligne de commande et la destination est effacée avant le début de la sortie. Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.

Exemple : **/Output : Clipboard**

### <a name="append"></a>/APPEND

Spécifie un mode pour toutes les redirections de sortie. La sortie n’apparaît pas sur la ligne de commande et la destination n’est pas effacée avant le début de la sortie et la sortie est ajoutée à la fin du contenu actuel de la destination. Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.

Exemple : **/Append : Clipboard**

### <a name="aggregate"></a>/AGGREGATE

Utilisé avec **les commutateurs** **List** et. Si agrégat est activé, liste et obtenir affichent leurs résultats lorsque tous les ordinateurs du/NODE ont répondu ou expiré. Si AGGREGATe est désactivé, LIST et affichent les résultats dès qu’ils sont reçus.

Exemple : **/Aggregate : OFF** ou **/Aggregate : on**

## <a name="commands"></a>Commandes

Les commandes WMIC suivantes sont disponibles à tout moment. Pour plus d’informations, consultez [commandes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

### <a name="class"></a>CLASS

Quitter le mode d’alias par défaut de WMIC pour accéder directement aux classes dans le schéma WMI. Pour plus d’informations sur les classes WMI disponibles, consultez [classes WMI](wmi-classes.md).

Exemple : **WMIC/output : c : \\ClassOutput.htm classe Win32 \_ SoundDevice**

### <a name="path"></a>PATH

Quitter le mode d’alias par défaut de WMIC pour accéder directement aux instances dans le schéma WMI.

Exemple : **WMIC/output : c : \\PathOutput.txt Path Win32 \_ SoundDevice/value**

### <a name="context"></a>CONTEXTE

Affichez les valeurs actuelles de tous les commutateurs globaux.

Exemple : **contexte WMIC**

### <a name="quit"></a>QUIT

Quittez WMIC.

Exemple : **WMIC Quit**

### <a name="exit"></a>EXIT

Quittez WMIC.

Exemple : **sortie WMIC**

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
