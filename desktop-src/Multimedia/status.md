---
title: commande Status
description: La commande status demande des informations d’État à partir d’un appareil. Tous les appareils reconnaissent cette commande.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- commande d’état Windows multimédia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119454"
---
# <a name="status-command"></a>commande Status

> [!NOTE]
> Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.  Dans ce document, il existe des références au mot « esclave ». Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.  Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes. Pour des fins de cohérence, ce document contient ce mot. Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.

La commande status demande des informations d’État à partir d’un appareil. Tous les appareils reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Indicateur de demande d’informations d’État. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Status** et les indicateurs utilisés par chaque type.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type d’appareil</th>
<th>Indicateurs de demande</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li><em>numéro</em> de suivi de type cdaudio</li>
<li>piste actuelle</li>
<li>length</li>
<li><em>nombre</em> de pistes de longueur</li>
<li>support présent</li>
<li>mode</li>
<li>nombre de pistes</li>
<li>position</li>
<li><em>numéro</em> de piste de position</li>
<li>ready</li>
<li>position de départ</li>
<li>format horaire</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>audio</li>
<li>alignement audio</li>
<li>BitsPerSample audio</li>
<li>sauts audio</li>
<li>bytespersec audio</li>
<li>entrée audio</li>
<li>enregistrement audio</li>
<li>source audio</li>
<li>SamplesPerSec audio</li>
<li>flux audio</li>
<li>graves</li>
<li>bitsperpel</li>
<li>luminosité</li>
<li>color</li>
<li>élevé</li>
<li>piste actuelle</li>
<li><em>lecteur</em> d’espace disque</li>
<li>saisie semi-automatique des fichiers</li>
<li>format de fichier</li>
<li>mode de fichier</li>
<li>forward</li>
<li>frames ignorés</li>
<li>gamma</li>
<li>entrée</li>
<li>volume de gauche</li>
<li>length</li>
<li><em>nombre</em> de pistes de longueur</li>
<li>support présent</li>
<li>mode</li>
<li>monitor</li>
<li>méthode Monitor</li>
<li>minime</li>
<li>fréquence d’images nominales</li>
<li>fréquence des images d’enregistrement nominales</li>
<li>nombre de pistes</li>
<li>sortie</li>
<li>handle de palette</li>
<li>mode pause</li>
<li>Vitesse de lecture</li>
<li>position</li>
<li><em>numéro</em> de piste de position</li>
<li>ready</li>
<li>fréquence des trames d’enregistrement</li>
<li><em>Frame</em> de référence</li>
<li>taille réservée</li>
<li>volume approprié</li>
<li>Rechercher exactement</li>
<li>netteté</li>
<li>intégrant</li>
<li>speed</li>
<li>position de départ</li>
<li>format de fichier toujours</li>
<li>format horaire</li>
<li>teinté</li>
<li>les aigus</li>
<li>non enregistrées</li>
<li>video</li>
<li>index de clé vidéo</li>
<li>couleur de la touche vidéo</li>
<li>enregistrement vidéo</li>
<li>source vidéo</li>
<li>Numéro de la source vidéo</li>
<li>flux vidéo</li>
<li>volume</li>
<li>handle de fenêtre</li>
<li>fenêtre visible</li>
<li>fenêtre réduite</li>
<li>fenêtre agrandie</li>
</ul></td>
</tr>
<tr class="odd">
<td>superposition</td>
<td><ul>
<li>support présent</li>
<li>mode</li>
<li>nombre de pistes</li>
<li>ready</li>
<li>étirement</li>
<li>handle de fenêtre</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>piste actuelle</li>
<li>type de division</li>
<li>length</li>
<li>longueur du <em>numéro</em> de suivi de la longueur</li>
<li>support présent</li>
<li>mode</li>
<li>nombre de pistes</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li><em>numéro</em> de piste de position</li>
<li>ready</li>
<li>subordonné</li>
<li>position de départ</li>
<li>tempo</li>
<li>format horaire</li>
</ul></td>
</tr>
<tr class="odd">
<td>vidéo</td>
<td><ul>
<li>enregistrement d’assemblage</li>
<li>moniteur audio</li>
<li>Numéro de moniteur audio</li>
<li>enregistrement audio</li>
<li><em>numéro</em> de piste d’enregistrement audio</li>
<li>source audio</li>
<li>Numéro de la source audio</li>
<li>channel</li>
<li><em>numéro</em> de récepteur de canal</li>
<li>horloge</li>
<li>ID de l’horloge</li>
<li>counter</li>
<li>format du compteur</li>
<li>résolution de compteur</li>
<li>piste actuelle</li>
<li>fréquence d’images</li>
<li>index</li>
<li>index sur</li>
<li>length</li>
<li><em>nombre</em> de pistes de longueur</li>
<li>support présent</li>
<li>type de média</li>
<li>mode</li>
<li>nombre de pistes audio</li>
<li>nombre de pistes</li>
<li>nombre de pistes vidéo</li>
<li><em>délai d’attente</em> de pause</li>
<li>format de lecture</li>
<li>position</li>
<li>début de la position</li>
<li><em>numéro</em> de piste de position</li>
<li><em>durée</em> de Postroll</li>
<li>Sous tension</li>
<li><em>durée</em> du préroll</li>
<li>ready</li>
<li>format d’enregistrement</li>
<li>speed</li>
<li>format horaire</li>
<li>mode heure</li>
<li>type de temps</li>
<li>code temporel présent</li>
<li>enregistrement du code temporel</li>
<li>type de code temporel</li>
<li>Numéro de tuner</li>
<li>moniteur vidéo</li>
<li>Numéro du moniteur vidéo</li>
<li>enregistrement vidéo</li>
<li><em>numéro</em> de piste de l’enregistrement vidéo</li>
<li>source vidéo</li>
<li>Numéro de la source vidéo</li>
<li>protégé en écriture</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>piste actuelle</li>
<li>taille du disque</li>
<li>forward</li>
<li>length</li>
<li><em>nombre</em> de pistes de longueur</li>
<li>support présent</li>
<li>type de média</li>
<li>mode</li>
<li>nombre de pistes</li>
<li>position</li>
<li><em>numéro</em> de piste de position</li>
<li>ready</li>
<li>initi</li>
<li>speed</li>
<li>position de départ</li>
<li>format horaire</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li>alignement</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>channels</li>
<li>piste actuelle</li>
<li>balise de format</li>
<li>entrée</li>
<li>length</li>
<li><em>nombre</em> de pistes de longueur</li>
<li>niveau</li>
<li>support présent</li>
<li>mode</li>
<li>nombre de pistes</li>
<li>sortie</li>
<li>position</li>
<li><em>numéro</em> de piste de position</li>
<li>ready</li>
<li>samplespersec</li>
<li>position de départ</li>
<li>format horaire</li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRequest** et leurs significations.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>alignement</td>
<td>Retourne l’alignement de bloc des données, en octets.</td>
</tr>
<tr class="even">
<td>enregistrement d’assemblage</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil est configuré pour l’enregistrement en mode d’assemblage.</td>
</tr>
<tr class="odd">
<td>audio</td>
<td>Retourne &quot; on &quot; ou &quot; OFF &quot; selon la commande <a href="setaudio.md">SetAudio</a> &quot; on &quot; ou OFF la plus &quot; récente &quot; . Elle retourne la valeur &quot; &quot; si un ou les deux enceintes sont activées, et &quot; désactivent dans le &quot; cas contraire.</td>
</tr>
<tr class="even">
<td>alignement audio</td>
<td>Retourne l’alignement des blocs de données par rapport au début des données Waveform-Audio en entrée.</td>
</tr>
<tr class="odd">
<td>BitsPerSample audio</td>
<td>Retourne le nombre de bits par échantillon que l’appareil utilise pour l’enregistrement. Cet indicateur s’applique uniquement aux appareils prenant en charge l' &quot; &quot; algorithme PCM.</td>
</tr>
<tr class="even">
<td>sauts audio</td>
<td>Retourne le nombre de fois que la partie audio de la dernière séquence AVI a été interrompue. Le système compte un saut audio chaque fois qu’il tente d’écrire des données audio sur le pilote de périphérique et découvre que le pilote a déjà lu toutes les données disponibles. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI. Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</td>
</tr>
<tr class="odd">
<td>bytespersec audio</td>
<td>Retourne le nombre moyen d’octets par seconde utilisés pour l’enregistrement.</td>
</tr>
<tr class="even">
<td>entrée audio</td>
<td>Retourne le niveau audio instantané approximatif du signal audio d’entrée analogique. Une valeur supérieure à 1000 implique une déformation de découpage. Certains appareils peuvent retourner cette valeur uniquement lors de l’enregistrement audio. La valeur n’a pas de commande <a href="set.md">Set</a> ou <a href="setaudio.md">SetAudio</a> associée.</td>
</tr>
<tr class="odd">
<td>moniteur audio</td>
<td>Retourne &quot; &quot; la sortie ou l’un des types d’entrée source valides. Pour plus d’informations, consultez la commande <strong>SetAudio</strong> &quot; Monitor &quot; .</td>
</tr>
<tr class="even">
<td>Numéro de moniteur audio</td>
<td>Retourne le numéro vidéo surveillée du type spécifié par le moniteur d' <strong>État</strong> &quot; audio &quot; . Pour plus d’informations, consultez la commande <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="odd">
<td>enregistrement audio</td>
<td>Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état défini par l’enregistrement <strong>SetAudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>numéro</em> de piste d’enregistrement audio</td>
<td>Renvoie la <strong>valeur true</strong> si le magnétoscope est configuré pour enregistrer l’audio. Si aucun numéro de piste n’est indiqué, la valeur par défaut de 1 est utilisée.</td>
</tr>
<tr class="odd">
<td>SamplesPerSec audio</td>
<td>Retourne le nombre d’échantillons par seconde enregistrés.</td>
</tr>
<tr class="even">
<td>source audio</td>
<td>Retourne la source de digitaliseur audio actuelle : &quot; gauche &quot; , &quot; droite &quot; , &quot; moyenne &quot; ou &quot; stéréo &quot; .</td>
</tr>
<tr class="odd">
<td>Numéro de la source audio</td>
<td>Retourne le numéro de source audio du type retourné par la <strong></strong> &quot; source audio d’état &quot; . Pour plus d’informations, consultez la commande <a href="setaudio.md">SetAudio</a> .</td>
</tr>
<tr class="even">
<td>flux audio</td>
<td>Retourne le numéro du flux audio actuel.</td>
</tr>
<tr class="odd">
<td>graves</td>
<td>Retourne le niveau audio-Bass actuel.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Retourne le nombre de bits par pixel pour l’enregistrement des données capturées ou enregistrées.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Retourne les bits par échantillon.</td>
</tr>
<tr class="even">
<td>luminosité</td>
<td>Retourne le niveau de luminosité vidéo actuel.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Retourne le nombre moyen d’octets par seconde lus ou enregistrés.</td>
</tr>
<tr class="even">
<td><em>numéro</em> de suivi de type cdaudio</td>
<td>Retourne le type du numéro de piste spécifié. Il peut s’agir &quot; de l’audio ou d’un &quot; &quot; autre.&quot;</td>
</tr>
<tr class="odd">
<td>channel</td>
<td>Retourne la valeur entière du canal défini sur le tuner.</td>
</tr>
<tr class="even">
<td><em>numéro</em> de récepteur de canal</td>
<td>Si &quot; le &quot; <em>numéro</em> de tuner est donné, le canal actuellement sélectionné sur le <em>numéro</em> de tuner logique est retourné. Notez qu’il peut y avoir plusieurs tuners logiques.</td>
</tr>
<tr class="odd">
<td>channels</td>
<td>Retourne le nombre de canaux définis (1 pour mono, 2 pour stéréo).</td>
</tr>
<tr class="even">
<td>horloge</td>
<td>Retourne l’heure externe. L’heure doit être un entier long non signé exprimant des incréments totaux. Pour plus d’informations, consultez la commande vitesse d’incrément de l’horloge de <a href="capability.md">capacité</a> &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>ID de l’horloge</td>
<td>Retourne un entier unique identifiant l’horloge.</td>
</tr>
<tr class="even">
<td>color</td>
<td>Retourne le niveau de couleur actuel.</td>
</tr>
<tr class="odd">
<td>élevé</td>
<td>Retourne le niveau de contraste actuel.</td>
</tr>
<tr class="even">
<td>counter</td>
<td>Retourne la position du compteur dans le format de compteur actuel.</td>
</tr>
<tr class="odd">
<td>format du compteur</td>
<td>Retourne le format de compteur actuel. Pour plus d’informations, consultez la commande <a href="set.md">Set</a> &quot; Counter format &quot; .</td>
</tr>
<tr class="even">
<td>résolution de compteur</td>
<td>Retourne des &quot; images &quot; ou des &quot; secondes &quot; , indiquant la résolution du compteur. Ce n’est pas la même chose que la précision.</td>
</tr>
<tr class="odd">
<td>piste actuelle</td>
<td>Retourne la piste actuelle. MCISEQ Sequencer retourne 1.</td>
</tr>
<tr class="even">
<td>taille du disque</td>
<td>Retourne 8 ou 12, indiquant la taille du disque chargé, en pouces.</td>
</tr>
<tr class="odd">
<td><em>lecteur</em> d’espace disque</td>
<td>Retourne l’espace disque approximatif, dans le format d’heure actuel, qui peut être obtenu par une commande <a href="reserve.md">Reserve</a> pour le lecteur de disque spécifié <em>.</em> Le <em>lecteur</em> est généralement spécifié sous la forme d’une lettre unique ou d’une lettre suivie d’un signe deux-points ( :). Certains appareils peuvent toutefois utiliser un chemin d’accès.</td>
</tr>
<tr class="even">
<td>type de division</td>
<td>Retourne l’un des types de divisions de fichier suivants :
<ul>
<li>PPQN</li>
<li>Cadre SMPTE 24</li>
<li>Cadre SMPTE 25</li>
<li>Trame de dépôt SMPTE 30</li>
<li>Trame de 30 SMPTE</li>
</ul>
<br/> Utilisez ces informations pour déterminer le format du fichier MIDI et la signification des informations relatives au tempo et à la position.<br/></td>
</tr>
<tr class="odd">
<td>saisie semi-automatique des fichiers</td>
<td>Retourne le pourcentage estimé pendant lequel l’opération de <a href="load.md">chargement</a>, d' <a href="save.md">enregistrement</a>, de <a href="capture.md">capture</a>, de <a href="cut.md">couper</a>, de <a href="copy.md">copier</a>, de <a href="delete.md">suppression</a>, de <a href="paste.md">Collage</a>ou d' <a href="undo.md">annulation</a> a progressé. (Les applications peuvent l’utiliser pour fournir un indicateur visuel de la progression.)</td>
</tr>
<tr class="even">
<td>format de fichier</td>
<td>Retourne le format de fichier actuel pour les <strong>commandes d'</strong> <a href="record.md">enregistrement</a> ou d’enregistrement.</td>
</tr>
<tr class="odd">
<td>mode de fichier</td>
<td>Retourne le &quot; chargement &quot; , &quot; l’enregistrement &quot; , la &quot; modification ou l' &quot; &quot; inactivité &quot; . Pendant une opération de <a href="load.md"><strong>chargement</strong></a> , elle retourne le &quot; chargement &quot; . Lors des opérations d' <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>enregistrement</strong></a> et de <a href="capture.md"><strong>capture</strong></a> , &quot; l’enregistrement est retourné &quot; . Pendant les opérations <a href="cut.md"><strong>couper</strong></a>, <a href="copy.md"><strong>copier</strong></a>, <a href="delete.md"><strong>supprimer</strong></a>, <a href="paste.md"><strong>coller</strong></a>ou <a href="undo.md"><strong>Annuler</strong></a> , retourne la &quot; modification &quot; .</td>
</tr>
<tr class="even">
<td>balise de format</td>
<td>Retourne la balise de format.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Retourne la <strong>valeur true</strong> si le sens de lecture est vers l’avant ou si l’appareil n’est pas en train de jouer.</td>
</tr>
<tr class="even">
<td>fréquence d’images</td>
<td>Retourne le nombre d’images par seconde que l’appareil doit utiliser par défaut. Les appareils NTSC renvoient 30, PAL 25, etc.</td>
</tr>
<tr class="odd">
<td>frames ignorés</td>
<td>Retourne le nombre de frames qui n’ont pas été dessinés lors de la lecture de la dernière séquence AVI. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI. Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Retourne la valeur définie avec <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma à &quot; <em>value</em>.</td>
</tr>
<tr class="odd">
<td>index</td>
<td>Retourne l’affichage actuel de l’index. Pour plus d’informations, consultez la commande <a href="set.md"><strong>Set</strong></a> &quot; index &quot; .</td>
</tr>
<tr class="even">
<td>index sur</td>
<td>Retourne la <strong>valeur true</strong> si l’index est activé.</td>
</tr>
<tr class="odd">
<td>entrée</td>
<td>Retourne le jeu de données d’entrée. Si aucune valeur n’est définie, l’erreur retournée indique que n’importe quel appareil peut être utilisé. Pour les périphériques vidéo numériques, modifie les &quot; basses &quot; , les &quot; aigus &quot; , le &quot; volume, la &quot; &quot; luminosité, la &quot; &quot; couleur, le &quot; &quot; contraste, la &quot; &quot; gamma, la &quot; &quot; netteté &quot; ou &quot; &quot; l’indicateur de teinte afin qu’elle s’applique uniquement à l’entrée. Il s’agit de la valeur par défaut lors de l’analyse de l’entrée.</td>
</tr>
<tr class="even">
<td>volume de gauche</td>
<td>Retourne le volume défini pour le canal audio de gauche.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Retourne la longueur totale du média, au format d’heure actuel. Pour les fichiers PPQN, la longueur est retournée dans les unités du pointeur de la chanson. Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames. Pour les périphériques VCR, la longueur est de 2 heures (sauf si la longueur a été explicitement modifiée à l’aide de la commande <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> ).</td>
</tr>
<tr class="even">
<td><em>nombre</em> de pistes de longueur</td>
<td>Retourne la longueur de la piste, en temps ou en images, spécifiée par <em>nombre</em>. Pour les fichiers PPQN, la longueur est retournée dans les unités du pointeur de la chanson. Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames.<br/></td>
</tr>
<tr class="odd">
<td>niveau</td>
<td>Retourne l’exemple de valeur audio PCM actuelle.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Retourne &quot; midi &quot; , &quot; None &quot; ou &quot; SMPTE &quot; selon le type de jeu de synchronisation.</td>
</tr>
<tr class="odd">
<td>support présent</td>
<td>Retourne la <strong>valeur true</strong> si le média est inséré dans l’appareil ou <strong>false</strong> dans le cas contraire. Les périphériques Sequencer, Video-Overlay, Digital-Video et Waveform-Audio renvoient la <strong>valeur true</strong>.</td>
</tr>
<tr class="even">
<td>type de média</td>
<td>Retourne le type du média. Pour les MAGNÉTOSCOPEs, il s’agit de &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; ou &quot; autre &quot; . Pour videodiscs, il s’agit de &quot; CAV &quot; , &quot; CLV &quot; ou &quot; other &quot; , selon le type de videodisc.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Retourne le mode actuel de l’appareil. Tous les appareils peuvent retourner les &quot; valeurs non prêt &quot; , &quot; suspendu &quot; , &quot; lecture &quot; et &quot; arrêté &quot; . Certains appareils peuvent renvoyer les valeurs supplémentaires ouvertes, imposées &quot; &quot; &quot; &quot; , &quot; d’enregistrement &quot; et de &quot; recherche &quot; .</td>
</tr>
<tr class="even">
<td>monitor</td>
<td>Retourne le &quot; fichier &quot; ou l' &quot; entrée &quot; . La valeur retournée indique la source de présentation actuelle.</td>
</tr>
<tr class="odd">
<td>méthode Monitor</td>
<td>Retourne &quot; pre &quot; , &quot; poster &quot; ou &quot; direct &quot; . La valeur retournée indique la méthode utilisée pour la surveillance d’entrée.</td>
</tr>
<tr class="even">
<td>minime</td>
<td>L’élément modifie les &quot; &quot; indicateurs de basses, de &quot; luminosité &quot; , de &quot; couleur &quot; , de &quot; contraste, de &quot; &quot; gamma, de netteté, de &quot; teinte, de &quot; &quot; &quot; &quot; &quot; aigu et de &quot; &quot; volume &quot; pour retourner la valeur nominale au lieu du paramètre actuel.</td>
</tr>
<tr class="odd">
<td>fréquence d’images nominales</td>
<td>Retourne la fréquence d’images nominales associée au fichier. Les unités sont en images par seconde, multiplié par 1000.</td>
</tr>
<tr class="even">
<td>fréquence des images d’enregistrement nominales</td>
<td>Retourne la fréquence d’images nominales associée au signal vidéo d’entrée. Les unités sont en images par seconde, multiplié par 1000.</td>
</tr>
<tr class="odd">
<td>nombre de pistes audio</td>
<td>Retourne le nombre de pistes audio sur le support.</td>
</tr>
<tr class="even">
<td>nombre de pistes</td>
<td>Retourne le nombre de pistes sur le média. Les appareils MCISEQ et MCIWAVE retournent 1, comme le font la plupart des périphériques VCR. L’appareil MCIPIONR ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="odd">
<td>nombre de pistes vidéo</td>
<td>Retourne le nombre de pistes vidéo sur le support.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Retourne le décalage d’un fichier basé sur une SMPTE. Le décalage est l’heure de début d’une séquence basée sur SMPTE. L’heure est retournée sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> est hours, <em>mm</em> correspond à minutes, <em>SS</em> à secondes et <em>FF</em> à la trame.</td>
</tr>
<tr class="odd">
<td>sortie</td>
<td>Retourne la sortie actuellement définie. Si aucune sortie n’est définie, l’erreur retournée indique que tous les appareils peuvent être utilisés. Pour les périphériques vidéo numériques, modifie les &quot; basses &quot; , les &quot; aigus &quot; , le &quot; volume, la &quot; &quot; luminosité, la &quot; &quot; couleur, le &quot; &quot; contraste, la &quot; &quot; gamma, la &quot; &quot; netteté &quot; ou &quot; &quot; l’indicateur de teinte afin qu’elle s’applique uniquement à la sortie. Il s’agit de la valeur par défaut lors de l’analyse d’un fichier.</td>
</tr>
<tr class="even">
<td>mode pause</td>
<td>Retourne l' &quot; enregistrement &quot; si l’appareil est mis en pause pendant l’enregistrement. Elle retourne &quot; &quot; la valeur si l’appareil est en pause pendant la durée de la diffusion. Elle retourne l' &quot; action d’erreur non applicable en mode actuel &quot; si l’appareil n’est pas suspendu.</td>
</tr>
<tr class="odd">
<td>délai d’attente de pause</td>
<td>Retourne la durée maximale, en millisecondes, d’une commande d' <a href="pause.md"><strong>interruption</strong></a> .</td>
</tr>
<tr class="even">
<td>format de lecture</td>
<td>Retourne un code qui indique le format de lecture des cassettes vidéo, s’il est détectable : &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; autre &quot; . Pour plus d’informations, consultez l' &quot; indicateur de format d’enregistrement &quot; .</td>
</tr>
<tr class="odd">
<td>Vitesse de lecture</td>
<td>Retourne une valeur représentant la différence entre la durée de l’exécution réelle de la dernière séquence AVI et la durée d’exécution de la cible. La valeur 1000 indique que l’heure cible et l’heure réelle étaient les mêmes. Une valeur de 2000, par exemple, indique que la séquence AVI prenait deux fois plus de temps que nécessaire. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI. Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Retourne le numéro de port MIDI affecté à la séquence.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Retourne la position actuelle. Pour les fichiers PPQN, la position est retournée dans les unités du pointeur de la chanson. Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, SS à secondes et <em>FF</em> à des trames.<br/></td>
</tr>
<tr class="even">
<td>début de la position</td>
<td>Retourne la position du début du média utilisable.</td>
</tr>
<tr class="odd">
<td><em>numéro</em> de piste de position</td>
<td>Retourne la position du début de la piste spécifiée par <em>nombre</em>. Pour les fichiers PPQN, le format d’heure est retourné dans les unités du pointeur de la chanson. Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames. MCISEQ Sequencer retourne zéro. L’appareil MCIPIONR ne prend pas en charge cet indicateur. L’appareil MCIWAVE retourne la valeur zéro.</td>
</tr>
<tr class="even">
<td>durée de Postroll</td>
<td>Retourne la longueur des cassettes vidéo au format de l’heure actuelle, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande <a href="stop.md"><strong>Stop</strong></a> ou <a href="pause.md"><strong>Pause</strong></a> .</td>
</tr>
<tr class="odd">
<td>Sous tension</td>
<td>Retourne la <strong>valeur true</strong> si la mise sous tension du magnétoscope est activée.</td>
</tr>
<tr class="even">
<td>durée du préroll</td>
<td>Retourne la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour stabiliser la sortie du magnétoscope.</td>
</tr>
<tr class="odd">
<td>ready</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil est prêt à accepter une autre commande.</td>
</tr>
<tr class="even">
<td>format d’enregistrement</td>
<td>Retourne un code qui indique le format dans lequel les cassettes vidéo seront enregistrées. Les types de retour actuels sont &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; autre &quot; . Ces formats ne sont pas spécifiques à la SHV et peuvent être appliqués à n’importe quel magnétoscope ayant plusieurs formats d’enregistrement sélectionnables. Le &quot; type de processeur &quot; de stockage est le format d’enregistrement de qualité le plus rapide et le plus élevé. il est utilisé par défaut sur les magnétoscopes à format unique.</td>
</tr>
<tr class="odd">
<td>fréquence des trames d’enregistrement</td>
<td>Retourne la fréquence d’images, en images par seconde, multiplié par 1000, utilisée pour la compression.</td>
</tr>
<tr class="even">
<td><em>Frame</em> de référence</td>
<td>Retourne le numéro de frame de l’image de l’image clé la plus proche qui précède le <em>cadre</em>spécifié.</td>
</tr>
<tr class="odd">
<td>taille réservée</td>
<td>Retourne la taille, dans le format d’heure actuel, de l’espace de travail réservé. La taille correspond au temps approximatif nécessaire pour lire les données compressées à partir d’un espace de travail complet. Elle retourne zéro s’il n’y a pas d’espace disque réservé. Cet indicateur retourne la taille approximative car l’espace disque précis pour les données compressées ne peut pas, en général, être prédit tant que les données n’ont pas été compressées.</td>
</tr>
<tr class="even">
<td>volume approprié</td>
<td>Retourne le volume défini pour le canal audio de droite.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Retourne le nombre d’échantillons par seconde lus ou enregistrés.</td>
</tr>
<tr class="even">
<td>Rechercher exactement</td>
<td>Retourne &quot; on &quot; ou &quot; OFF &quot; , indiquant si l' &quot; indicateur Seek exact &quot; est défini.</td>
</tr>
<tr class="odd">
<td>netteté</td>
<td>Retourne le niveau de netteté actuel de l’appareil.</td>
</tr>
<tr class="even">
<td>initi</td>
<td>Retourne 1 ou 2 pour indiquer le côté du videodisc à charger.</td>
</tr>
<tr class="odd">
<td>subordonné</td>
<td>Retourne &quot; fichier &quot; , &quot; midi &quot; , &quot; aucun &quot; ou &quot; SMPTE &quot; selon le type de jeu de synchronisation.</td>
</tr>
<tr class="even">
<td>intégrant</td>
<td>Retourne le code temporel SMPTE associé à la position actuelle dans l’espace de travail. Il s’agit d’une chaîne au format <em>JJ : JJ : JJ : JJ</em>, où chaque <em>d</em> désigne un chiffre compris entre 0 et 9. Si les données de l’espace de travail n’incluent pas de données de code temporel, cet indicateur retourne 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>speed</td>
<td>Retourne la vitesse actuelle de l’appareil en images par seconde (ou dans le même format que celui utilisé par la commande <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> &quot; Speed &quot; ). MCIPIONR videodisc Player ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td>position de départ</td>
<td>Retourne la position de départ du média.</td>
</tr>
<tr class="odd">
<td>format de fichier toujours</td>
<td>Retourne le format de fichier actuel pour la commande de <a href="capture.md"><strong>capture</strong></a> .</td>
</tr>
<tr class="even">
<td>étirement</td>
<td>Retourne la <strong>valeur true</strong> si l’étirement est activé.</td>
</tr>
<tr class="odd">
<td>tempo</td>
<td>Retourne le tempo actuel d’une séquence MIDI dans le format d’heure actuel. Pour les fichiers avec le format PPQN, le tempo est en temps par minute. Pour les fichiers avec le format SMPTE, le tempo est en images par seconde.</td>
</tr>
<tr class="even">
<td>format horaire</td>
<td>Retourne le format d’heure actuel. Pour plus d’informations, consultez les formats d’heure dans la commande <a href="set.md"><strong>Set</strong></a> .</td>
</tr>
<tr class="odd">
<td>mode heure</td>
<td>Retourne le mode de l’heure de la position actuelle. Il peut s’agir de la &quot; détection &quot; , du &quot; code temporel &quot; ou du &quot; compteur &quot; .</td>
</tr>
<tr class="even">
<td>type de temps</td>
<td>Retourne l’heure de la position actuelle en cours d’utilisation : &quot; code temporel &quot; ou &quot; compteur &quot; .</td>
</tr>
<tr class="odd">
<td>code temporel présent</td>
<td>Retourne la <strong>valeur true</strong> si le code temporel a été enregistré à la position actuelle sur la bande. Le code temporel doit avancer à partir de la position actuelle. Il peut être nécessaire de lire un magnétoscope pour vérifier cette condition.</td>
</tr>
<tr class="even">
<td>enregistrement du code temporel</td>
<td>Renvoie la <strong>valeur true</strong> si le magnétoscope est défini pour enregistrer le code temporel.</td>
</tr>
<tr class="odd">
<td>type de code temporel</td>
<td>Retourne &quot; SMPTE &quot; , la &quot; suppression SMPTE &quot; , &quot; other &quot; ou &quot; None &quot; . Notez que les images par seconde peuvent être obtenues à partir de la &quot; commande fréquence des trames d’État et que la &quot; précision de l’appareil peut être retournée par la commande de précision de la <a href="capability.md"><strong>fonction</strong></a> &quot; Seek &quot; .</td>
</tr>
<tr class="even">
<td>teinté</td>
<td>Retourne le niveau de teinte vidéo actuel.</td>
</tr>
<tr class="odd">
<td>les aigus</td>
<td>Retourne le niveau des aigus audio actuels.</td>
</tr>
<tr class="even">
<td>Numéro de tuner</td>
<td>Retourne le numéro de tuner logique actuel.</td>
</tr>
<tr class="odd">
<td>non enregistrées</td>
<td>Retourne la <strong>valeur true</strong> s’il y a des données enregistrées dans l’espace de travail qui peuvent être perdues à la suite d’une commande de <a href="close.md"><strong>fermeture</strong></a>, de <a href="load.md"><strong>chargement</strong></a>, d' <a href="record.md"><strong>enregistrement</strong></a>, de <a href="reserve.md"><strong>réserve</strong></a>, de <a href="cut.md"><strong>coupure</strong></a>, de <a href="delete.md"><strong>suppression</strong></a>ou de <a href="paste.md"><strong>Collage</strong></a> . Sinon, retourne <strong>false</strong> .</td>
</tr>
<tr class="even">
<td>video</td>
<td>Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état défini par la commande <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="odd">
<td>couleur de la touche vidéo</td>
<td>Retourne la valeur de la couleur de la clé.</td>
</tr>
<tr class="even">
<td>index de clé vidéo</td>
<td>Retourne la valeur de l’index de clé.</td>
</tr>
<tr class="odd">
<td>moniteur vidéo</td>
<td>Retourne &quot; &quot; la sortie ou l’un des types d’entrée source valides. Pour plus d’informations, consultez la commande <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Monitor &quot; .</td>
</tr>
<tr class="even">
<td>Numéro du moniteur vidéo</td>
<td>Retourne le numéro vidéo surveillée du type retourné par le &quot; moniteur vidéo d’état &quot; . Pour plus d’informations, consultez la commande <a href="setvideo.md">setvideo</a> .</td>
</tr>
<tr class="odd">
<td>enregistrement vidéo</td>
<td>Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état actuel défini par l’enregistrement <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>numéro</em> de piste de l’enregistrement vidéo</td>
<td>Retourne la <strong>valeur true</strong> si le magnétoscope est configuré pour enregistrer la vidéo. Si aucun numéro de piste n’est indiqué, la valeur par défaut de 1 est utilisée.</td>
</tr>
<tr class="odd">
<td>source vidéo</td>
<td>Retourne le type de source vidéo. Pour plus d’informations, consultez la commande <a href="setvideo.md"><strong>setvideo</strong></a> .</td>
</tr>
<tr class="even">
<td>Numéro de la source vidéo</td>
<td>Retourne un nombre correspondant à la source vidéo du type en cours d’utilisation. Par exemple, elle retourne 2 si la deuxième entrée de la source vidéo NTSC est utilisée.</td>
</tr>
<tr class="odd">
<td>flux vidéo</td>
<td>Retourne le numéro de flux vidéo actuel.</td>
</tr>
<tr class="even">
<td>volume</td>
<td>Retourne le volume moyen du haut-parleur gauche et droit. Cela renvoie une erreur si l’appareil n’a pas été lu ou si le volume n’a pas été défini.</td>
</tr>
<tr class="odd">
<td>handle de fenêtre</td>
<td>Retourne la valeur décimale ASCII du handle de fenêtre dans le mot de poids faible de la valeur de retour.</td>
</tr>
<tr class="even">
<td>fenêtre agrandie</td>
<td>Retourne la <strong>valeur true</strong> si la fenêtre est agrandie.</td>
</tr>
<tr class="odd">
<td>fenêtre réduite</td>
<td>Retourne la <strong>valeur true</strong> si la fenêtre est réduite.</td>
</tr>
<tr class="even">
<td>fenêtre visible</td>
<td>Retourne la <strong>valeur true</strong> si la fenêtre n’est pas masquée.</td>
</tr>
<tr class="odd">
<td>protégé en écriture</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil détecte qu’il ne peut pas enregistrer (autrement dit, si la protection en écriture est activée). S’il peut enregistrer ou s’il ne parvient pas à déterminer s’il peut enregistrer (sans réellement écrire), le pilote retourne la <strong>valeur false</strong>.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne des informations dans le paramètre *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)). Les informations dépendent du type de demande.

## <a name="remarks"></a>Notes

Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .

## <a name="examples"></a>Exemples

La commande suivante retourne le mode actuel de l’appareil « mySound ».

``` syntax
status mysound mode
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[attire](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[réduis](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[load](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Insérer](paste.md)
</dt> <dt>

[enregistrement](record.md)
</dt> <dt>

[reserve](reserve.md)
</dt> <dt>

[enregistrer](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[annuler](undo.md)
</dt> </dl>

 

