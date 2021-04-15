---
title: Message WM_APPCOMMAND (winuser. h)
description: Avertit une fenêtre que l’utilisateur a généré un événement de commande d’application, par exemple, en cliquant sur un bouton de commande d’application à l’aide de la souris ou en tapant une touche de commande d’application sur le clavier.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384431"
---
# <a name="wm_appcommand-message"></a>\_Message WM APPCOMMAND

Avertit une fenêtre que l’utilisateur a généré un événement de commande d’application, par exemple, en cliquant sur un bouton de commande d’application à l’aide de la souris ou en tapant une touche de commande d’application sur le clavier.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre dans laquelle l’utilisateur a cliqué sur le bouton ou a appuyé sur la touche. Il peut s’agir d’une fenêtre enfant de la fenêtre recevant le message. Pour plus d’informations sur le traitement de ce message, consultez la section Notes.

</dd> <dt>

*lParam* 
</dt> <dd>

Utilisez le code suivant pour récupérer les informations contenues dans le paramètre *lParam* .


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



La commande d’application est *cmd*, qui peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                  | Signification                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ GRAVES \_ Booster**</dt> <dt>20</dt> </dl>                                                                         | Activez ou désactivez l’option augmentation des basses.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ BASSES \_ baisse**</dt> <dt>19</dt> </dl>                                                                            | Diminuez les basses.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ BASSES \_**</dt> de <dt>21</dt> </dl>                                                                                  | Augmentez la taille des basses.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ NAVIGATEUR \_ précédent**</dt> <dt>1</dt> </dl>                                                        | Naviguer vers l’arrière.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ \_Favoris du navigateur**</dt> <dt>6</dt> </dl>                                                     | Ouvrir les favoris.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ NAVIGATEUR \_ suivant**</dt> <dt>2</dt> </dl>                                                           | Naviguer vers l’avant.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ \_Page d’hébergement du navigateur**</dt> <dt>7</dt> </dl>                                                                    | Accédez à la page d’hébergement.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ \_Actualisation du navigateur**</dt> <dt>3</dt> </dl>                                                           | Actualiser la page.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ \_Recherche de navigateur**</dt> <dt>5</dt> </dl>                                                              | Ouvrez la recherche.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ NAVIGATEUR \_ Stop**</dt> <dt>4</dt> </dl>                                                                    | Arrêter le téléchargement.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ FERMER**</dt> <dt>31</dt> </dl>                                                                                         | Fermez la fenêtre (pas l’application).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPIE**</dt> <dt>36</dt> </dl>                                                                                            | Copiez la sélection.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ \_Liste de CORRECTION**</dt> <dt>45</dt> </dl>                                                          | Affiche la liste de correction lorsqu’un mot est identifié de manière incorrecte lors de l’entrée vocale. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ COUPER**</dt> <dt>37</dt> </dl>                                                                                               | Coupez la sélection.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ \_Commande de dictée ou de \_ \_ contrôle \_ de commande**</dt> <dt>43</dt> </dl> | Bascule entre deux modes d’entrée vocale : dictée et commande/contrôle (en donnant des commandes à une application ou en accédant à des menus). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ Rechercher**</dt> <dt>28</dt> </dl>                                                                                            | Ouvrez la boîte de dialogue **Rechercher** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ TRANSFÉRER le \_ courrier**</dt> <dt>40</dt> </dl>                                                                   | Transférer un message électronique.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ AIDE**</dt> <dt>27</dt> </dl>                                                                                            | Ouvre la boîte de dialogue **d’aide** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ LANCER \_ App1**</dt> <dt>17</dt> </dl>                                                                      | Démarrez App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ LANCER \_ App2**</dt> <dt>18</dt> </dl>                                                                      | Démarrez App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ LANCER la \_ messagerie**</dt> <dt>15</dt> </dl>                                                                      | Ouvrir le courrier.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ DÉMARRER le \_ support \_ Sélectionner**</dt> <dt>16</dt> </dl>                                             | Accédez au mode de sélection du média.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ Canal de média \_ \_ vers le dessous**</dt> de <dt>52</dt> </dl>                                                | Décrémenter la valeur du canal, par exemple pour un téléviseur ou un tuner radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ \_Chaîne multimédia \_ up**</dt> <dt>51</dt> </dl>                                                      | Incrémentez la valeur du canal, par exemple pour un téléviseur ou un tuner radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Transfert rapide des médias**</dt> <dt>49</dt> </dl>                                                | Augmentez la vitesse de lecture du flux. Cela peut être implémenté de nombreuses façons, par exemple, à l’aide d’une vitesse fixe ou d’un basculement à travers une série de vitesses accrues. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ MÉDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | Aller à la piste suivante.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ Mise en \_ pause du support**</dt> <dt>47</dt> </dl>                                                                      | Suspendre. S’il est déjà suspendu, n’effectuez aucune action supplémentaire. Il s’agit d’une commande de PAUSE directe qui n’a aucun État. S’il existe des boutons de lecture et d’interruption discrets, les applications doivent agir sur cette commande, ainsi que sur **APPCOMMAND \_ Media \_ Play \_ Pause**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Début de la diffusion à la position actuelle. S’il est déjà suspendu, il reprend. Il s’agit d’une commande de lecture directe qui n’a aucun État. S’il existe des boutons de **lecture** et d' **interruption** discrets, les applications doivent agir sur cette commande, ainsi que sur **APPCOMMAND \_ Media \_ Play \_ Pause**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ Play \_ Pause**</dt> <dt>14</dt> </dl>                                                      | Lire ou suspendre la lecture. S’il existe des boutons de **lecture** et d' **interruption** discrets, les applications doivent agir sur cette commande, ainsi que sur **APPCOMMAND \_ Media \_ Play** et **APPCOMMAND \_ Media \_ Pause**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ \_PREVIOUSTRACK multimédia**</dt> <dt>12</dt> </dl>                                              | Aller à la piste précédente.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ \_Enregistrement multimédia**</dt> <dt>48</dt> </dl>                                                                   | Commence l’enregistrement du flux actuel.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ \_Rembobinage de média**</dt> <dt>50</dt> </dl>                                                                   | Revenir en arrière dans un flux à un taux de vitesse plus élevé. Cela peut être implémenté de nombreuses façons, par exemple, à l’aide d’une vitesse fixe ou d’un basculement à travers une série de vitesses accrues. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ Stop**</dt> <dt>13</dt> </dl>                                                                         | Arrêter la lecture.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ MIC \_ \_ désactivé \_ /bascule**</dt> <dt>44</dt> </dl>                                                  | Activez/désactivez le microphone.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME du MICROPHONE en \_ \_ baisse**</dt> <dt>25</dt> </dl>                                    | Réduire le volume du microphone.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ VOLUME du MICROPHONE \_ \_ muet**</dt> <dt>24</dt> </dl>                                    | Rendre le microphone muet.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ \_Volume de \_ microphone**</dt> <dt>26</dt> </dl>                                          | Augmentez le volume du microphone.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NOUVEAU**</dt> <dt>29</dt> </dl>                                                                                               | Créez une nouvelle fenêtre.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ Ouvrez**</dt> <dt>30</dt> </dl>                                                                                            | Ouvrez une fenêtre.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ COLLER**</dt> <dt>38</dt> </dl>                                                                                         | Coller<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ IMPRIMER**</dt> <dt>33</dt> </dl>                                                                                         | Imprime le document actif.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ RÉTABLIR**</dt> <dt>35</dt> </dl>                                                                                            | Rétablir la dernière action.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ RÉPONDRE \_ au \_ courrier**</dt> <dt>39</dt> </dl>                                                               | Répondre à un message électronique.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ ENREGISTRER**</dt> <dt>32</dt> </dl>                                                                                            | Enregistrer le document actif.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ Envoyer un \_ message**</dt> <dt>41</dt> </dl>                                                                            | Envoyer un message électronique.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ \_Vérification orthographique**</dt> <dt>42</dt> </dl>                                                                      | Lancez une vérification orthographique.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ AIGUs \_ vers le PG**</dt> . <dt>22</dt> </dl>                                                                      | Réduisez les aigus.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ AIGUs \_ vers le haut**</dt> <dt>23</dt> </dl>                                                                            | Augmentez les aigus.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ ANNULER**</dt> <dt>34</dt> </dl>                                                                                            | Annuler la dernière action.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ \_Baisser le volume**</dt> <dt>9</dt> </dl>                                                                       | Diminuez le volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ muet**</dt> <dt>8</dt> </dl>                                                                       | Désactiver le volume.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_**</dt> <dt>10</dt> </dl>                                                                            | Augmentez le volume.<br/>                                                                                                                                                                                                                                                               |



 

