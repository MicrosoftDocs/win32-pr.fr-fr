---
title: commande Set
description: La commande Set établit les paramètres de contrôle de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- définir la commande Windows multimédia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75f407a1e360cfbd6407f7ada29192addece7f7a968a2437326dc091fe0d9522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371011"
---
# <a name="set-command"></a>commande Set

> [!NOTE]
> Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.  Dans ce document, il existe des références au mot « esclave ». Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.  Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes. Pour des fins de cohérence, ce document contient ce mot. Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.


La commande Set établit les paramètres de contrôle de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Indicateur pour l’établissement des paramètres de contrôle. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Set** et les indicateurs utilisés par chaque type.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type d’appareil</th>
<th>Indicateurs de commande</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>format d’heure en millisecondes</li>
<li>format d’heure MSF</li>
<li>format d’heure TMSF</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li><em>format</em> de format de fichier</li>
<li>recherche exacte</li>
<li>recherche exacte</li>
<li><em>facteur</em> de vitesse</li>
<li><em>format</em> de format de fichier toujours</li>
<li>frames de format d’heure</li>
<li>format d’heure en millisecondes</li>
<li>vidéo désactivée</li>
<li>vidéo sur</li>
</ul></td>
</tr>
<tr class="odd">
<td>superposition</td>
<td><ul>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>vidéo désactivée</li>
<li>vidéo sur</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>MIDI maître</li>
<li>maître aucun</li>
<li>SMPTE maître</li>
<li><em>heure</em> du décalage</li>
<li>mappeur de port</li>
<li>port aucun</li>
<li><em>port_number</em> de port</li>
<li>fichier esclave</li>
<li>MIDI esclave</li>
<li>esclave aucun</li>
<li>SMPTE esclave</li>
<li>tempo <em>tempo_value</em></li>
<li>format d’heure en millisecondes</li>
<li>format d’heure SMPTE <em>fps</em></li>
<li>suppression du format d’heure SMPTE 30</li>
<li>pointeur de chanson au format d’heure</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>vidéo</strong></td>
<td><ul>
<li>enregistrement d’assemblage activé</li>
<li>réassembler l’enregistrement désactivé</li>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li><em>heure</em> de l’horloge</li>
<li>format du compteur</li>
<li><em>valeur</em> de compteur</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>compteur d’index</li>
<li>Date d’index</li>
<li>heure de l’index</li>
<li>heure de l’index</li>
<li><em>durée</em> de CodeLength</li>
<li><em>délai d’attente</em> de pause</li>
<li>durée de Postroll-</li>
<li><em>duration</em></li>
<li>Sous tension</li>
<li>mettre hors tension</li>
<li><em>durée</em> du préroll</li>
<li>format d’enregistrement SP</li>
<li>format d’enregistrement LP</li>
<li>format d’enregistrement EP</li>
<li><em>facteur</em> de vitesse</li>
<li>frames de format d’heure</li>
<li>format d’heure HMS</li>
<li>format d’heure en millisecondes</li>
<li>format d’heure MSF</li>
<li>format d’heure SMPTE <em>fps</em></li>
<li>suppression du format d’heure SMPTE 30</li>
<li>format d’heure TMSF</li>
<li>compteur du mode temps</li>
<li>détection du mode de temps</li>
<li>code temporel du mode Time</li>
<li>suivi plus</li>
<li>suivi moins</li>
<li>réinitialisation du suivi</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>frames de format d’heure</li>
<li>format d’heure HMS</li>
<li>format d’heure en millisecondes</li>
<li>suivi du format d’heure</li>
<li>vidéo désactivée</li>
<li>vidéo sur</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li><em>entier</em> d’alignement</li>
<li>toute entrée</li>
<li>toute sortie</li>
<li>tout audio désactivé</li>
<li>tout son sur</li>
<li>audio quitté</li>
<li>audio restant activé</li>
<li>audio immédiatement éteint</li>
<li>contenu audio</li>
<li>BitsPerSample <em>BIT_COUNT</em></li>
<li>bytespersec <em>byte_rate</em></li>
<li>canaux <em>channel_count</em></li>
<li>porte fermée</li>
<li>porte ouverte</li>
<li>format de balise PCM</li>
<li><em>balise</em> de format tag</li>
<li><em>entier</em> d’entrée</li>
<li><em>entier</em> de sortie</li>
<li><em>entier</em> SamplesPerSec</li>
<li>octets de format d’heure</li>
<li>format d’heure en millisecondes</li>
<li>exemples de format d’heure</li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszSetting** et leurs significations.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>entier</em> d’alignement</td>
<td>Définit l’alignement des blocs de données par rapport au début des données transmises au périphérique Wave-audio. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="even">
<td>toute entrée</td>
<td>Utilise toute entrée qui prend en charge le format actuel lors de l’enregistrement. Il s'agit du paramètre par défaut.</td>
</tr>
<tr class="odd">
<td>toute sortie</td>
<td>Utilise une sortie qui prend en charge le format actuel lors de la diffusion. Il s’agit de la valeur par défaut.</td>
</tr>
<tr class="even">
<td>enregistrement d’assemblage activé <br/> réassembler l’enregistrement désactivé <br/></td>
<td>En mode assembler, toutes les pistes sont enregistrées comme défini par l’appareil. La plupart des magnétoscopes sont en mode assemblage par défaut.</td>
</tr>
<tr class="odd">
<td>tout audio désactivé <br/> tout son sur <br/></td>
<td>Désactive ou active la sortie audio. Les périphériques de superposition vidéo, MCISEQ Sequencer et MCIWAVE périphérique audio-audio ne prennent pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td>audio quitté <br/> audio restant activé <br/> audio immédiatement éteint <br/> contenu audio <br/></td>
<td>Désactive ou active la sortie vers le canal audio gauche ou droit. Les périphériques de superposition vidéo, MCISEQ Sequencer et MCIWAVE périphérique audio-audio ne prennent pas en charge cet indicateur.</td>
</tr>
<tr class="odd">
<td>BitsPerSample <em>BIT_COUNT</em></td>
<td>Définit le nombre de bits par échantillon PCM (Pulse Code Modulation) lu ou enregistré. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="even">
<td>bytespersec <em>byte_rate</em></td>
<td>Définit le nombre moyen d’octets par seconde lus ou enregistrés. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="odd">
<td>canaux <em>channel_count</em></td>
<td>Définit les canaux pour la diffusion et l’enregistrement. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="even">
<td><em>heure</em> de l’horloge</td>
<td>Définit l’heure de l’horloge externe <em>.</em> Le format est spécifié en tant qu’entier long non signé.</td>
</tr>
<tr class="odd">
<td>format du compteur</td>
<td>Définissez le format d’heure du compteur, tel qu’il est retourné par le compteur d' <a href="status.md">État</a> &quot; &quot; . Pour plus d’informations sur les types applicables, consultez la commande <strong>Set</strong> &quot; Time format &quot; .</td>
</tr>
<tr class="even">
<td><em>valeur</em> de compteur</td>
<td>Définit le compteur VCR à la valeur spécifiée. La valeur doit être spécifiée dans le format de compteur actuel. Pour plus d’informations, consultez la commande <strong>Set</strong> &quot; Counter format &quot; .</td>
</tr>
<tr class="odd">
<td>porte fermée</td>
<td>Retire la barre d’État et ferme la porte, si possible. Pour les magnétoscopes, charge automatiquement la bande.</td>
</tr>
<tr class="even">
<td>porte ouverte</td>
<td>Ouvre la porte et éjecte le plateau ou la bande, si possible.</td>
</tr>
<tr class="odd">
<td><em>format</em> de format de fichier</td>
<td>Spécifie un format de fichier utilisé pour les commandes d' <a href="save.md">enregistrement</a> ou de <a href="capture.md">capture</a> . En cas d’omission, il peut s’agit d’un format défini par défaut pour le pilote de périphérique. Si le format de fichier spécifié est en conflit avec l’algorithme et la qualité actuellement sélectionnés, ils sont remplacés par les valeurs par défaut pour le format de fichier. Les formats de fichier suivants sont définis :
<ul>
<li>AVI : spécifie le format AVI.</li>
<li>avss : spécifie le format AVSS.</li>
<li>DIB : spécifie le format DIB.</li>
<li>JFIF : spécifie le format JFIF.</li>
<li>JPEG : spécifie le format JPEG.</li>
<li>MPEG : spécifie le format MPEG.</li>
<li>RDIB : spécifie le format DIB RLE.</li>
<li>rjpeg : spécifie le format RJPEG.</li>
</ul></td>
</tr>
<tr class="even">
<td>format de balise PCM</td>
<td>Définit le type de format PCM pour la diffusion et l’enregistrement. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="odd">
<td><em>balise</em> de format tag</td>
<td>Définit le type de format pour la diffusion et l’enregistrement. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="even">
<td>code temporel de l’index <br/> compteur d’index <br/> Date d’index <br/> heure de l’index <br/></td>
<td>Définit l’écran d’affichage actuel sur le magnétoscope.</td>
</tr>
<tr class="odd">
<td><em>entier</em> d’entrée</td>
<td>Définit le canal audio utilisé comme entrée.</td>
</tr>
<tr class="even">
<td><em>durée</em> de la durée</td>
<td>Définit la longueur spécifiée par l’utilisateur de la bande dans le magnétoscope. Cette longueur est retournée par la commande de longueur d' <a href="status.md">État</a> &quot; &quot; et est fournie à des fins de compatibilité avec les applications qui nécessitent cette commande pour retourner une longueur valide.</td>
</tr>
<tr class="odd">
<td>midi maître</td>
<td>Définit le séquenceur MIDI comme source de synchronisation. Les données de synchronisation sont envoyées au format MIDI. MCISEQ Sequencer ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td>maître aucun</td>
<td>Empêche le séquenceur MIDI d’envoyer des données de synchronisation. MCISEQ Sequencer ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="odd">
<td>SMPTE maître</td>
<td>Définit le séquenceur MIDI comme source de synchronisation. Les données de synchronisation sont envoyées au format SMPTE (société de motion image and Television Engineers). MCISEQ Sequencer ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td><em>heure</em> du décalage</td>
<td>Définit le <em>temps</em>de décalage SMPTE. Le décalage est l’heure de début d’une séquence basée sur SMPTE. L' <em>heure</em> est exprimée sous la forme <em>hh</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, où <em>hh</em> est hours, <em>mm</em> correspond à minutes, <em>SS</em> à secondes et <em>FF</em> à la trame.</td>
</tr>
<tr class="odd">
<td><em>entier</em> de sortie</td>
<td>Définit le canal audio utilisé comme sortie.</td>
</tr>
<tr class="even">
<td><em>délai d’attente</em> de pause</td>
<td>Définit la durée maximale, en millisecondes, d’une commande de <a href="pause.md">Pause</a> . Une valeur de <em>délai d’attente</em> de zéro indique qu’aucun délai d’attente n’A lieu.</td>
</tr>
<tr class="odd">
<td><em>durée</em> de la durée de Postroll</td>
<td>Définit la longueur, dans le format d’heure actuel, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande d' <a href="stop.md">arrêt</a> ou de <strong>Pause</strong> .</td>
</tr>
<tr class="even">
<td>mappeur de port</td>
<td>Définit le Mappeur MIDI comme port recevant les messages MIDI. Cette commande échoue si le Mappeur MIDI ou un port dont il a besoin est utilisé par une autre application.</td>
</tr>
<tr class="odd">
<td>port aucun</td>
<td>Désactive l’envoi des messages MIDI. Cette commande ferme également un port MIDI.</td>
</tr>
<tr class="even">
<td><em>port_number</em> de port</td>
<td>Définit le port MIDI recevant les messages MIDI. Cette commande échoue si le port que vous essayez d’ouvrir est utilisé par une autre application.</td>
</tr>
<tr class="odd">
<td>Sous tension <br/> mettre hors tension <br/></td>
<td>Active ou désactive la mise sous tension de l’appareil.</td>
</tr>
<tr class="even">
<td><em>durée</em> du préroll</td>
<td>Définit la longueur, dans le format d’heure actuel, nécessaire pour stabiliser la sortie du magnétoscope.</td>
</tr>
<tr class="odd">
<td>format d’enregistrement SP <br/> format d’enregistrement LP <br/> format d’enregistrement EP <br/></td>
<td>Définit le mode d’enregistrement du magnétoscope sur SP pour la lecture standard, EP pour extension de lecture ou LP pour une lecture longue. Ces valeurs ne sont pas destinées à être spécifiques à la SHV. Elles sont mappées à trois modes appropriés avec d’autres formats de bande. Par exemple, SP est mappé à l’enregistrement le plus rapide et de qualité la plus élevée.</td>
</tr>
<tr class="even">
<td><em>entier</em> SamplesPerSec</td>
<td>Définit le taux d’échantillonnage pour la diffusion et l’enregistrement. Le fichier est enregistré dans ce format.</td>
</tr>
<tr class="odd">
<td>recherche exacte<br/> recherche exacte <br/></td>
<td>Sélectionne l’un des deux modes de recherche. Lorsque &quot; Seek est activé &quot; , Seek passe toujours à la trame spécifiée. Lorsque &quot; Seek &quot; est défini sur OFF, Seek se déplace vers l’image clé la plus proche avant le frame spécifié.</td>
</tr>
<tr class="even">
<td>fichier esclave</td>
<td>Définit le séquenceur MIDI pour utiliser les données de fichier en tant que source de synchronisation. Il s'agit du paramètre par défaut.</td>
</tr>
<tr class="odd">
<td>midi esclave</td>
<td>Définit le séquenceur MIDI pour qu’il utilise les données MIDI entrantes pour la source de synchronisation. Sequencer reconnaît les données de synchronisation avec le format MIDI. MCISEQ Sequencer ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td>esclave aucun</td>
<td>Définit le séquenceur MIDI pour ignorer la synchronisation</td>
</tr>
<tr class="odd">
<td>SMPTE esclave</td>
<td>Définit le séquenceur MIDI pour qu’il utilise les données MIDI entrantes pour la source de synchronisation. Sequencer reconnaît les données de synchronisation avec le format SMPTE. MCISEQ Sequencer ne prend pas en charge cet indicateur.</td>
</tr>
<tr class="even">
<td>facteur de vitesse</td>
<td>Définit la vitesse relative de lecture vidéo et audio à partir de l’espace de travail. Factor est le rapport entre la fréquence d’images nominale et la fréquence d’images souhaitée, où la fréquence d’images nominale est désignée comme 1000. (Un taux de 500 est une vitesse semi-normale, 2000 une vitesse normale, et ainsi de suite.) Si vous définissez la vitesse sur zéro, la vidéo est lue le plus rapidement possible sans supprimer les images ni les données audio.</td>
</tr>
<tr class="odd">
<td><em>format</em> de format de fichier toujours</td>
<td>Spécifie le format de fichier utilisé pour les commandes de capture.</td>
</tr>
<tr class="even">
<td>tempo tempo_value</td>
<td>Définit le tempo de la séquence en fonction du format d’heure actuel. Dans le cas d’un fichier basé sur PPQN, le tempo_value est interprété comme un temps par minute. Dans le cas d’un fichier basé sur la SMPTE, le tempo_value est interprété comme un nombre d’images par seconde.</td>
</tr>
<tr class="odd">
<td>octets de format d’heure</td>
<td>Dans un format de fichier PCM, définit le format d’heure sur octets. Toutes les informations de position sont spécifiées sous la forme d’octets après cette commande.</td>
</tr>
<tr class="even">
<td>frames de format d’heure</td>
<td>Définit le format d’heure sur les frames. Toutes les commandes qui utilisent des valeurs de position supposent des frames. Lorsque l’appareil est ouvert, frames est le mode par défaut. Pris en charge par videodiscs à l’aide du format CAV.</td>
</tr>
<tr class="odd">
<td>format d’heure HMS</td>
<td>Définit le format d’heure sur les heures, les minutes et les secondes. Toutes les commandes qui utilisent des valeurs de position supposent HMS. HMS est le format par défaut pour CLV videodiscs. Spécifiez une valeur HMS hh : mm : SS, où HH correspond à heures, mm à minutes et SS à secondes. Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls. Par exemple, 3, 3:0 et 3:0:0 sont tous des moyens valides pour exprimer 3 heures. <br/></td>
</tr>
<tr class="even">
<td>format d’heure en millisecondes</td>
<td>Définit le format d’heure sur millisecondes. Toutes les commandes qui utilisent des valeurs de position prennent la valeur en millisecondes. Vous pouvez abréger les millisecondes comme &quot; MS &quot; . Pour les appareils Sequencer, le fichier de séquence définit le format par défaut sur PPQN ou SMPTE. Les périphériques de superposition vidéo ne prennent pas en charge cet indicateur.<br/></td>
</tr>
<tr class="odd">
<td>format d’heure MSF</td>
<td>Définit le format d’heure sur les minutes, les secondes et les frames. Toutes les commandes qui utilisent des valeurs de position supposent MSF (le format par défaut pour les CD audio). Spécifiez une valeur MSF au format mm : SS : FF, où mm correspond à minutes, SS à secondes et FF à frames. Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls. Par exemple, 3, 3:0 et 3:0:0 sont des méthodes valides pour exprimer 3 minutes.<br/> Les champs MSF ont les valeurs maximales suivantes :<br/>
<ul>
<li>Minutes 99</li>
<li>Secondes 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="even">
<td>exemples de format d’heure</td>
<td>Définit le format d’heure sur Samples. Toutes les informations de position sont spécifiées en tant qu’exemples après cette commande.</td>
</tr>
<tr class="odd">
<td>format d’heure SMPTE 24<br/> format d’heure SMPTE 25<br/> format d’heure SMPTE 30<br/></td>
<td>Définit le format d’heure sur une fréquence d’images SMPTE. Pour les magnétoscopes, définit le format d’heure hh : mm : SS : FF, où les valeurs autorisées sont comprises entre 00:00:00:00 et 23:59:59 : XX, tandis que la valeur XX est inférieure aux images par seconde, comme spécifié par le nombre 24, 25 ou 30 comme spécifié dans l’indicateur. En entrée, deux-points ( :) sont requis pour séparer les composants. Les unités les moins significatives peuvent être omises si elles sont égales à 00 ; par exemple, 02:00 est le même que 02:00:00:00. Toutes les commandes qui utilisent des valeurs de position prennent le format SMPTE.<br/> Le fichier de séquence définit le format par défaut sur PPQN ou SMPTE.<br/></td>
</tr>
<tr class="even">
<td>suppression du format d’heure SMPTE 30</td>
<td>Définit le format d’heure sur la fréquence d’images de dépôt SMPTE 30. Pour les magnétoscopes, identique à SMPTE 30, sauf que certaines positions du code temporel sont supprimées du format de façon à ce que les positions du code temporel enregistrées pour chaque image (à la fréquence d’images NTSC de 29,97 fps) correspondent au temps réel (à 30 i/s). Les positions de code temporel supprimées sont les suivantes : deux fois par minute, pour les neuf premières minutes de contenu enregistré. Par exemple, à 01:04:59:29, la position suivante du code temporel est 01:05:00:02, et non 01:05:00:00. Toutes les commandes qui utilisent des valeurs de position prennent le format SMPTE.<br/> Le fichier de séquence définit le format par défaut sur PPQN ou SMPTE.<br/></td>
</tr>
<tr class="odd">
<td>pointeur de chanson au format d’heure</td>
<td>Définit le format d’heure sur le pointeur de la chanson (seizième Remarques). Toutes les commandes qui utilisent des valeurs de position supposent l’utilisation d’unités de pointeur de chanson. Cet indicateur n’est valide que pour une séquence de type de division PPQN.</td>
</tr>
<tr class="even">
<td>format d’heure TMSF</td>
<td>Définit le format d’heure sur les suivis, les minutes, les secondes et les frames. Toutes les commandes qui utilisent des valeurs de position supposent TMSF. Spécifiez une valeur TMSF comme TT : mm : SS : FF, où TT est Tracks, mm est minutes, SS est secondes et FF est le frame. Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls. Par exemple, 3, 3:0, 3:0:0 et 3:0:0:0 sont tous des moyens valides pour exprimer Track 3. <br/> Les valeurs maximales des champs TMSF sont les suivantes :<br/>
<ul>
<li>Suit 99</li>
<li>Minutes 90</li>
<li>Secondes 59</li>
<li>Frames 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>suivi du format d’heure</td>
<td>Définit le format de position des pistes. Toutes les commandes qui utilisent des valeurs de position supposent des pistes.</td>
</tr>
<tr class="even">
<td>compteur du mode temps</td>
<td>Définit le mode de positionnement-informations pour utiliser les compteurs VCR.</td>
</tr>
<tr class="odd">
<td>détection du mode de temps</td>
<td>Définit le mode d’informations de position en fonction de la détection des informations de code temporel sur la bande. Si des informations de code temporel sont détectées, le type d’heure est défini sur &quot; timecode &quot; ; sinon, le type d’heure est défini sur &quot; Counter &quot; . &quot;&quot;La détection est un mode spécial. Chaque fois que le pilote est ouvert, une nouvelle bande est insérée, ou la &quot; commande de mode &quot; de temps est émise, le pilote vérifie le mode d’heure actuel disponible sur la bande et définit le &quot; type &quot; de temps sur &quot; code temporel &quot; ou &quot; compteur &quot; . Une fois le &quot; type &quot; de temps défini, le pilote ne le modifie pas tant que l’une des conditions ci-dessus n’a pas été reproduite.<br/></td>
</tr>
<tr class="even">
<td>code temporel du mode Time</td>
<td>Définit le mode d’informations de position pour utiliser &quot; &quot; les informations de code temporel sur la bande.</td>
</tr>
<tr class="odd">
<td>suivi plus <br/> suivi moins <br/> réinitialisation du suivi <br/></td>
<td>Ajuste la vitesse du transport des cassettes vidéo en incréments précis. Utilisez les &quot; indicateurs de suivi &quot; lorsqu’une image bruyante est obtenue à partir d’un magnétoscope. &quot;Le suivi plus &quot; augmente la vitesse de transport. &quot;Le suivi moins &quot; diminue la vitesse de transport. &quot;Le suivi &quot; de la réinitialisation retourne l’ajustement de suivi à zéro.</td>
</tr>
<tr class="even">
<td>vidéo désactivée</td>
<td>Désactive la sortie vidéo.</td>
</tr>
<tr class="odd">
<td>vidéo sur</td>
<td>Active la sortie vidéo.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Plusieurs propriétés des données Waveform-Audio sont définies lors de la création du fichier de stockage des données. Ces propriétés décrivent comment les données sont structurées dans le fichier et ne peuvent pas être modifiées une fois l’enregistrement commencé. La liste suivante identifie ces propriétés :

-   alignement
-   bitspersample
-   bytespersec
-   channels
-   balise de format
-   samplespersec

## <a name="examples"></a>Exemples

La commande suivante définit le format d’heure sur millisecondes et définit le format Waveform-Audio sur 8 bits, mono, 11 kHz.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Configuration requise



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

[attire](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[enregistrer](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

