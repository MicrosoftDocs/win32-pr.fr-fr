---
description: L’utilitaire de ligne de commande WMI (WMIC) fournit une interface de ligne de commande pour WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222927"
---
# <a name="wmic"></a>wmic

L’utilitaire de ligne de commande WMI (WMIC) fournit une interface de ligne de commande pour Windows Management Instrumentation (WMI). WMIC est compatible avec les interpréteurs de commandes et les commandes utilitaires existantes. Voici une rubrique de référence générale pour WMIC. Pour plus d’informations et des instructions sur l’utilisation de WMIC, y compris des informations supplémentaires sur les alias, les verbes, les commutateurs et les commandes, consultez [utilisation de Windows Management Instrumentation ligne de commande](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) et [WMIC-prendre le contrôle de ligne de commande sur WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias est un changement de nom convivial d’une classe, d’une propriété ou d’une méthode qui facilite l’utilisation et la lecture de WMI. Vous pouvez déterminer les alias disponibles pour WMIC via le **/ ?** . Vous pouvez également déterminer les alias pour une classe spécifique à l’aide du **<className> / ?** . Pour plus d’informations, consultez [alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Commutateur

Un commutateur est une option WMIC que vous pouvez définir globalement ou éventuellement. Pour obtenir la liste des commutateurs disponibles, consultez [commutateurs WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbes et adverbes

Pour utiliser des verbes dans WMIC, entrez le nom d’alias suivi du verbe. Si un alias ne prend pas en charge un verbe, vous recevez le message « le fournisseur ne peut pas prendre en charge l’opération tentée ». Pour plus d’informations, consultez [verbes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La plupart des alias prennent en charge les verbes suivants.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>Craddock
</dt> <dd>

Retourne le résultat de la `Associators of (<wmi_object>)` requête où *<\_ objet WMI>* correspond au chemin d’accès des objets retournés par les commandes **path** ou **Class** . Les résultats sont des instances associées à l’objet. Lorsque ASSOC est utilisé avec un alias, les classes avec la classe sous-jacente de l’alias sont retournées. Par défaut, la sortie est retournée au format HTML.

Le verbe ASSOC contient les commutateurs suivants.



| Commutateur                         | Description                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Les points de terminaison retournés associés à l’objet source doivent appartenir à la classe spécifiée ou en être dérivés.      |
| /RESULTROLE:<rolename>   | Les points de terminaison retournés doivent jouer un rôle spécifique dans les associations avec l’objet source.                              |
| /ASSOCCLASS:<assocclass> | Les points de terminaison retournés doivent être associés à la source par le biais de la classe spécifiée ou de l’une de ses classes dérivées. |



 

Exemple : **Assoc du système d’exploitation**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>INVOQU
</dt> <dd>

Exécute une méthode.

Exemple : **service où Caption = 'telnet’appelle STARTSERVICE**

> [!Note]  
> Pour déterminer les méthodes disponibles pour une classe donnée, utilisez **/ ?**. Par exemple, **service où Caption = 'telnet’appelle/ ?** répertorie les fonctions disponibles pour la classe de service.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>CRÉÉS
</dt> <dd>

Crée une nouvelle instance et définit les valeurs de propriété. Impossible d’utiliser CREATe pour créer une nouvelle classe.

Exemple : **Environment Create Name = "Temp"; VARIABLEVALUE = "nouveau"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>SUPPRIMER
</dt> <dd>

Supprime l’instance actuelle ou l’ensemble d’instances. La suppression peut être utilisée pour supprimer une classe.

Exemple : **processus où name = "CALC.EXE" Delete**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Télécharger
</dt> <dd>

Récupérer des valeurs de propriété spécifiques.

La commande dispose des commutateurs suivants.



| Commutateur                               | Description                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | La sortie est mise en forme avec chaque valeur figurant sur une ligne distincte et avec le nom de la propriété.                                           |
| /ALL                                 | La sortie est mise en forme en tant que table.                                                                                                            |
| Traduire<translation table> | Traduisez la sortie à l’aide de la table de traduction nommée par la commande. Les tables de traduction BasicXml et novirgule sont incluses avec WMIC. |
| Chaque<interval>              | Répétez la commande toutes les <interval> secondes.                                                                                         |
| FORMAT<format specifier>     | Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.                                                                                  |



 

Exemple : **traiter demander un nom**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>TARIFS
</dt> <dd>

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
| Traduire<translation table> | Traduisez la sortie à l’aide de la table de traduction nommée par la commande. Les tables de traduction BasicXml et novirgule sont incluses avec WMIC. |
| Chaque<interval>              | Répétez la commande toutes les <interval> secondes.                                                                                         |
| FORMAT<format specifier>     | Spécifie un mot clé ou un nom de fichier XSL pour mettre en forme les données.                                                                                  |



 

Exemple : **Brief (liste de processus** )

</dd> <dt>

<span id="SET"></span><span id="set"></span>DÉFINIE
</dt> <dd>

Affecte des valeurs aux propriétés. Exemple : **Environment Set Name = "Temp"**, **VARIABLEVALUE = "New"**

</dd> </dl>

## <a name="switches"></a>Commutateurs

Les commutateurs globaux sont utilisés pour définir les valeurs par défaut de l’environnement WMIC. Vous pouvez afficher la valeur actuelle des conditions définies par ces commutateurs en entrant la commande de **contexte** .

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Espace de noms utilisé en général par l’alias. La valeur par défaut est le \\ cimv2 racine.

Exemple : **/Namespace : \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

L’espace de noms WMIC recherche généralement des alias et d’autres informations WMIC.

Exemple : **/Role : \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Noms d’ordinateur, délimité par des virgules. Toutes les commandes sont exécutées de façon synchrone sur tous les ordinateurs répertoriés dans cette valeur. Les noms de fichiers doivent être précédés de &. Les noms d’ordinateur dans un fichier doivent être séparés par des virgules ou des lignes distinctes.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Niveau d'emprunt d'identité.

Exemple : **/IMPLEVEL : Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Niveau d’authentification.

Exemple : **/AUTHLEVEL : PKT**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Paramètres régionaux.

Exemple : **/locale : MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Activez ou désactivez tous les privilèges.

Exemple : **/privileges : Enable** ou **/privileges : Disable**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Affiche la réussite ou l’échec de toutes les fonctions utilisées pour exécuter les commandes WMIC.

Exemple : **/trace : on** ou **/trace : OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Enregistre toute la sortie dans un fichier XML. La sortie s’affiche également à l’invite de commandes.

Exemple : **/Record :** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

En règle générale, les commandes DELETE sont confirmées.

Exemple : **/interactive : on** ou **/interactive : OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Si, sur les ordinateurs/NODE, la commande ping est exécutée avant d’envoyer des commandes WMIC à celles-ci. Si un ordinateur ne répond pas, les commandes WMIC ne sont pas envoyées à celui-ci.

Exemple : « /FAILFAST : ON » ou « /FAILFAST : OFF »

**/FAILFAST WMIC : 1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Nom d’utilisateur utilisé par WMIC lors de l’accès aux ordinateurs/NODE ou aux ordinateurs spécifiés dans les alias. Vous êtes invité à entrer le mot de passe. Un nom d’utilisateur ne peut pas être utilisé avec l’ordinateur local.

Exemple : **/User :**_jdupont_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Mot de passe utilisé par WMIC lors de l’accès aux ordinateurs/NODE. Le mot de passe est visible sur la ligne de commande.

Exemple : **/Password :**_mot_de_passe_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Spécifie un mode pour toutes les redirections de sortie. La sortie n’apparaît pas sur la ligne de commande et la destination est effacée avant le début de la sortie. Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.

Exemple : **/Output : Clipboard**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Spécifie un mode pour toutes les redirections de sortie. La sortie n’apparaît pas sur la ligne de commande et la destination n’est pas effacée avant le début de la sortie et la sortie est ajoutée à la fin du contenu actuel de la destination. Les valeurs valides sont STDOUT, CLIPBOARD ou un nom de fichier.

Exemple : **/Append : Clipboard**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Utilisé avec **les commutateurs** **List** et. Si agrégat est activé, liste et obtenir affichent leurs résultats lorsque tous les ordinateurs du/NODE ont répondu ou expiré. Si AGGREGATe est désactivé, LIST et affichent les résultats dès qu’ils sont reçus.

Exemple : **/Aggregate : OFF** ou **/Aggregate : on**

</dd> </dl>

## <a name="commands"></a>Commandes

Les commandes WMIC suivantes sont disponibles à tout moment. Pour plus d’informations, consultez [commandes WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>TYPE
</dt> <dd>

Quitter le mode d’alias par défaut de WMIC pour accéder directement aux classes dans le schéma WMI. Pour plus d’informations sur les classes WMI disponibles, consultez [classes WMI](wmi-classes.md).

Exemple : **WMIC/output : c : \\ClassOutput.htm classe Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>D
</dt> <dd>

Quitter le mode d’alias par défaut de WMIC pour accéder directement aux instances dans le schéma WMI.

Exemple : **WMIC/output : c : \\PathOutput.txt Path Win32 \_ SoundDevice/value**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>CONTEXTE
</dt> <dd>

Affichez les valeurs actuelles de tous les commutateurs globaux.

Exemple : **contexte WMIC**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>DÉMISSIONN
</dt> <dd>

Quittez WMIC.

Exemple : **WMIC Quit**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>TERMINER
</dt> <dd>

Quittez WMIC.

Exemple : **sortie WMIC**

</dd> </dl>

## <a name="examples"></a>Exemples

Le [script de définition des paramètres IP/sous-réseau/passerelle/DNS à l’aide de l’exemple WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sur la Galerie TechNet décrit comment modifier et mettre à jour les paramètres IP, de sous-réseau, de passerelle et DNS.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

