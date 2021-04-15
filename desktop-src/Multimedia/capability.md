---
title: fonctionnalité, commande
description: La commande Capability demande des informations sur une capacité particulière d’un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- commande de fonctionnalité multimédia Windows
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464635"
---
# <a name="capability-command"></a>fonctionnalité, commande

La commande Capability demande des informations sur une capacité particulière d’un appareil. Tous les périphériques MCI reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
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

Indicateur qui identifie une fonctionnalité de l’appareil. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de **fonctionnalité** et les indicateurs utilisés par chaque type :



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Type</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>peut éjecter</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut enregistrer</li>
<li>appareil composé</li>
</ul></td>
<td><ul>
<li>type de périphérique</li>
<li>a de l’audio</li>
<li>a une vidéo</li>
<li>utilise des fichiers</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>peut éjecter</li>
<li>peut geler</li>
<li>verrouillage possible</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut inverser</li>
<li>peut enregistrer</li>
<li>peut étirer</li>
<li>peut étirer l’entrée</li>
<li>test possible</li>
</ul></td>
<td><ul>
<li>appareil composé</li>
<li>type de périphérique</li>
<li>a de l’audio</li>
<li>a toujours</li>
<li>a une vidéo</li>
<li>taux de lecture maximal</li>
<li>Vitesse de lecture minimale</li>
<li>utilise des fichiers</li>
<li>utilise des palettes</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>superposition</td>
<td><ul>
<li>peut éjecter</li>
<li>peut geler</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut enregistrer</li>
<li>peut étirer</li>
</ul></td>
<td><ul>
<li>appareil composé</li>
<li>type de périphérique</li>
<li>a de l’audio</li>
<li>a une vidéo</li>
<li>utilise des fichiers</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>peut éjecter</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut enregistrer</li>
<li>appareil composé</li>
</ul></td>
<td><ul>
<li>type de périphérique</li>
<li>a de l’audio</li>
<li>a une vidéo</li>
<li>utilise des fichiers</li>
</ul></td>
</tr>
<tr class="odd">
<td>vidéo</td>
<td><ul>
<li>peut détecter une longueur</li>
<li>peut éjecter</li>
<li>peut geler</li>
<li>peut surveiller les sources</li>
<li>peut jouer</li>
<li>peut être préroll</li>
<li>peut afficher un aperçu</li>
<li>peut enregistrer</li>
<li>peut inverser</li>
<li>peut enregistrer</li>
<li>test possible</li>
</ul></td>
<td><ul>
<li>taux d’incrément d’horloge</li>
<li>appareil composé</li>
<li>type de périphérique</li>
<li>a de l’audio</li>
<li>a une horloge</li>
<li>a un code temporel</li>
<li>a une vidéo</li>
<li>nombre de marques</li>
<li>précision de la recherche</li>
<li>utilise des fichiers</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>peut éjecter</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut inverser</li>
<li>peut enregistrer</li>
<li>CAV</li>
<li>CLV</li>
<li>appareil composé</li>
</ul></td>
<td><ul>
<li>type de périphérique</li>
<li>Vitesse de lecture rapide</li>
<li>a de l’audio</li>
<li>a une vidéo</li>
<li>taux de lecture normal</li>
<li>taux de lecture lent</li>
<li>utilise des fichiers</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li>peut éjecter</li>
<li>peut jouer</li>
<li>peut enregistrer</li>
<li>peut enregistrer</li>
<li>appareil composé</li>
<li>type de périphérique</li>
</ul></td>
<td><ul>
<li>a de l’audio</li>
<li>a une vidéo</li>
<li>inputs</li>
<li>outputs</li>
<li>utilise des fichiers</li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszRequest* et leurs significations :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>peut détecter une longueur</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut détecter la longueur du média.</td>
</tr>
<tr class="even">
<td>peut éjecter</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut éjecter le média.</td>
</tr>
<tr class="odd">
<td>peut geler</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut geler des données dans la mémoire tampon de trame.</td>
</tr>
<tr class="even">
<td>verrouillage possible</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut verrouiller les données.</td>
</tr>
<tr class="odd">
<td>peut surveiller les sources</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut passer une entrée (source) à la sortie analysée, indépendamment de la sélection d’entrée actuelle.</td>
</tr>
<tr class="even">
<td>peut jouer</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut jouer.</td>
</tr>
<tr class="odd">
<td>peut être préroll</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge l' &quot; &quot; indicateur de préroll avec la commande <a href="cue.md">CUE</a> .</td>
</tr>
<tr class="even">
<td>peut afficher un aperçu</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge les aperçus.</td>
</tr>
<tr class="odd">
<td>peut enregistrer</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge l’enregistrement.</td>
</tr>
<tr class="even">
<td>peut inverser</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut jouer en sens inverse.</td>
</tr>
<tr class="odd">
<td>peut enregistrer</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut enregistrer des données.</td>
</tr>
<tr class="even">
<td>peut étirer</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut étirer des frames pour remplir un rectangle d’affichage donné.</td>
</tr>
<tr class="odd">
<td>peut étirer l’entrée</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil peut redimensionner une image dans le processus de sa numérisation dans la mémoire tampon de trame.</td>
</tr>
<tr class="even">
<td>test possible</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil reconnaît le mot clé test.</td>
</tr>
<tr class="odd">
<td>cav</td>
<td>Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CAV videodiscs. Il s’agit de la valeur par défaut si aucun videodisc n’est inséré.</td>
</tr>
<tr class="even">
<td>taux d’incrément d’horloge</td>
<td>Retourne le nombre de sous-cloisonnements pris en charge par l’horloge externe par seconde. Si l’horloge externe est une horloge en millisecondes, la valeur de retour est 1000. Si la valeur de retour est 0, aucune horloge n’est prise en charge.</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CLV videodiscs.</td>
</tr>
<tr class="even">
<td>appareil composé</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge un nom d’élément (fileName).</td>
</tr>
<tr class="odd">
<td>type de périphérique</td>
<td>Retourne un nom de type d’appareil, qui peut être l’un des éléments suivants :
<ul>
<li>cdaudio</li>
<li>anciens</li>
<li>digitalvideo</li>
<li>autre</li>
<li>superposition</li>
<li>scanneur</li>
<li>sequencer</li>
<li>vidéo</li>
<li>videodisc</li>
<li>WaveAudio</li>
</ul></td>
</tr>
<tr class="even">
<td>Vitesse de lecture rapide</td>
<td>Retourne le taux de lecture rapide en images par seconde, ou zéro si l’appareil ne peut pas être lu rapidement.</td>
</tr>
<tr class="odd">
<td>a de l’audio</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge la lecture audio.</td>
</tr>
<tr class="even">
<td>a une horloge</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil a une horloge.</td>
</tr>
<tr class="odd">
<td>a toujours</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil traite les fichiers avec une seule image plus efficacement que les fichiers vidéo animés.</td>
</tr>
<tr class="even">
<td>a un code temporel</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil est en capacité de prendre en charge le code temporel, ou s’il est inconnu.</td>
</tr>
<tr class="odd">
<td>a une vidéo</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil prend en charge la vidéo.</td>
</tr>
<tr class="even">
<td>inputs</td>
<td>Retourne le nombre total de périphériques d’entrée.</td>
</tr>
<tr class="odd">
<td>taux de lecture maximal</td>
<td>Retourne la vitesse de lecture maximale, en images par seconde, pour l’appareil.</td>
</tr>
<tr class="even">
<td>Vitesse de lecture minimale</td>
<td>Retourne la vitesse de lecture minimale, en images par seconde, pour l’appareil.</td>
</tr>
<tr class="odd">
<td>taux de lecture normal</td>
<td>Retourne la vitesse de lecture normale, en images par seconde, pour l’appareil.</td>
</tr>
<tr class="even">
<td>nombre de marques</td>
<td>Retourne le nombre maximal de marques qui peuvent être utilisées ; la valeur zéro indique que les marques ne sont pas prises en charge.</td>
</tr>
<tr class="odd">
<td>outputs</td>
<td>Retourne le nombre total de périphériques de sortie.</td>
</tr>
<tr class="even">
<td>précision de la recherche</td>
<td>Retourne la précision attendue d’une recherche dans les frames ; 0 indique que l’appareil est correct, 1 indique que l’appareil s’attend à se trouver dans une trame de la position de recherche indiquée, et ainsi de suite.</td>
</tr>
<tr class="odd">
<td>taux de lecture lent</td>
<td>Retourne le taux de lecture lent en images par seconde, ou zéro si l’appareil ne peut pas fonctionner lentement.</td>
</tr>
<tr class="even">
<td>utilise des fichiers</td>
<td>Retourne la <strong>valeur true</strong> si le stockage de données utilisé par un périphérique composé est un fichier.</td>
</tr>
<tr class="odd">
<td>utilise des palettes</td>
<td>Retourne la <strong>valeur true</strong> si l’appareil utilise des palettes.</td>
</tr>
<tr class="even">
<td>windows</td>
<td>Retourne le nombre de fenêtres d’affichage simultanées que l’appareil peut prendre en charge.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne des informations dans le paramètre *lpszReturnString* de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Les informations dépendent du type de demande.

## <a name="examples"></a>Exemples

La commande suivante retourne le type de périphérique de l’appareil « mySound ».

``` syntax
capability mysound device type
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

[signal](cue.md)
</dt> </dl>

 

