---
description: options de ligne de commande pour msiexec.exe pour Windows Installer 3,0 et versions antérieures. Fournit un tableau contenant des options, des paramètres et des descriptions. Exemples montrant comment installer des produits et d’autres tâches.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Options de ligne de commande
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 164947ce7baee8df69758be70ab03d9630a3bdd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092178"
---
# <a name="command-line-options"></a>Options de ligne de commande

Le programme exécutable qui interprète les packages et installe les produits est Msiexec.exe. Notez que msiexec définit également un niveau d’erreur au retour qui correspond aux [codes d’erreur système](/windows/desktop/Debug/system-error-codes). Les options de ligne de commande ne respectent pas la casse.

les options de ligne de commande du tableau suivant sont disponibles avec Windows Installer 3,0 et versions antérieures. les [Options du programme d’installation Standard Command-Line](standard-installer-command-line-options.md) sont également disponibles à partir de Windows Installer 3,0.



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
<td><strong>/I</strong></td>
<td><em>Package | ProductCode</em></td>
<td>Installe ou configure un produit.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p | o | e | d | c | a | u | m | v] <em>Package</em> | <em>ProductCode</em></td>
<td>Répare un produit. Cette option ignore toutes les valeurs de propriété entrées sur la ligne de commande. La liste d’arguments par défaut de cette option est « omus ». Cette option partage la même liste d’arguments que la propriété <a href="reinstallmode.md"><strong>REINSTALLMODE</strong></a> .<br/> p-Réinstalle uniquement si le fichier est manquant.<br/> o-réinstalle si le fichier est manquant ou si une version antérieure est installée.<br/> e-réinstalle si le fichier est manquant ou si une version égale ou antérieure est installée.<br/> d-réinstalle si le fichier est manquant ou si une version différente est installée.<br/> c-réinstalle si le fichier est manquant ou si la somme de contrôle stockée ne correspond pas à la valeur calculée. Répare uniquement les fichiers qui ont <strong>msidbFileAttributesChecksum</strong> dans la colonne attributs de la table <a href="file-table.md">file</a> .<br/> a-force la réinstallation de tous les fichiers.<br/> u-réécrit toutes les entrées de Registre spécifiques à l’utilisateur requises.<br/> m-réécrit toutes les entrées de Registre requises propres à l’ordinateur.<br/> s-remplace tous les raccourcis existants.<br/> v-exécute à partir de la source et met à nouveau le package local en cache. N’utilisez pas l’option de réinstallation <strong>v</strong> pour la première installation d’une application ou d’une fonctionnalité.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Package</em></td>
<td>Option <a href="administrative-installation.md">d’installation administrative</a> . Installe un produit sur le réseau.<br/></td>
</tr>
<tr class="even">
<td><strong>/Path</strong></td>
<td><em>Package | ProductCode</em></td>
<td>Désinstalle un produit.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m] <em>Package</em><br/> [u | m] <em>Liste des transformations</em> du <em>package</em><strong>/t</strong><br/> <em>or</em><br/> [u | m] <em>Package</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Publie un produit. Cette option ignore toutes les valeurs de propriété entrées sur la ligne de commande.<br/> u-publie l’utilisateur actuel.<br/> m-publie sur tous les utilisateurs de l’ordinateur.<br/> identificateur g-Language.<br/> t-applique la transformation au package publié.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + | ! | *] <em>Fichier journal</em></td>
<td>Écrit les informations de journalisation dans un fichier journal au niveau du chemin d’accès existant spécifié. Le chemin d’accès à l’emplacement du fichier journal doit déjà exister. Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal. Les indicateurs indiquent les informations à consigner. Si aucun indicateur n’est spécifié, la valeur par défaut est « iwearmo ».<br/> i-messages d’État.<br/> w-avertissements non irrécupérables.<br/> e-tous les messages d’erreur.<br/> a-démarrage des actions.<br/> r-enregistrements spécifiques à l’action.<br/> u-demandes de l’utilisateur.<br/> c-paramètres d’interface utilisateur initiaux.<br/> m-mémoire insuffisante ou informations de sortie irrécupérables.<br/> e-messages d’espace disque insuffisants.<br/> p-propriétés du terminal.<br/> v-sortie détaillée.<br/> x-informations supplémentaires sur le débogage. <strong>Windows Installer 2,0 :</strong> Non pris en charge. l’option x est disponible avec Windows Installer version 3.0.3790.2180 et ultérieure.<br/> <br/> + - Ajouter au fichier existant.<br/> ! -Videz chaque ligne dans le journal.<br/> &quot;*&quot; -Caractère générique, enregistrer toutes les informations, à l’exception des options v et x. Pour inclure les options v et x, spécifiez &quot; /l* VX &quot; .<br/>
<blockquote>
[!Note]<br />
pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez <a href="normal-logging.md">journalisation normale</a> dans la section <a href="windows-installer-logging.md">journalisation des Windows Installer</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>extension</em>
<blockquote>
[!Note]<br />
La longueur du <em>nom de fichier</em> ne doit pas dépasser huit caractères.
</blockquote>
<br/></td>
<td>Génère un fichier. mif d’état SMS. Doit être utilisé avec les options installer (-i), supprimer (-x), installation administrative (-a) ou réinstaller (-f). Le ISMIF32.DLL est installé dans le cadre de SMS et doit se trouver sur le chemin d’accès.<br/> Les champs du fichier MIF d’État sont renseignés avec les informations suivantes :<br/> Fabricant- <a href="author-summary.md"> <strong>auteur</strong></a><br/> Numéro de <a href="revision-number-summary.md"> <strong>révision</strong> du produit</a><br/> Version- <a href="subject-summary.md"> <strong>objet</strong></a><br/> Paramètres régionaux- <a href="template-summary.md"> <strong>modèle</strong></a><br/> Numéro de série-non défini<br/> Installation-définie par ISMIF32.DLL sur &quot; DateTime&quot;<br/> InstallStatus- &quot; réussite &quot; ou &quot; échec&quot;<br/> Description : messages d’erreur dans l’ordre suivant : 1) messages d’erreur générés par le programme d’installation. 2) ressource de Msi.dll si l’installation n’a pas pu commencer ou si l’utilisateur a quitté. 3) fichier de message d’erreur système. 4) message mis en forme : &quot; Erreur du programme d’installation% i &quot; , où% i est une erreur renvoyée par Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage [;P atchpackage2</em> ]</td>
<td>Applique un correctif. Pour appliquer un correctif à une image administrative installée, vous devez combiner les options suivantes :<br/> /p <em> &lt; PatchPackage &gt; [;p atchpackage2]</em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>Définit le niveau de l' <a href="user-interface-levels.md">interface utilisateur</a>.<br/> q, qn-aucune interface utilisateur<br/> QB <a href="b-gly.md"><em>interface utilisateur de base</em></a>. Utilisez br ! pour masquer le bouton <strong>Annuler</strong> .<br/> QR- <a href="r-gly.md"><em>IU réduite</em></a> sans boîte de dialogue modale affichée à la fin de l’installation.<br/> QF : <a href="f-gly.md"><em>interface utilisateur complète</em></a> et toutes les <a href="fatalerror-dialog.md"></a>boîtes de dialogue modales, <a href="userexit-dialog.md">UserExit</a>ou <a href="exit-dialog.md">Exit</a> créées à la fin.<br/> qn +-aucune interface utilisateur, à l’exception d’une boîte de dialogue modale affichée à la fin.<br/> QB +- <a href="b-gly.md"><em>interface utilisateur de base</em></a> avec une boîte de dialogue modale affichée à la fin. La zone modale ne s’affiche pas si l’utilisateur annule l’installation. Utiliser QB + ! ou qb ! + pour masquer le bouton <strong>Annuler</strong> .<br/> QB-- <a href="b-gly.md"><em>interface utilisateur de base</em></a> sans boîtes de dialogue modales. Notez que/QB +-n’est pas un niveau d’interface utilisateur pris en charge. Utilisez QB- ! ou Br !-pour masquer le bouton <strong>Annuler</strong> .<br/> Notez que le ! l’option est disponible avec Windows Installer 2,0 et fonctionne uniquement avec l’interface utilisateur de base. Elle n’est pas valide avec l’interface utilisateur complète.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> ou <strong>/h</strong></td>
<td> </td>
<td>affiche des informations de copyright pour Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>modules</em></td>
<td>Appelle la fonction système <strong>DllRegisterServer</strong> pour inscrire automatiquement les modules passés sur la ligne de commande. Spécifiez le chemin d’accès complet à la DLL. Par exemple, pour MY_FILE.DLL dans le dossier actif, vous pouvez utiliser :<br/> <strong>msiexec/y. \MY_FILE.DLL</strong><br/> Cette option est utilisée uniquement pour les informations de Registre qui ne peuvent pas être ajoutées à l’aide des tables de Registre du fichier .msi.<br/></td>
</tr>
<tr class="even">
<td><strong>z</strong></td>
<td><em>modules</em></td>
<td>Appelle la fonction système <strong>DllUnregisterServer</strong> pour annuler l’inscription des modules passés sur la ligne de commande. Spécifiez le chemin d’accès complet à la DLL. Par exemple, pour MY_FILE.DLL dans le dossier actif, vous pouvez utiliser : <br/> <strong>msiexec/z. \MY_FILE.DLL</strong><br/> Cette option est utilisée uniquement pour les informations de Registre qui ne peuvent pas être supprimées à l’aide des tables de Registre du fichier .msi.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Publie une nouvelle instance du produit. Doit être utilisé conjointement avec/t. disponible à partir de la version Windows Installer fournie avec Windows Server 2003 et Windows XP avec Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Spécifie une instance particulière du produit. Utilisé pour identifier une instance installée à l’aide de la prise en charge de plusieurs instances par le biais des transformations de modification de code de produit. disponible à partir de la version Windows Installer fournie avec Windows Server 2003 et Windows XP avec SP1. <br/></td>
</tr>
</tbody>
</table>



 

