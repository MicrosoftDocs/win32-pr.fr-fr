---
title: Fonctions d’entrée de souris
description: Fonctions d’entrée de souris
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b9dffed2446addaced30341364d2f755fcd4c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192556"
---
# <a name="mouse-input-functions"></a>Fonctions d’entrée de souris


## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br /> | Publie des messages lorsque le pointeur de la souris quitte une fenêtre ou pointe sur une fenêtre pendant un laps de temps spécifié. Cette fonction appelle <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si elle existe, sinon elle l’émule.<br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br /> | Capture la souris et suit ses déplacements jusqu'à ce que l'utilisateur relâche le bouton gauche, appuie sur la touche Échap ou déplace la souris en dehors du rectangle de glissement entourant le point spécifié. La largeur et la hauteur du rectangle de glissement sont spécifiées par le <strong>SM_CXDRAG</strong> et <strong>SM_CYDRAG</strong> valeurs retournées par la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> .<br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br /> | Récupère un handle vers la fenêtre (le cas échéant) qui a capturé la souris. Une seule fenêtre à la fois peut capturer la souris ; Cette fenêtre reçoit l’entrée de la souris, que le curseur figure ou non dans ses limites. <br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br /> | Récupère le temps de double-clic actuel pour la souris. Un double-clic est une série de deux clics du bouton de la souris, le second se produisant dans un délai spécifié après le premier. L’heure du double-clic correspond au nombre maximal de millisecondes qui peuvent se produire entre le premier et le deuxième clic d’un double-clic. La durée maximale de double-clic est de 5000 millisecondes.<br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br /> | Récupère un historique allant jusqu’à 64 coordonnées précédentes de la souris ou du stylet.<br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br /> | La fonction <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> synthétise le mouvement de la souris et les clics de bouton.<br /><blockquote>[!Note]<br />Cette fonction a été remplacée. Utilisez plutôt <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br /> | Libère la capture de la souris d’une fenêtre dans le thread actuel et restaure le traitement d’entrée de souris normal. Une fenêtre qui a capturé la souris reçoit toutes les entrées de la souris, quelle que soit la position du curseur, sauf si l’utilisateur clique sur un bouton de la souris alors que la zone réactive du curseur se trouve dans la fenêtre d’un autre thread. <br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br /> | Définit la capture de la souris sur la fenêtre spécifiée qui appartient au thread actuel.<br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a><br /> | Définit l’heure du double-clic de la souris. Un double-clic est une série de deux clics du bouton de la souris, le second se produisant dans un délai spécifié après le premier. L’heure du double-clic correspond au nombre maximal de millisecondes qui peuvent se produire entre le premier et le deuxième clic d’un double-clic. <br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br /> | Inverse ou restaure la signification des boutons gauche et droit de la souris. <br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br /> | Publie des messages lorsque le pointeur de la souris quitte une fenêtre ou pointe sur une fenêtre pendant un laps de temps spécifié.<br /><blockquote>[!Note]<br />La fonction <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> appelle <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si elle existe, sinon <strong>_TrackMouseEvent</strong> émule <strong>TrackMouseEvent</strong>.</blockquote><br /> | 




 

 

