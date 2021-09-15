---
description: Utilisation des menus de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Utilisation des menus de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238763"
---
# <a name="working-with-dvd-menus"></a>Utilisation des menus de DVD

Le navigateur DVD peut afficher un menu lorsque l’utilisateur active un bouton ou lorsque le navigateur accède au premier domaine de lecture. Pour afficher un menu par programme, appelez la méthode [**IDvdControl2 :: ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .

Il existe plusieurs façons de sélectionner des boutons de menu par programme :

-   Pour sélectionner un bouton par numéro, appelez [**IDvdControl2 :: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Les boutons sont numérotés de 1 à 36. La méthode [**IDvdInfo2 :: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) retourne le nombre de boutons disponibles.
-   Pour sélectionner un bouton par rapport à la position du bouton actuellement sélectionné, appelez [**IDvdControl2 :: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Vous pouvez sélectionner un bouton dans la direction vers le haut, vers le bas, à gauche ou à droite.
-   Pour sélectionner un bouton par ses coordonnées dans la fenêtre, appelez [**IDvdControl2 :: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Cette méthode prend les coordonnées (x, y) relatives à la zone cliente de la fenêtre vidéo. (Pour le mode sans fenêtre, il s’agit de la fenêtre d’application.) S’il n’existe aucun bouton à cet emplacement, la méthode retourne \_ le \_ bouton VFW E DVD \_ no \_ .

De plus, il existe plusieurs façons d’activer un bouton :

-   Pour activer un bouton par nombre, appelez [**IDvdControl2 :: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Pour activer un bouton par ses coordonnées, appelez [**IDvdControl2 :: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Pour activer le bouton qui est actuellement sélectionné, appelez [**IDvdControl2 :: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Si aucun bouton n’est sélectionné, la méthode retourne \_ le \_ bouton VFW E DVD \_ no \_ .

N’oubliez pas que la sélection d’un bouton met simplement en évidence ses bordures. Pour déclencher l’activation de la commande associée, le bouton doit être activé. L’activation d’un bouton par programmation peut être effectuée de différentes manières, mais le bouton doit toujours être sélectionné avant de pouvoir être activé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



