---
description: votre application intègre une conception et une utilisation optimales du stylet de tablette en envoyant à la fois des messages de souris Microsoft Windows et des événements système.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Événements système et messages de la souris
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235068"
---
# <a name="system-events-and-mouse-messages"></a>Événements système et messages de la souris

votre application intègre une conception et une utilisation optimales du stylet de tablette en envoyant à la fois des messages de souris Microsoft Windows et des événements système. Les applications reçoivent les deux ensembles d’événements pour chaque mouvement ou action du stylet. L’application choisit ensuite l’événement approprié à utiliser en fonction du contexte de l’action. Windows les messages de la souris fonctionnent bien pour le pointage et la sélection des activités. vous devez les utiliser pour les activités qui impliquent une interaction avec les éléments de l’interface utilisateur. Les événements PEN fonctionnent bien pour les applications manuscrites en temps réel, les actions du stylet et l’écriture manuscrite.

> [!Note]  
> Les événements de stylet et les messages de la souris sont envoyés à une application, que le stylet ou la souris soit utilisé ou non.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Distinction entre l’entrée du stylet et la souris

Lorsque votre application reçoit un message de souris (tel que WM \_ LBUTTONDOWN), elle peut appeler la fonction [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) pour évaluer si le message provient d’un stylet ou d’un périphérique de souris.

La valeur retournée par [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) doit être masquée par rapport à 0xFFFFFF00, puis comparée à 0xFF515700. Les définitions suivantes peuvent rendre ce plus clair :


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Si la comparaison est vraie, ce message de souris a été généré par un écran tactile ou un stylet de tablette Tablet PC. Dans tous les autres cas, vous pouvez supposer que ce message a été généré par un périphérique de souris.

Les 8 bits de poids faible retournés à partir de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) sont des variables. Parmi ces bits, 7 (le plus petit 7, masqué par 0x7F) sont utilisés pour représenter l’ID de curseur, zéro pour la souris ou une valeur de variable pour l’ID de stylet. en outre, dans Windows Vista, le huitième bit, masqué par 0x80, est utilisé pour différencier les entrées tactiles de l’entrée de stylet (0 = pen, 1 = touch).

## <a name="supported-system-gestures"></a>Gestes système pris en charge

le tableau suivant répertorie les gestes système actuellement inclus dans Windows XP édition Tablet PC, détaille les actions de stylet et les événements système correspondants, et montre comment ils se rapportent aux actions de la souris traditionnelles.



