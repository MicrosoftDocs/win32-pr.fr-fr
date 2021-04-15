---
description: VShadow est un outil de ligne de commande que vous pouvez utiliser pour créer et gérer des clichés instantanés de volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Outil et exemple VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485025"
---
# <a name="vshadow-tool-and-sample"></a>Outil et exemple VShadow

VShadow est un outil de ligne de commande que vous pouvez utiliser pour créer et gérer des clichés instantanés de volume.

> [!Note]  
> VShadow est inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures. Le kit de développement logiciel (SDK) VSS 7,2 comprend une version de VShadow qui s’exécute uniquement sur Windows Server 2003. Pour plus d’informations sur le téléchargement de la SDK Windows et du kit de développement logiciel (SDK) VSS 7,2, consultez [service VSS](volume-shadow-copy-service-portal.md).

 

L’outil VShadow utilise des options de ligne de commande et des indicateurs facultatifs pour identifier le travail à effectuer. Lorsqu’elle est utilisée sans aucune option de ligne de commande, la commande VShadow crée un jeu de clichés instantanés.

Les commandes VShadow effectuent les opérations suivantes :

-   [Création d’un jeu de clichés instantanés](#creating-a-shadow-copy-set)
-   [Importation d’un jeu de clichés instantanés](#importing-a-shadow-copy-set)
-   [Interrogation des propriétés des clichés instantanés](#querying-shadow-copy-properties)
-   [Suppression de clichés instantanés](#deleting-shadow-copies)
-   [Rupture d’un jeu de clichés instantanés](#breaking-a-shadow-copy-set)
-   [Rupture d’un jeu de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Exposition locale d’un cliché instantané](#exposing-a-shadow-copy-locally)
-   [Exposition à distance d’un cliché instantané](#exposing-a-shadow-copy-remotely)
-   [Affichage de l’État et des métadonnées de l’enregistreur](#listing-writer-status-and-metadata)
-   [Exécution d’opérations de restauration](#performing-restore-operations)
-   [Retour à un cliché instantané précédent](#reverting-to-a-previous-shadow-copy)
-   [Resynchronisation des numéros d’unités logiques](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Création d’un jeu de clichés instantanés

**vshadow** \[ OptionalFlags \] *VolumeList*

Cette commande crée un jeu de clichés instantanés.

*VolumeList* est une liste de noms de volumes. VShadow crée un cliché instantané pour chaque volume de la liste. Un nom de volume peut éventuellement se terminer par une barre oblique inverse ( \\ ). Par exemple, C : et C : \\ sont des noms de volume valides. Vous pouvez également spécifier des dossiers montés (par exemple, C : \\ DirectoryName) ou des noms de GUID de volume (par exemple \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9D01-505054503030}).

*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur d’indicateur facultative</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés matériels différentiels. Cet indicateur et l’indicateur <strong>-AP</strong> s’excluent mutuellement.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés matériels du Plex. Cet indicateur et l’indicateur <strong>-ad</strong> s’excluent mutuellement.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>file</em><strong>. xml</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés non transportables et stocke le document des composants de sauvegarde dans le fichier spécifié. Ce fichier peut être utilisé dans une opération de restauration ultérieure. Cet indicateur et l’indicateur <strong>-t</strong> s’excluent mutuellement.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-Exec =,</strong><em>commande</em><br/></td>
<td>Cet indicateur facultatif exécute une commande ou un script après la création des clichés instantanés, mais avant la fermeture de l’outil VShadow. La <em>commande</em> peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd. Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.<br/>
<blockquote>
[!Note]<br />
Pour des raisons de sécurité et pour simplifier l’implémentation, l’indicateur facultatif <strong>-Exec</strong> n’acceptera pas de paramètres à passer à la commande ou au script. La chaîne entière transmise à l’indicateur facultatif <strong>-Exec</strong> est traitée comme un fichier cmd ou exe unique. Pour plus d’informations sur cette limitation, consultez le code source VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Cet indicateur facultatif spécifie que l’opération de cliché instantané ne doit être effectuée que si toutes les signatures de disque peuvent être restaurées.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-Mask</strong><br/></td>
<td>Cet indicateur facultatif spécifie que les numéros d’unités logiques des clichés instantanés doivent être masqués sur l’ordinateur lorsque le jeu de clichés instantanés est rompu.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-NAR</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés sans récupération automatique. Pour plus d’informations sur cette option, consultez la documentation de l’indicateur VSS_VOLSNAP_ATTR_NO_AUTORECOVERY de l’énumération <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-Revert</strong><br/></td>
<td>Cet indicateur facultatif spécifie que les signatures de disque ne doivent pas être restaurées.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés sans impliquer d’enregistreurs. Pour plus d’informations sur les clichés instantanés sans participation aux rédacteurs, consultez détails de la création de clichés <a href="shadow-copy-creation-details.md">instantanés</a>. Cet indicateur et les indicateurs <strong>-Wi</strong> et <strong>-WX</strong> s’excluent mutuellement.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Cet indicateur facultatif spécifie les <a href="vssgloss-p.md"><em>clichés instantanés persistants</em></a>.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong><br/></td>
<td>Cet indicateur facultatif spécifie que les numéros d’unités logiques des clichés instantanés doivent être en lecture/écriture lorsque le jeu de clichés instantanés est rompu.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Cet indicateur facultatif spécifie <a href="vssgloss-c.md"><em>les clichés instantanés accessibles par le client</em></a>.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>file</em><strong>. cmd</strong><br/></td>
<td>Cet indicateur facultatif génère un fichier CMD contenant les variables d’environnement associées aux clichés instantanés créés, comme les ID de cliché instantané et les ID de jeu de clichés instantanés.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>file</em><strong>. xml</strong><br/></td>
<td>Cet indicateur facultatif spécifie les clichés instantanés transportables et stocke le document des composants de sauvegarde dans le fichier spécifié par le paramètre <em>File.xml</em> . Ce fichier peut être utilisé dans une opération d’importation et/ou de restauration ultérieure. Cet indicateur et l’indicateur <strong>-BC</strong> s’excluent mutuellement.<br/> <strong>Windows server 2003, Standard Edition et Windows server 2003, Web Edition :</strong> Les clichés instantanés transportables ne sont pas pris en charge. Toutes les éditions de Windows Server 2003 avec Service Pack 1 (SP1) prennent en charge les clichés instantanés transportables.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong><br/></td>
<td>Cet indicateur facultatif spécifie que la récupération TxF doit être appliquée lors de la création de clichés instantanés.<br/>
<blockquote>
[!Note]<br />
Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-suivi</strong><br/></td>
<td>Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong><br/></td>
<td>Cet indicateur facultatif force l’outil VShadow à attendre la confirmation de l’utilisateur avant de quitter.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>enregistreur</em><br/></td>
<td>Cet indicateur facultatif vérifie que le composant ou le writer spécifié est inclus dans le cliché instantané. L' <em>enregistreur</em> peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur. Cet indicateur et l’indicateur <strong>-NW</strong> s’excluent mutuellement.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>enregistreur</em><br/></td>
<td>Cet indicateur facultatif vérifie que le composant ou le writer spécifié est exclu du cliché instantané. L' <em>enregistreur</em> peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur. Cet indicateur et l’indicateur <strong>-NW</strong> s’excluent mutuellement.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importation d’un jeu de clichés instantanés

**vshadow** \[ OptionalFlags \] **-i =**_file_*_. xml_*

L’option de ligne **de commande-i** importe un jeu de clichés instantanés transportable.

> [!Note]  
> Cette option de ligne de commande est prise en charge uniquement sur les systèmes d’exploitation Windows Server.

 

Le fichier de *File.xml* doit être un fichier de document de composants de sauvegarde pour un jeu de clichés instantanés transportable créé avec l’indicateur facultatif **-t** ou **-BC** .

Un jeu de clichés instantanés est un cliché [*instantané persistant*](vssgloss-p.md) s’il a été créé avec l’indicateur **-p** facultatif. Si le jeu de clichés instantanés transportable n’est pas persistant, il apparaît pendant une brève période pendant l’exécution de la commande de création de clichés instantanés, et est automatiquement supprimé lorsque la commande retourne. Vous pouvez importer des clichés instantanés non persistants uniquement lors de la création de clichés instantanés, en créant le jeu de clichés instantanés à l’aide de l’indicateur facultatif **-Exec** pour exécuter un fichier cmd qui appelle VShadow **-i**.

L’option de ligne **de commande-i** ne peut pas être combinée avec d’autres options de ligne de commande.

*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.



| Valeur d’indicateur facultative                                                                                                            | Description                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =,**_commande_<br/> | Cet indicateur facultatif exécute une commande ou un script après l’importation des clichés instantanés, mais avant la sortie de l’outil VShadow. La *commande* peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd. Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-suivi**<br/>                                                  | Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-Wait**<br/>                                                           | Cet indicateur facultatif force l’outil VShadow à attendre la confirmation de l’utilisateur avant de quitter.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Interrogation des propriétés des clichés instantanés

**vshadow** **-q**

**vshadow** **-qx =**_ShadowCopySetId_

**vshadow** **-s =**_ShadowCopyId_

L’option de ligne de commande **-q** répertorie les propriétés de tous les clichés instantanés sur l’ordinateur.

L’option de ligne de commande **-qx** répertorie les propriétés de tous les clichés instantanés dans le jeu de clichés instantanés dont l’ID est spécifié par *ShadowCopySetId*.

L’option de ligne de commande **-s** répertorie les propriétés du cliché instantané dont l’ID est spécifié par *ShadowCopyId*.

Ces options de ligne de commande utilisent une combinaison de [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) et [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) pour obtenir les propriétés du jeu de clichés instantanés donné.

Les options de ligne de commande **-q**, **-qx** et **-s** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.

## <a name="deleting-shadow-copies"></a>Suppression de clichés instantanés

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-DX =**_ShadowCopySetId_

**vshadow** **-DS =**_ShadowCopyId_

La commande **-da** supprime tous les clichés instantanés sur l’ordinateur.

> [!Note]  
> L’option de ligne de commande **-da** requiert la confirmation de l’utilisateur.

 

L’option **de ligne de commande-do** supprime le cliché instantané le plus ancien sur l’ordinateur.

L’option de ligne de commande **-DX** supprime tous les clichés instantanés dans le jeu de clichés instantanés dont l’ID est spécifié par *ShadowCopySetId*.

L’option de ligne de commande **-DS** supprime le cliché instantané dont l’ID est spécifié par *ShadowCopyId*.

Ces options de ligne de commande sont destinées uniquement aux [*clichés instantanés persistants*](vssgloss-p.md) . Les clichés instantanés non persistants n’ont pas besoin d’être explicitement supprimés, car ils sont automatiquement supprimés lors de la fermeture de la commande de création de VShadow.

Les options de ligne de commande **-da**, **-do**, **-DX** et **-DS** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.

## <a name="breaking-a-shadow-copy-set"></a>Rupture d’un jeu de clichés instantanés

**vshadow** **-b =**_ShadowCopySetId_

**vshadow** **-BW =**_ShadowCopySetId_

L’option de ligne de commande **-b =**_ShadowCopySetId_ convertit chaque cliché instantané dans le jeu de clichés instantanés en un volume en lecture seule autonome.

L’option de ligne de commande **-BW =**_ShadowCopySetId_ convertit chaque cliché instantané dans le jeu de clichés instantanés en un volume inscriptible autonome.

> [!Note]  
> Les options de ligne de commande **-b** et **-BW** sont uniquement prises en charge sur les systèmes d’exploitation Windows Server.

 

Pour plus d’informations sur l’arrêt d’un jeu de clichés instantanés, consultez [interruption des clichés instantanés](breaking-shadow-copies.md).

Une fois le jeu de clichés instantanés rompu, le jeu de clichés instantanés et les clichés instantanés individuels n’existent plus et ne peuvent pas être gérés à l’aide de commandes VSS.

Un jeu de clichés instantanés est persistant s’il a été créé avec l’indicateur **-p** facultatif. Si le jeu de clichés instantanés transportable n’est pas persistant, il apparaît pendant une brève période pendant l’exécution de la commande de création de clichés instantanés, et est automatiquement supprimé lorsque la commande retourne. Vous pouvez arrêter les jeux de clichés instantanés non persistants uniquement lors de la création de clichés instantanés, en créant le jeu de clichés instantanés à l’aide de l’indicateur facultatif **-Exec** pour exécuter un fichier cmd qui appelle **vshadow** **-b** ou **vshadow** **-BW**.

Les options de ligne de commande **-b** et **-BW** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Rupture d’un jeu de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx

**vshadow** **-Bex**

L’option de ligne de commande **-Bex** divise un jeu de clichés instantanés selon les options spécifiées par les indicateurs facultatifs **-Mask**, **-RW**, **-forcerevert** et **-Revert** . Cette option de ligne de commande est similaire aux options de ligne de commande **-b** et **-BW** . L’option de ligne de commande **-Bex** utilise la méthode [**IVssBackupComponentsEx2 :: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , tandis que les options de ligne de commande- **b** et **-BW** utilisent la méthode [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .

Pour plus d’informations sur l’arrêt d’un jeu de clichés instantanés, consultez [interruption des clichés instantanés](breaking-shadow-copies.md).

> [!Note]  
> L’option de ligne de commande **-Bex** est prise en charge uniquement sur les systèmes d’exploitation Windows Server.

 

**vshadow** **-Bex** **-Mask**

L’indicateur **-Mask** spécifie que le numéro d’unité logique de cliché instantané sera masqué de l’hôte. Si l’indicateur **-Mask** est spécifié, les indicateurs **-RW**, **-forcerevert** et **-Revert** ne peuvent pas être spécifiés.

**vshadow** **-Bex** **-RW**

L’indicateur **-RW** spécifie que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture.

**vshadow** **-Bex** **-forcerevert**

L’indicateur **-forcerevert** spécifie que les identificateurs de disque de tous les numéros d’unités logiques de cliché instantané seront restaurés sur ceux des numéros d’unités logiques d’origine. Toutefois, si l’un des numéros d’unités logiques d’origine est présent sur le système, l’opération échoue et aucun des identificateurs n’est rétabli. Cet indicateur et l’indicateur **-Revert** s’excluent mutuellement.

**vshadow** **-Bex** **-Revert**

L’indicateur **-Revert** indique qu’aucun identificateur de disque LUN de cliché instantané ne sera rétabli. Cet indicateur et l’indicateur **-forcerevert** s’excluent mutuellement.

## <a name="exposing-a-shadow-copy-locally"></a>Exposition locale d’un cliché instantané

**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_

L’option de ligne de commande **-El** affecte un dossier monté ou une lettre de lecteur à un cliché instantané persistant. Notez que le contenu du volume restera en lecture seule à moins que vous n’appeliez par la suite **vshadow** **-BW** pour rompre le jeu de clichés instantanés.

> [!Note]  
> Les clichés instantanés non persistants et les [*clichés instantanés accessibles par le client*](vssgloss-c.md) ne peuvent pas être exposés localement.

 

Par exemple, si {edbed95e-7e8d-11D8-9D01-505054503030} est le GUID d’un cliché instantané persistant existant et X : est une lettre de lecteur inutilisée, la commande suivante expose le cliché instantané sous X :

**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, x :**

L’exemple suivant montre comment exposer le même cliché instantané sous le dossier monté C : \\ ShadowCopies \\ June23 :

**mkdir c : \\ ShadowCopies \\ June23**

**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, c : \\ ShadowCopies \\ June23**

L’option de ligne de commande **-El** ne peut pas être combinée avec d’autres options de ligne de commande.

## <a name="exposing-a-shadow-copy-remotely"></a>Exposition à distance d’un cliché instantané

**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

L’option de ligne de commande **-er** assigne un nom de partage en lecture seule au répertoire racine (ou à un sous-répertoire) à partir du cliché instantané. Notez que le contenu du partage restera en lecture seule à moins que vous n’appeliez par la suite **vshadow** **-BW** pour rompre le jeu de clichés instantanés.

> [!Note]  
> [*Les clichés instantanés accessibles par le client*](vssgloss-c.md) ne peuvent pas être exposés à distance.

 

Par exemple, si {edbed95e-7e8d-11D8-9D01-505054503030} est le GUID d’un cliché instantané persistant existant et que \_ le partage 123 est un nom de partage inutilisé, la commande suivante expose le cliché instantané sous le partage \_ 123 :

**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, partage \_ 123**

L’exemple suivant montre comment exposer uniquement une sous-arborescence (nommée « dossier1 \\ dossier2 ») du même cliché instantané sous le même partage :

**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, partage \_ 123, dossier1 \\ dossier2**

L’option de ligne de commande **-er** ne peut pas être combinée avec d’autres options de ligne de commande.

## <a name="listing-writer-status-and-metadata"></a>Affichage de l’État et des métadonnées de l’enregistreur

**vshadow** **-WS**

**vshadow** **-WM**

**vshadow** **-wm2**

**vshadow** **-WM3**

L’option de ligne **de commande-WS** énumère les enregistreurs VSS en cours d’exécution sur l’ordinateur et décrit leur état. Cette commande est l’équivalent de la commande [vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Il existe six valeurs d’État possibles : stable, échec, inconnu, en attente de gel, figé et en attente de la fin de l’opération.

L’option de ligne de commande **-WM** répertorie un résumé des métadonnées de l’enregistreur, y compris les volumes affectés.

L’option de ligne de commande **-wm2** répertorie toutes les métadonnées de l’enregistreur.

L’option de ligne de commande **-WM3** répertorie toutes les métadonnées de l’enregistreur au format XML brut.

**Windows Vista et Windows Server 2003 :** L’option de ligne de commande **-WM3** n’est pas prise en charge.

Vous pouvez utiliser ces informations pour déterminer les volumes à inclure dans le jeu de clichés instantanés de volume.

> [!Note]  
> Si l’état du writer est stable ou en attente de la fin de l’exécution, le writer peut être considéré comme étant dans un état stable, prêt pour la sauvegarde suivante.

 

Les options de ligne de commande **-WS**, **-WM**, **-wm2** et **-WM3** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.

## <a name="performing-restore-operations"></a>Exécution d’opérations de restauration

**vshadow** \[ OptionalFlags \] **-r =**_file_*_. xml_*

**vshadow** \[ OptionalFlags \] **-RS =**_file_*_. xml_*

L’option de ligne **de commande-r** effectue une opération de restauration.

L’option de ligne **de commande-RS** effectue une opération de restauration simulée.

Le fichier de *File.xml* doit être un fichier de document de composants de sauvegarde pour un jeu de clichés instantanés qui a été créé avec l’indicateur facultatif **-t** ou **-BC** .

Les options de ligne de commande **-r** et **-RS** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.

*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.



| Valeur d’indicateur facultative                                                                                                            | Description                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_enregistreur_<br/>             | Cet indicateur facultatif vérifie que l’enregistreur ou le composant spécifié est inclus dans la restauration. L' *enregistreur* peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_enregistreur_<br/>             | Cet indicateur facultatif vérifie que l’enregistreur ou le composant spécifié est exclu de la restauration. L' *enregistreur* peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =,**_commande_<br/> | Cet indicateur facultatif exécute une commande ou un script entre les événements antérieurs et postérieurs à la restauration qui sont envoyés aux enregistreurs. La *commande* peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd. Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-suivi**<br/>                                                  | Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Retour à un cliché instantané précédent

**vshadow** **-Revert =**_ShadowCopyId_

> [!Note]  
> Cette option de ligne de commande est prise en charge uniquement sur les systèmes d’exploitation Windows Server.

 

**Windows server 2008 et Windows server 2003 :** Non pris en charge.

L’option de ligne de commande **-Revert** retourne un volume au cliché instantané précédent dont l’ID est spécifié par *ShadowCopyId*.

L’option de ligne de commande **-Revert** ne peut pas être combinée avec d’autres options de ligne de commande.

## <a name="resynchronizing-luns"></a>Resynchronisation des numéros d’unités logiques

**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

L’option de ligne de commande **-addresync** spécifie les volumes à inclure dans une opération de resynchronisation des numéros d’unités logiques. Le paramètre *ShadowCopyId* spécifie l’identificateur du cliché instantané. Le paramètre facultatif *TargetVolumeDriveLetter* spécifie le volume de destination dans lequel le contenu du volume de clichés instantanés doit être copié.

L’option de ligne de commande **-Resync** lance une opération de resynchronisation des numéros d’unités logiques. Une fois l’opération terminée, la signature de chaque LUN cible doit être identique à celle du numéro d’unité logique du volume cible. Le paramètre *BCDFileName* spécifie le nom du fichier XML qui contient le document du composant de sauvegarde.

> [!Note]  
> Les options de ligne de commande **-addresync** et **-Resync** sont uniquement prises en charge sur les systèmes d’exploitation Windows Server.

 

**Windows server 2008 et Windows server 2003 :** Non pris en charge.

*OptionalResyncFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur d’indicateur facultative</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>Cet indicateur facultatif spécifie qu’une fois l’opération terminée, la signature de chaque LUN cible doit être identique à celle du numéro d’unité logique d’origine qui a été utilisé pour créer le cliché instantané, et non le numéro d’unité logique du volume cible.<br/>
<blockquote>
[!Note]<br />
L’indicateur <strong>-revertsig</strong> est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 et Windows server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Cet indicateur facultatif spécifie que le service VSS ne doit pas vérifier les volumes non sélectionnés qui seraient remplacés par l’opération de resynchronisation des LUN.<br/>
<blockquote>
[!Note]<br />
L’indicateur <strong>-novolcheck</strong> est pris en charge uniquement sur les systèmes d’exploitation Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 et Windows server 2003 :</strong> Non pris en charge.<br/></td>
</tr>
</tbody>
</table>



 

 

 