Les options/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a,/p,/y et/z ne doivent pas être utilisées ensemble. La seule exception à cette règle est que la mise à jour corrective d’une [installation administrative](administrative-installation.md) requiert l’utilisation de/p et/a. Les options/t,/c et/g doivent uniquement être utilisées avec/j. Les options/l et/q peuvent être utilisées avec les options/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a et/p. L’option/n peut être utilisée avec les options/i,/f,/x et/p.

Pour installer un produit à partir de : \\Example.msi, installez le produit comme suit :

**msiexec/i A : \\Example.msi**

Seules les [propriétés publiques](public-properties.md) peuvent être modifiées à l’aide de la ligne de commande. Tous les noms de propriété sur la ligne de commande sont interprétés comme majuscules, mais la valeur conserve le respect de la casse. Si vous entrez **MyProperty** sur une ligne de commande, le programme d’installation remplace la valeur de MyProperty et non la valeur de **MyProperty** dans la table de propriétés. Pour plus d’informations, consultez [à propos des propriétés](about-properties.md).

Pour installer un produit dont la propriété a la valeur VALUE, utilisez la syntaxe suivante sur la ligne de commande. Vous pouvez placer la propriété n’importe où, sauf entre une option et son argument.

Syntaxe correcte :

**msiexec/i A : \\Example.msi propriété = valeur**