| Mouvement du stylet                                  | Action de la souris                                                    | Description du mouvement du stylet                                                                                                                                                                                                             | Messages d’événement                                                                                                                       | Messages de la souris                                                                                                                        | comportements dans les applications basées sur Windows                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taper<br/>                               | Clic gauche<br/>                                           | Appuyez une fois sur l’écran avec le stylet.<br/>                                                                                                                                                                                        | ISG \_ Appuyez sur envoyé lorsque le stylet est levé.<br/>                                                                                         | WM \_ LBUTTONDOWN et WM \_ LBUTTONUP envoyés lorsque le stylet est levé.<br/>                                                                    | Choisir une commande à partir d’un menu ou d’une barre d’outils, agir si la commande est sélectionnée, définir le point d’insertion (IP), afficher les commentaires de sélection.<br/>                                                |
| Double appui<br/>                        | Double-clic<br/>                                         | Appuyez deux fois sur l’écran en succession rapide.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP envoyé le second TAP (vers le point). \_Événement TAP ISG envoyé sur le premier TAP.<br/>                                           | WM \_ LBUTTONDBLCLK envoyé au second appui (vers le-dessus). WM \_ LBUTTONDOWN et WM \_ LBUTTONUP envoyés au premier appui (haut) comme pour un seul TAP.<br/> | Sélectionnez Word, ouvrir un fichier ou un dossier.<br/>                                                                                                                                     |
| Appuyer de manière prolongée<br/>                    | Cliquer avec le bouton droit<br/>                                          | Appuyez sur l’écran et maintenez la touche enfoncée jusqu’à ce qu’une icône de souris apparaisse, puis soulevez le stylet pour afficher un menu contextuel. Une application peut choisir d’effectuer une action différente de l’illustration d’un menu contextuel lorsque le stylet est levé.<br/> | ISG \_ HOLDENTER envoyé lorsque le stylet est trop long. ISG \_ RIGHTTAP envoyé lorsque Pen est levé et que le clic droit se produit.<br/> | \_Les RBUTTONDOWN WM et WM \_ RBUTTONUP envoyés lorsque le clic droit se produit (lorsque le stylet est levé).<br/>                                       | Afficher le menu contextuel.<br/>                                                                                                                                                   |
| Blocage<br/>                      | Clic gauche<br/>                                           | Appuyez sur l’écran et maintenez le bouton enfoncé jusqu’à ce que l’icône de la souris s’affiche et disparaît. Les utilisateurs sont susceptibles de le faire lorsqu’ils envisagent d’appuyer et de maintenir une pression et veulent revenir au TAP.<br/>                                                 | ISG \_ Appuyez sur envoyé lorsque le stylet est levé.<br/>                                                                                         | WM \_ LBUTTONDOWN et WM \_ LBUTTONUP envoyés lorsque Pen est levé.<br/>                                                                 | Cliquez longuement sur pendant un certain temps. Il n’existe aucun équivalent de souris. Il s’agit d’une solution de secours pour les cas où un utilisateur s’exécute pendant un long moment. L’événement revient à un TAP.<br/> |
| Glissement<br/>                              | Faire glisser vers la gauche<br/>                                            | Appuyez sur l’écran pour sélectionner l’objet à déplacer, puis faites glisser après avoir sélectionné l’objet.<br/>                                                                                                                     | ISG \_ glissement envoyé lorsque l’opération de glisser-déplacer commence.<br/>                                                                                          | WM \_ LBUTTONDOWN envoyé au démarrage de l’opération glisser, suivi d’une série de messages de déplacement de la souris, puis d’un \_ événement WM LBUTTONUP.<br/> | faites glisser la sélection, comme dans Microsoft Word lors du démarrage avec une adresse IP ; Sélectionnez plusieurs mots. Faites glisser, comme lorsque vous faites glisser un objet dans Windows ; défilement.<br/>                            |
| Appuyer et maintenir suivi d’un glissement<br/> | Faites glisser le bouton droit<br/>                                           | Appuyez sur l’écran pour sélectionner l’objet à déplacer. Maintenez le bouton de la souris enfoncé, puis faites glisser pour déplacer l’objet. Soulevez le stylet pour afficher un menu contextuel.<br/>                                                   | ISG \_ HOLDENTER envoyé lorsque le stylet est arrêté pendant un certain temps. ISG \_ RIGHTDRAG envoyé au démarrage de l’opération glisser.<br/>                           | WM \_ RBUTTONDOWN envoyé au démarrage de l’opération glisser, suivi d’une série de messages de déplacement de la souris, suivi d’un \_ événement WM RBUTTONUP.<br/>     | Faites glisser, comme lorsque vous faites glisser un objet ou une sélection suivi d’un menu contextuel.<br/>                                                                                             |
| Pointage du stylet<br/>                         | Pointage de la souris<br/>                                          | Maintenez le stylet stable à une petite distance de l’écran.<br/>                                                                                                                                                                 | \_Événement ISG HOVERENTER envoyé initialement. Lorsque l’intervalle de survol est terminé, ISG \_ HOVERLEAVEis envoyé.<br/>                           | Aucun message de souris équivalent.<br/>                                                                                               | Affichez l’info-bulle, les effets de repositionnement et les autres comportements de pointage de la souris.<br/>                                                                                                     |
| Tremblement dans l’air<br/>                      | Afficher le **panneau de saisie Tablet PC**. Aucun équivalent de la souris.<br/> | Déplacez le stylet rapidement d’un côté à l’autre, en maintenant le Conseil ci-dessus, mais dans la plage de, l’écran.<br/>                                                                                                                          | L’événement n’est pas passé à l’application.<br/>                                                                                   | Aucun message de souris équivalent.<br/>                                                                                               | Nouveau, spécifique à Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Spécification des interactions de stylet et Touch

Par défaut, votre fenêtre recevra tous les événements de mouvement système et utilisera le modèle d’interaction par défaut. Certains éléments de ce modèle peuvent interférer avec votre application. vous pouvez donc les désactiver de manière sélective en répondant [**au \_ \_ message WM QUERYSYSTEMGESTURESTATUS**](wm-tablet-querysystemgesturestatus-message.md) dans votre WndProc.

 

 
