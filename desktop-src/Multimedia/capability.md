---
title: fonctionnalité, commande
description: La commande Capability demande des informations sur une capacité particulière d’un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- commande de fonctionnalité Windows multimédia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e57a793f799214753f50504d80bce7051fba14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007220"
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




| Valeur | Type | Type | 
|-------|------|------|
| cdaudio | <ul><li>peut éjecter</li><li>peut jouer</li><li>peut enregistrer</li><li>peut enregistrer</li><li>appareil composé</li></ul> | <ul><li>type de périphérique</li><li>a de l’audio</li><li>a une vidéo</li><li>utilise des fichiers</li></ul> | 
| digitalvideo | <ul><li>peut éjecter</li><li>peut geler</li><li>verrouillage possible</li><li>peut jouer</li><li>peut enregistrer</li><li>peut inverser</li><li>peut enregistrer</li><li>peut étirer</li><li>peut étirer l’entrée</li><li>test possible</li></ul> | <ul><li>appareil composé</li><li>type de périphérique</li><li>a de l’audio</li><li>a toujours</li><li>a une vidéo</li><li>taux de lecture maximal</li><li>Vitesse de lecture minimale</li><li>utilise des fichiers</li><li>utilise des palettes</li><li>windows</li></ul> | 
| superposition | <ul><li>peut éjecter</li><li>peut geler</li><li>peut jouer</li><li>peut enregistrer</li><li>peut enregistrer</li><li>peut étirer</li></ul> | <ul><li>appareil composé</li><li>type de périphérique</li><li>a de l’audio</li><li>a une vidéo</li><li>utilise des fichiers</li><li>windows</li></ul> | 
| sequencer | <ul><li>peut éjecter</li><li>peut jouer</li><li>peut enregistrer</li><li>peut enregistrer</li><li>appareil composé</li></ul> | <ul><li>type de périphérique</li><li>a de l’audio</li><li>a une vidéo</li><li>utilise des fichiers</li></ul> | 
| vidéo | <ul><li>peut détecter une longueur</li><li>peut éjecter</li><li>peut geler</li><li>peut surveiller les sources</li><li>peut jouer</li><li>peut être préroll</li><li>peut afficher un aperçu</li><li>peut enregistrer</li><li>peut inverser</li><li>peut enregistrer</li><li>test possible</li></ul> | <ul><li>taux d’incrément d’horloge</li><li>appareil composé</li><li>type de périphérique</li><li>a de l’audio</li><li>a une horloge</li><li>a un code temporel</li><li>a une vidéo</li><li>nombre de marques</li><li>précision de la recherche</li><li>utilise des fichiers</li></ul> | 
| videodisc | <ul><li>peut éjecter</li><li>peut jouer</li><li>peut enregistrer</li><li>peut inverser</li><li>peut enregistrer</li><li>CAV</li><li>CLV</li><li>appareil composé</li></ul> | <ul><li>type de périphérique</li><li>Vitesse de lecture rapide</li><li>a de l’audio</li><li>a une vidéo</li><li>taux de lecture normal</li><li>taux de lecture lent</li><li>utilise des fichiers</li></ul> | 
| WaveAudio | <ul><li>peut éjecter</li><li>peut jouer</li><li>peut enregistrer</li><li>peut enregistrer</li><li>appareil composé</li><li>type de périphérique</li></ul> | <ul><li>a de l’audio</li><li>a une vidéo</li><li>inputs</li><li>outputs</li><li>utilise des fichiers</li></ul> | 




 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszRequest* et leurs significations :




