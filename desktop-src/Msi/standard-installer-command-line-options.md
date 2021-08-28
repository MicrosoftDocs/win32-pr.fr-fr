---
Description : le programme exécutable qui interprète les packages et installe les produits est Msiexec.exe. Remarque Msiexec définit également un niveau d’erreur au retour qui correspond aux codes d’erreur système. Le tableau suivant identifie les options de ligne de commande standard pour ce programme. Les options de ligne de commande ne respectent pas la casse. Windows programme d’installation 2,0 : les options de ligne de commande qui sont identifiées dans cette rubrique sont disponibles à partir de Windows Installer 3,0. les Options de Command-Line Windows Installer sont disponibles avec Windows Installer&\# 160 ; 3.0 et versions antérieures.
ms. AssetID : b1707c88-1cca-45ab-bb23-6002bfd5204e title : programme d’installation standard Command-Line options ms. topic : article ms. Date : 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Options du programme d’installation standard Command-Line

Le programme exécutable qui interprète les packages et installe les produits est Msiexec.exe.

> [!Note]  
> Msiexec définit également un niveau d’erreur au retour qui correspond aux [codes d’erreur système](../debug/system-error-codes.md).

 

Le tableau suivant identifie les options de ligne de commande standard pour ce programme. Les options de ligne de commande ne respectent pas la casse.

**Windows Installer 2,0 :** les options de ligne de commande qui sont identifiées dans cette rubrique sont disponibles à partir de Windows Installer 3,0. les [Options de ligne de commande](command-line-options.md) Windows Installer sont disponibles avec Windows Installer 3,0 et versions antérieures.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Paramètres</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/Help</strong></td>
<td> </td>
<td>Aide et aide-mémoire. Affiche l’utilisation correcte de la commande d’installation, y compris la liste de tous les commutateurs et comportements. La description de l’utilisation peut être affichée dans l’interface utilisateur. Une utilisation incorrecte de toute option appelle cette option d’aide.<br/> Exemple : <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
l' <a href="command-line-options.md">Option de ligne de commande</a> équivalente Windows Installer est <strong>/ ?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Option Display quiet. Le programme d’installation exécute une installation sans afficher d’interface utilisateur. Aucune invite, aucun message ou boîte de dialogue n’est affiché à l’utilisateur. L’utilisateur ne peut pas annuler l’installation. Utilisez les options de ligne de commande <strong>/norestart</strong> ou <strong>/forcerestart</strong> standard pour contrôler les redémarrages. Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur.<br/> Exemples : <br/> <strong>msiexec/package Application.msi/quiet</strong><br/> <strong>Msiexec/Uninstall Application.msi/quiet</strong><br/> <strong>Msiexec/Update msipatch. msp/quiet</strong><br/> <strong>Msiexec/Uninstall msipatch. msp/package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
l’équivalent <a href="command-line-options.md">de l’Option de ligne de commande</a> Windows Installer est <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Option d’affichage passif. Le programme d’installation affiche une barre de progression à l’utilisateur qui indique qu’une installation est en cours, mais aucune invite ni aucun message d’erreur ne s’affiche pour l’utilisateur. L’utilisateur ne peut pas annuler l’installation. Utilisez les options de ligne de commande <strong>/norestart</strong> ou <strong>/forcerestart</strong> standard pour contrôler les redémarrages. Si aucune option de redémarrage n’est spécifiée, le programme d’installation redémarre l’ordinateur chaque fois que nécessaire sans afficher d’invite ou d’avertissement à l’utilisateur. <br/> Exemple : <strong>msiexec/package Application.msi/passive</strong> <br/>
<blockquote>
[!Note]<br />
l’équivalent de l' <a href="command-line-options.md">Option de ligne de commande</a> Windows Installer est <strong>/qb !-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S défini sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Option ne jamais redémarrer. Le programme d’installation ne redémarre jamais l’ordinateur après l’installation.<br/> Exemple : msiexec/package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
l’équivalent de la ligne de commande Windows Installer a <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress défini sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Option Always restart. Le programme d’installation redémarre toujours l’ordinateur après chaque installation.<br/> Exemple : msiexec/package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
l’équivalent de la ligne de commande Windows Installer est <a href="reboot.md"><strong>reboot</strong></a>= Force définie sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Invite avant le redémarrage de l’option. Affiche un message indiquant qu’un redémarrage est nécessaire pour terminer l’installation et demande à l’utilisateur s’il faut redémarrer le système maintenant. Cette option ne peut pas être utilisée avec l’option <strong>/Quiet</strong> .<br/>
<blockquote>
[!Note]<br />
l’équivalent de la ligne de commande Windows Installer a <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option de désinstallation du produit. Désinstalle un produit.<br/>
<blockquote>
[!Note]<br />
l’équivalent <a href="command-line-options.md">de l’Option de ligne de commande</a> Windows Installer est <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Uninstall</strong></td>
<td><em>/package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></td>
<td>Option de désinstallation de mise à jour. Désinstalle un correctif de mise à jour.<br/>
<blockquote>
[!Note]<br />
l’équivalent de l' <a href="command-line-options.md">Option de ligne de commande</a> Windows Installer est <strong>/i</strong> avec <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= update 1. msp | PatchGUID1[; Update2. msp | PatchGUID2] défini sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Option de journalisation. Écrit les informations de journalisation dans un fichier journal au niveau du chemin d’accès existant spécifié. Le chemin d’accès à l’emplacement du fichier journal doit déjà exister. Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal.<br/> Les informations suivantes sont entrées dans le journal :<br/>
<ul>
<li>Messages d'état</li>
<li>Avertissements récupérables</li>
<li>Tous les messages d’erreur</li>
<li>Démarrer des actions</li>
<li>Enregistrements spécifiques aux actions</li>
<li>Demandes de l’utilisateur</li>
<li>Paramètres initiaux de l’interface utilisateur</li>
<li>Informations de sortie insuffisantes ou irrécupérables</li>
<li>Messages d’espace disque insuffisant</li>
<li>Propriétés du terminal</li>
</ul>
<blockquote>
[!Note]<br />
l’équivalent <a href="command-line-options.md">de l’Option de ligne de commande</a> Windows Installer est <strong>/l *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez <a href="normal-logging.md">journalisation normale</a> dans la section <a href="windows-installer-logging.md">journalisation Windows Installer</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option d’installation du produit. Installe ou configure un produit.<br/>
<blockquote>
[!Note]<br />
l’équivalent <a href="command-line-options.md">de l’Option de ligne de commande</a> Windows Installer est <strong>/i</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. msp]</em></td>
<td>Option installer les correctifs. Installe un ou plusieurs correctifs. <br/>
<blockquote>
[!Note]<br />
l’équivalent de la ligne de commande Windows Installer contient <a href="patch.md"><strong>PATCH</strong></a> = [msipatch. msp] < ; PatchGuid2> défini sur la ligne de commande.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