Syntaxe incorrecte :

**msiexec/i PROPERTY = valeur A : \\Example.msi**

Les valeurs de propriété qui sont des chaînes littérales doivent être placées entre guillemets. Incluez tous les espaces blancs dans la chaîne entre les marques.

**msiexec/i A : \\Example.msi propriété = "espace blanc incorporé"**

Pour effacer une propriété publique à l’aide de la ligne de commande, définissez sa valeur sur une chaîne vide.

**msiexec/i A : \\Example.msi propriété = ""**

Pour les sections de texte séparées par des guillemets littéraux, mettez la section entre deux guillemets.

**msiexec/i A : \\Example.msi propriété = "incorporé" "guillemets" "espace blanc"**

L’exemple suivant montre une ligne de commande complexe.

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* msi. log CompanyName = « Acme » « widgets » et « gizmos ».**

L’exemple suivant montre les options de publication. Notez que les commutateurs ne respectent pas la casse.

**msiexec/JM msisample.msi/T Transform. MST/LIME logfile.txt**

L’exemple suivant montre comment installer une nouvelle instance d’un produit à publier. Ce produit est créé pour prendre en charge plusieurs transformations d’instance.

**msiexec/JM msisample.msi/T : Instance1. MST ; personnalisation. MST/c/LIME logfile.txt**

L’exemple suivant montre comment appliquer un correctif à une instance d’un produit installé à l’aide de plusieurs transformations d’instance.

**msiexec/p msipatch. msp ; msipatch2. msp/n {00000001-0002-0000-0000-624474736554} /qb**

Lorsque vous appliquez des correctifs à un produit spécifique, les options/i et/p ne peuvent pas être spécifiées ensemble dans une ligne de commande. Dans ce cas, vous pouvez appliquer des correctifs à un produit comme suit.

**msiexec/i A : \\Example.msi correctif = msipatch. msp ; msipatch2. msp/QB**

La propriété [**patch**](patch.md) ne peut pas être définie dans une ligne de commande, lorsque l’option/p est utilisée. Si la propriété **patch** est définie lors de l’utilisation de l’option/p, la valeur de la propriété **patch** est ignorée et remplacée.

 