Le composant *uDevice* indique le périphérique d’entrée qui a généré l’événement d’entrée, et peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                 | Signification                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ CLÉ**</dt> <dt>0</dt> </dl>            | L’utilisateur a appuyé sur une touche.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ SOURIS**</dt> <dt>0x8000</dt> </dl> | L’utilisateur a cliqué sur un bouton de la souris.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_ OEM**</dt> <dt>0x1000</dt> </dl>       | Une source matérielle non identifiée a généré l’événement. Il peut s’agir d’un événement de souris ou de clavier.<br/> |



 

Le composant *dwKeys* indique si différentes clés virtuelles sont arrêtées et peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                               | Signification                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle </dl>    | La touche CTRL est enfoncée.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Le bouton gauche de la souris est enfoncé.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Le bouton central de la souris est enfoncé.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Le bouton droit de la souris est enfoncé.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | La touche Maj est enfoncée.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt> </dl> | Le premier bouton X est enfoncé.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Le deuxième bouton X est enfoncé.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**. Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.

## <a name="remarks"></a>Notes

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère le message **WM \_ APPCOMMAND** lors du traitement du [**message \_ WM XBUTTONUP**](wm-xbuttonup.md) ou [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md) , ou lorsque l’utilisateur tape une clé de commande d’application.

Si une fenêtre enfant ne traite pas ce message et appelle à la place [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), **DefWindowProc** envoie le message à sa fenêtre parente. Si une fenêtre de niveau supérieur ne traite pas ce message et appelle à la place **DefWindowProc**, **DefWindowProc** appellera un hook de Shell avec le code de hook égal à **HSHELL \_ APPCOMMAND**.

Pour obtenir les coordonnées du curseur si le message a été généré par un clic de souris, l’application peut appeler [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Une application peut tester si le message a été généré par la souris en vérifiant si *lParam* contient **FAPPCOMMAND \_ Mouse**.

Contrairement à d’autres messages Windows, une application doit retourner la **valeur true** à partir de ce message si elle le traite. Cela permettra aux logiciels qui simulent ce message sur les systèmes Windows antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Obtient \_ APPCOMMAND \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**Obtient l' \_ appareil \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**Obtient le \_ KeyState \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**\_XBUTTONUP WM**](wm-xbuttonup.md)
</dt> <dt>

[**\_NCXBUTTONUP WM**](wm-ncxbuttonup.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> </dl>

 