| Indicateurs | Signification | 
|-------|---------|
| peut détecter une longueur | Retourne la <strong>valeur true</strong> si l’appareil peut détecter la longueur du média. | 
| peut éjecter | Retourne la <strong>valeur true</strong> si l’appareil peut éjecter le média. | 
| peut geler | Retourne la <strong>valeur true</strong> si l’appareil peut geler des données dans la mémoire tampon de trame. | 
| verrouillage possible | Retourne la <strong>valeur true</strong> si l’appareil peut verrouiller les données. | 
| peut surveiller les sources | Retourne la <strong>valeur true</strong> si l’appareil peut passer une entrée (source) à la sortie analysée, indépendamment de la sélection d’entrée actuelle. | 
| peut jouer | Retourne la <strong>valeur true</strong> si l’appareil peut jouer. | 
| peut être préroll | Retourne la <strong>valeur true</strong> si l’appareil prend en charge l’indicateur de préroll avec la commande <a href="cue.md">CUE</a> . | 
| peut afficher un aperçu | Retourne la <strong>valeur true</strong> si l’appareil prend en charge les aperçus. | 
| peut enregistrer | Retourne la <strong>valeur true</strong> si l’appareil prend en charge l’enregistrement. | 
| peut inverser | Retourne la <strong>valeur true</strong> si l’appareil peut jouer en sens inverse. | 
| peut enregistrer | Retourne la <strong>valeur true</strong> si l’appareil peut enregistrer des données. | 
| peut étirer | Retourne la <strong>valeur true</strong> si l’appareil peut étirer des frames pour remplir un rectangle d’affichage donné. | 
| peut étirer l’entrée | Retourne la <strong>valeur true</strong> si l’appareil peut redimensionner une image dans le processus de sa numérisation dans la mémoire tampon de trame. | 
| test possible | Retourne la <strong>valeur true</strong> si l’appareil reconnaît le mot clé test. | 
| cav | Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CAV videodiscs. Il s’agit de la valeur par défaut si aucun videodisc n’est inséré. | 
| taux d’incrément d’horloge | Retourne le nombre de sous-cloisonnements pris en charge par l’horloge externe par seconde. Si l’horloge externe est une horloge en millisecondes, la valeur de retour est 1000. Si la valeur de retour est 0, aucune horloge n’est prise en charge. | 
| clv | Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CLV videodiscs. | 
| appareil composé | Retourne la <strong>valeur true</strong> si l’appareil prend en charge un nom d’élément (fileName). | 
| type de périphérique | Retourne un nom de type d’appareil, qui peut être l’un des éléments suivants :<ul><li>cdaudio</li><li>anciens</li><li>digitalvideo</li><li>other</li><li>superposition</li><li>scanneur</li><li>sequencer</li><li>vidéo</li><li>videodisc</li><li>WaveAudio</li></ul> | 
| Vitesse de lecture rapide | Retourne le taux de lecture rapide en images par seconde, ou zéro si l’appareil ne peut pas être lu rapidement. | 
| a de l’audio | Retourne la <strong>valeur true</strong> si l’appareil prend en charge la lecture audio. | 
| a une horloge | Retourne la <strong>valeur true</strong> si l’appareil a une horloge. | 
| a toujours | Retourne la <strong>valeur true</strong> si l’appareil traite les fichiers avec une seule image plus efficacement que les fichiers vidéo animés. | 
| a un code temporel | Retourne la <strong>valeur true</strong> si l’appareil est en capacité de prendre en charge le code temporel, ou s’il est inconnu. | 
| a une vidéo | Retourne la <strong>valeur true</strong> si l’appareil prend en charge la vidéo. | 
| inputs | Retourne le nombre total de périphériques d’entrée. | 
| taux de lecture maximal | Retourne la vitesse de lecture maximale, en images par seconde, pour l’appareil. | 
| Vitesse de lecture minimale | Retourne la vitesse de lecture minimale, en images par seconde, pour l’appareil. | 
| taux de lecture normal | Retourne la vitesse de lecture normale, en images par seconde, pour l’appareil. | 
| nombre de marques | Retourne le nombre maximal de marques qui peuvent être utilisées ; la valeur zéro indique que les marques ne sont pas prises en charge. | 
| outputs | Retourne le nombre total de périphériques de sortie. | 
| précision de la recherche | Retourne la précision attendue d’une recherche dans les frames ; 0 indique que l’appareil est correct, 1 indique que l’appareil s’attend à se trouver dans une trame de la position de recherche indiquée, et ainsi de suite. | 
| taux de lecture lent | Retourne le taux de lecture lent en images par seconde, ou zéro si l’appareil ne peut pas fonctionner lentement. | 
| utilise des fichiers | Retourne la <strong>valeur true</strong> si le stockage de données utilisé par un périphérique composé est un fichier. | 
| utilise des palettes | Retourne la <strong>valeur true</strong> si l’appareil utilise des palettes. | 
| windows | Retourne le nombre de fenêtres d’affichage simultanées que l’appareil peut prendre en charge. | 




 

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

[signal](cue.md)
</dt> </dl>

 

