---
description: 'En savoir plus sur : JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538712"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_cbtyp"></a>JET_CBTYP

Le **JET_CBTYP** groupe de constantes décrit tous les points possibles d’une opération que le moteur de base de données notifiera à une application en appelant la fonction de rappel [JET_CALLBACK](./jet-callback-callback-function.md) . Le moteur de base de données passe une de ces constantes dans le paramètre *cbtyp* de la fonction de rappel. La signification des autres paramètres passés par le moteur de base de données dans cet appel dépend de la **JET_CBTYP** spécifique passée.

**Windows XP :**  Le **JET_CBTYP** groupe de constantes est introduit dans Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_cbtypNull<br />
0x00000000</p></td>
<td><p>Ce rappel est réservé et toujours considéré comme non valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Ce rappel est réservé pour une utilisation ultérieure.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Ce rappel se produit juste avant l’insertion d’un nouvel enregistrement dans une table par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session qui a l’enregistrement à insérer.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à insérer.</p></li>
<li><p><em>TableID</em>: curseur qui a préparé le nouvel enregistrement à insérer. Il est important de noter que la valeur de toutes les colonnes de version ou d’incrémentation automatique peut être incorrecte pour l’instant.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Ce rappel se produit juste après l’insertion d’un nouvel enregistrement dans une table par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a> mais avant que <a href="gg269288(v=exchg.10).md">JetUpdate</a> retourne à son appelant.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session qui a l’enregistrement qui vient d’être inséré.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être inséré.</p></li>
<li><p><em>TableID</em>: curseur sur la table dans lequel l’enregistrement qui vient d’être inséré. Notez que le curseur est toujours positionné sur la même entrée d’index que dans le rappel Before Insert. Notez que cette entrée d’index ne peut pas être associée à l’enregistrement en cours d’insertion.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, elle sera ignorée.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Ce rappel se produit juste avant un enregistrement existant dans une table en cours de modification par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session dont l’enregistrement doit être modifié.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à modifier.</p></li>
<li><p><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement à modifier. Il est important de noter que la valeur de toutes les colonnes de version ou d’incrémentation automatique peut être incorrecte pour l’instant.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Ce rappel se produit juste après qu’un enregistrement existant dans une table a été modifié par un appel à <a href="gg269288(v=exchg.10).md">JetUpdate</a> mais avant le retour de <a href="gg269288(v=exchg.10).md">JetUpdate</a> à son appelant.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session qui a l’enregistrement qui vient d’être modifié.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être modifié.</p></li>
<li><p><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement qui vient d’être modifié.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, elle sera ignorée.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Ce rappel se produit juste avant qu’un enregistrement existant dans une table ne soit supprimé par un appel à <a href="gg269315(v=exchg.10).md">JetDelete</a>.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session qui a l’enregistrement à supprimer.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement à supprimer.</p></li>
<li><p><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement à supprimer.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si une erreur est retournée par le rappel, l’opération à l’origine du rappel échoue avec cette erreur.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Ce rappel se produit juste après qu’un enregistrement existant dans une table a été supprimé par un appel à <a href="gg269315(v=exchg.10).md">JetDelete</a> mais avant que <a href="gg269315(v=exchg.10).md">JetDelete</a> retourne à son appelant.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou est configuré au moment de l’exécution par le biais de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Pour plus d’informations, consultez <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session qui a l’enregistrement qui vient d’être supprimé.</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient l’enregistrement qui vient d’être supprimé.</p></li>
<li><p><em>TableID</em>: curseur positionné sur une entrée d’index associée à l’enregistrement qui vient d’être supprimé.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: pointeur de contexte passé à <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si une erreur est retournée par le rappel, elle sera ignorée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Ce rappel se produit lorsque le moteur doit récupérer la valeur par défaut définie par l’utilisateur d’une colonne à partir de l’application. Ce rappel est essentiellement une implémentation limitée de <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> qui est évaluée par l’application. Un maximum de valeur de colonne peut être retourné pour une valeur par défaut définie par l’utilisateur.</p>
<p>Le pointeur de fonction pour cette raison de rappel est soit passé à <a href="gg294122(v=exchg.10).md">JetAddColumn</a> au moyen d’une structure de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , soit passé à <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> au moyen d’une structure de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> dans une structure de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dans une structure de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: la session qui calcule la valeur par défaut définie par l’utilisateur</p></li>
<li><p><em>dbid</em>: ID de base de données de la table qui contient la valeur par défaut définie par l’utilisateur.</p></li>
<li><p><em>TableID</em>: curseur positionné sur l’enregistrement pour lequel la valeur par défaut définie par l’utilisateur est Récupérée</p></li>
<li><p><em>pvArg1</em>: mémoire tampon de sortie pour la valeur par défaut définie par l’utilisateur</p></li>
<li><p><em>pvArg2</em>: en entrée, il s’agit de la taille de la mémoire tampon de sortie. En sortie, il s’agit de la taille réelle de la valeur par défaut définie par l’utilisateur. dans les deux cas, la taille est un entier non signé 32 bits.</p></li>
<li><p><em>pvContext</em>: pointeur vers une mémoire tampon contenant les données utilisateur spécifiées dans la structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> lorsque la colonne a été créée ou null si aucun contexte n’a été fourni.</p></li>
<li><p><em>ulUnused</em>: ID de colonne de la colonne pour laquelle la valeur par défaut définie par l’utilisateur est récupérée.</p></li>
</ul>
<p>Si une erreur est retournée par le rappel, l’opération à l’origine du rappel échouera avec cette erreur.</p>
<p>Si JET_wrnBufferTruncated est retourné par le rappel, l’opération se poursuit, mais la valeur entière n’est pas récupérée pendant le rappel.</p>
<p>Si JET_wrnColumnNull est retourné par le rappel, l’opération se poursuit, mais la valeur par défaut définie par l’utilisateur pour la colonne est NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Ce rappel se produit lorsque la défragmentation en ligne d’une base de données telle qu’elle est lancée par <a href="gg269317(v=exchg.10).md">JetDefragment</a> s’est arrêtée en raison de l’exécution du processus ou de la limite de temps atteinte.</p>
<p>Le pointeur de fonction pour cette raison de rappel est passé à <a href="gg269317(v=exchg.10).md">JetDefragment</a>. Pour plus d’informations, consultez <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: session utilisée pour effectuer une défragmentation en ligne de la base de données ou JET_sesidNil pour un fichier de streaming.</p></li>
<li><p><em>dbid</em>: ID de base de données de la base de données en cours de défragmentation ou JET_dbidNil pour un fichier de streaming.</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si une erreur est retournée par le rappel, elle sera ignorée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Ce rappel se produit lorsque l’application doit nettoyer le descripteur de contexte pour le stockage local associé à un curseur libéré par le moteur de base de données. Pour plus d’informations, consultez <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Le pointeur de fonction pour cette raison de rappel est configuré au moyen de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: descripteur de contexte défini à l’aide de <a href="gg269243(v=exchg.10).md">JetSetLS</a></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si une erreur est retournée par le rappel, elle sera ignorée.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Ce rappel se produit en raison de la nécessité pour l’application de nettoyer le descripteur de contexte pour le stockage local associé à une table qui est publiée par le moteur de base de données. Pour plus d’informations, consultez <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Le pointeur de fonction pour cette raison de rappel est configuré au moyen de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Les paramètres de rappel auront les valeurs suivantes :</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: descripteur de contexte défini à l’aide de <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si une erreur est retournée par le rappel, elle sera ignorée.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)
